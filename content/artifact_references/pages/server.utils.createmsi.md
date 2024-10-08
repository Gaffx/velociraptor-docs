---
title: Server.Utils.CreateMSI
hidden: true
tags: [Server Artifact]
---

Build an MSI ready for deployment in the current org.

This artifact depends on the following tools:

* <velo-tool-viewer name="VelociraptorWindowsMSI" />
* <velo-tool-viewer name="VelociraptorWindows_x86MSI" />

You can replace those with suitable MSI builds.


<pre><code class="language-yaml">
name: Server.Utils.CreateMSI
description: |
  Build an MSI ready for deployment in the current org.

  This artifact depends on the following tools:

  * &lt;velo-tool-viewer name="VelociraptorWindowsMSI" /&gt;
  * &lt;velo-tool-viewer name="VelociraptorWindows_x86MSI" /&gt;

  You can replace those with suitable MSI builds.

type: SERVER

parameters:
  - name: CustomConfig
    description: Supply a custom client config instead of using the one from the current org
    type: yaml
  - name: AlsoBuild_x86
    description: Also build 32 bit MSI for deployment.
    type: bool

sources:
- query: |
    LET ValidateConfig(Config) = Config.Client.server_urls
          AND Config.Client.ca_certificate =~ "(?ms)-----BEGIN CERTIFICATE-----.+-----END CERTIFICATE-----"
          AND Config.Client.nonce

    LET client_config &lt;= if(condition=ValidateConfig(Config=CustomConfig),
                         then=CustomConfig,
                         else=org()._client_config)

    LET Build(Target) = repack(
        upload_name=format(
          format='Org_%v_%v',
          args=[org().name, inventory_get(tool=Target).Definition.filename]),
        target=Target,
        config=serialize(format='yaml', item=client_config))

    SELECT * FROM chain(a={
       SELECT Build(Target="VelociraptorWindowsMSI") FROM scope()
    }, b={
       SELECT Build(Target="VelociraptorWindows_x86MSI") FROM scope()
       WHERE AlsoBuild_x86
    })

</code></pre>

