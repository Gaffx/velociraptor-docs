---
title: Server.Utils.AddTimeline
hidden: true
tags: [Server Artifact]
---

Adds a new timeline to a super timeline.


<pre><code class="language-yaml">
name: Server.Utils.AddTimeline
description: |
  Adds a new timeline to a super timeline.

type: SERVER

parameters:
  - name: NotebookId
  - name: Timeline
    description: SuperTimeline name
  - name: ChildName
    description: Name of child timeline
  - name: Query
    description: A query that will be parsed and run.
  - name: Key
    description: Sort column for time
  - name: MessageColumn
    description: The name of the column to appear as the message
  - name: RemoveLimit
    description: If specified, we remove the limit clause before adding to the timeline.
    type: bool
  - name: Env
    type: json

sources:
  - query: |
      SELECT timeline_add(
         notebook_id=NotebookId,
         timeline=Timeline,
         name=ChildName,
         message_column=MessageColumn,
         query={
           SELECT * FROM query(query=if(condition=RemoveLimit,
             then=regex_replace(re="(?i)LIMIT [0-9]+", replace="", source=Query),
             else=Query), env=Env)
         },
         key=Key), RemoveLimit
      FROM scope()

</code></pre>

