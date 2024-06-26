---
title: Linux.KapeFiles.CollectFromDirectory
hidden: true
tags: [Client Artifact]
---


Kape is a popular bulk collector tool for triaging a system
quickly. While KAPE itself is not an opensource tool, the logic it
uses to decide which files to collect is encoded in YAML files
hosted on the KapeFiles project
(https://github.com/EricZimmerman/KapeFiles) and released under an
MIT license.

This artifact is automatically generated from these YAML files,
contributed and maintained by the community. This artifact only
encapsulates the KAPE "Targets" - basically a bunch of glob
expressions used for collecting files on the endpoint. We do not
do any post processing these files - we just collect them.

We recommend that timeouts and upload limits be used
conservatively with this artifact because we can upload really
vast quantities of data very quickly.


<pre><code class="language-yaml">
name: Linux.KapeFiles.CollectFromDirectory
description: |

    Kape is a popular bulk collector tool for triaging a system
    quickly. While KAPE itself is not an opensource tool, the logic it
    uses to decide which files to collect is encoded in YAML files
    hosted on the KapeFiles project
    (https://github.com/EricZimmerman/KapeFiles) and released under an
    MIT license.

    This artifact is automatically generated from these YAML files,
    contributed and maintained by the community. This artifact only
    encapsulates the KAPE "Targets" - basically a bunch of glob
    expressions used for collecting files on the endpoint. We do not
    do any post processing these files - we just collect them.

    We recommend that timeouts and upload limits be used
    conservatively with this artifact because we can upload really
    vast quantities of data very quickly.

reference:
  - https://www.kroll.com/en/insights/publications/cyber/kroll-artifact-parser-extractor-kape
  - https://github.com/EricZimmerman/KapeFiles

type: client

parameters:
  - name: Device
    description: Path from where to start the search.
    default: "/mnt/windows_mount"

  - name: _BasicCollection
    description: "Basic Collection (by Phill Moore): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T, Amcache, Amcache, Amcache transaction files, Amcache transaction files, AppCompat PCA Folder, Desktop LNK Files, Desktop LNK Files XP, Event logs Win7+, Event logs Win7+, Event logs XP, GatherLogs, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, PowerShell Console Log, Prefetch, Prefetch, RECYCLER - WinXP, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, Restore point LNK Files XP, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, Start Menu LNK Files, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), Thumbcache DB, User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files, WindowsIndexSearch, XML, XML, XML, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt"
    type: bool
  - name: _KapeTriage
    description: "Calls Kape Triage (by Phill Moore): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T, AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, Action1 Client Application logs, ActivitiesCache.db, Addons, Addons XP, Amcache, Amcache, Amcache transaction files, Amcache transaction files, Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, AppCompat PCA Folder, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, Bookmarks, Bookmarks, Bookmarks, Box Drive Application Metadata, Box Sync Application Metadata, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome Snapshots Folder, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, ComboFix, Cookies, Cookies, Cookies, Cookies XP, Crash Dumps, Crash Dumps, Crash Dumps, Current Session, Current Tabs, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, Cylance Optics Logs, Cylance Program Files Logs, Cylance ProgramData Logs, DWAgent Log Files, Desktop LNK Files, Desktop LNK Files XP, DetectionHistory, Download Metadata, Downloads, Downloads XP, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge WebAssistDatabase, Edge bookmarks, Edge folder, Emsisoft Scan Logs, Event logs Win7+, Event logs Win7+, Event logs XP, Extensions, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, Favicons, Favicons, Favicons XP, Form history, Form history XP, Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata, History, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, ISL AlwaysOn - App Logs, ISL AlwaysOn - Configuration, ISL AlwaysOn - Email Configuration, ISL AlwaysOn Logs - Sessions, ISL AlwaysOn Logs - Sessions List, ISL Light Logs - Sessions, ISLOnline Logs - Session Configurations, ISLOnline Logs - Sessions - *.out, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Level RMM Client Application logs, Local Internet Explorer folder, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, Local User Quarantine, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, Login Data, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Net Monitor Client Config, Net Monitor Client Logs, Net Monitor Server Config, Net Monitor Server Data, Net Monitor Server Logs, Net Monitor Server Temp Folder, Network Action Predictor, Network Persistent State, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, OneDrive Metadata Logs, OneDrive Metadata Settings, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, PowerShell Console Log, Preferences, Preferences, Prefetch, Prefetch, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RECYCLER - WinXP, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, Rclone Config, RealVNC Log, RealVNC Log, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, Reporting and NEL, Restore point LNK Files XP, Roaming Internet Explorer folder, RogueKiller Reports, RustDesk logs, RustDesk logs, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SUM Database (.mdb files), SUPERAntiSpyware Logs, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, SYSTEM user quarantine, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Search, Search XP, Secure Preferences, SecureAge Antvirus Logs, SentinelOne EDR Log, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Shortcuts, Signons, Signons XP, Sophos Logs, Sophos Logs (XP), Splashtop Log Files, Splashtop Log Files in ProgramData, Start Menu LNK Files, Storage Sync, Supremo Connection Logs, Supremo File Transfer Inbox, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), TeamViewer Application Logs, TeamViewer Application User Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, TightVNC Application Logs, Top Sites, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, UltraViewer Connection Log, UltraViewer Service Log, UltraViewer System Logs, UltraViewer User Logs, User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Visited Links, Vivaldi Bookmarks, Vivaldi Calendar, Vivaldi Contacts, Vivaldi Cookies, Vivaldi Download Metadata, Vivaldi Favicons, Vivaldi History, Vivaldi Login Data, Vivaldi Network Action Predictor, Vivaldi Network Persistent State, Vivaldi Notes, Vivaldi Preferences, Vivaldi Sessions Folder, Vivaldi Top Sites, Vivaldi User Tracking, Vivaldi Visited Links, Vivaldi Web Data, WBEM, WBEM, WER Files, WER Files, Web Data, Webappstore, Webappstore XP, Webroot Program Data, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Quarantine, Windows Protect Folder, Windows Protect Folder, Windows Protect Folder, Windows.old RDP Cache Files, XML, XML, XML, Xeox RMM Client Application logs, Yandex Autofill data, Yandex Bookmarks, Yandex Cookies, Yandex Favicons, Yandex History, Yandex Login Data, Yandex Network Action Predictor, Yandex Network Persistent State, Yandex Passman logs, Yandex Preferences, Yandex Sessions Folder, Yandex Shortcuts, Yandex Top Sites, Yandex Visited Links, Yandex Web Data, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt, ccSubSDK Database, mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings, registrationInfo.xml"
    type: bool
  - name: _SANS_Triage
    description: "SANS Triage Collection (by Mark Hallman): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T, .NET CLR UsageLogs (system-scoped), .NET CLR UsageLogs (user-scoped), AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, Action1 Client Application logs, ActivitiesCache.db, Addons, Addons XP, Amcache, Amcache, Amcache transaction files, Amcache transaction files, Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, AppCompat PCA Folder, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, BITS files, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, Bookmarks, Bookmarks, Bookmarks, Box Drive Application Metadata, Box Sync Application Metadata, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome Snapshots Folder, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Cisco Jabber Database, ComboFix, Computer Group Policy files, Cookies, Cookies, Cookies, Cookies XP, Crash Dumps, Crash Dumps, Crash Dumps, Current Session, Current Tabs, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, Cylance Optics Logs, Cylance Program Files Logs, Cylance ProgramData Logs, DWAgent Log Files, Delivery Optimization Trace Logs, Desktop LNK Files, Desktop LNK Files XP, DetectionHistory, Discord Cache Files, Discord Local Storage LevelDB Files, Download Metadata, Downloads, Downloads XP, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge WebAssistDatabase, Edge bookmarks, Edge folder, Emsisoft Scan Logs, Energy-NTKL Trace Logs, Event logs Win7+, Event logs Win7+, Event logs XP, Extensions, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, Favicons, Favicons, Favicons XP, Form history, Form history XP, GatherLogs, Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata, Group Policy Files, HexChat Chat Logs, History, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, ISL AlwaysOn - App Logs, ISL AlwaysOn - Configuration, ISL AlwaysOn - Email Configuration, ISL AlwaysOn Logs - Sessions, ISL AlwaysOn Logs - Sessions List, ISL Light Logs - Sessions, ISLOnline Logs - Session Configurations, ISLOnline Logs - Sessions - *.out, IceChat Chat Logs, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Level RMM Client Application logs, Local Group Policy Files - Registry Policy Files, Local Group Policy Files - Registry Policy Files, Local Group Policy Files - Startup/Shutdown Scripts, Local Group Policy Files - Startup/Shutdown Scripts, Local Group Policy INI Files, Local Internet Explorer folder, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, Local User Quarantine, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, Login Data, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, Mattermost - Chat Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, Microsoft Store WhatsApp Cache, Microsoft Store WhatsApp Local Storage, Microsoft Teams Cache, Microsoft Teams Config, Microsoft Teams IndexedDB Cache, Microsoft Teams Local Storage Cache, Microsoft Teams Logs (Windows 11), NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Net Monitor Client Config, Net Monitor Client Logs, Net Monitor Server Config, Net Monitor Server Data, Net Monitor Server Logs, Net Monitor Server Temp Folder, Network Action Predictor, Network Persistent State, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, OneDrive Metadata Logs, OneDrive Metadata Settings, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, PowerShell Console Log, Preferences, Preferences, Prefetch, Prefetch, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RECYCLER - WinXP, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, Rclone Config, RealVNC Log, RealVNC Log, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, Reporting and NEL, Restore point LNK Files XP, Roaming Internet Explorer folder, RogueKiller Reports, RustDesk logs, RustDesk logs, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SUM Database (.mdb files), SUPERAntiSpyware Logs, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, SYSTEM user quarantine, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Search, Search XP, Secure Preferences, SecureAge Antvirus Logs, SentinelOne EDR Log, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, Shortcuts, Signal Attachments cache, Signal Database, Signal Logs, Signal config.json, Signons, Signons XP, Skype for Destkop v8+ Chromium Cache, Slack - Chat Logs, Slack Cache, Slack Electron Logs, Slack LevelDB Files, Slack Storage, SleepStudy Trace Logs, SleepStudy Trace Logs, Sophos Logs, Sophos Logs (XP), Splashtop Log Files, Splashtop Log Files in ProgramData, Start Menu LNK Files, Storage Sync, Supremo Connection Logs, Supremo File Transfer Inbox, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), TeamViewer Application Logs, TeamViewer Application User Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, Telegram app folder, Telegram downloaded files, Thumbcache DB, TightVNC Application Logs, Top Sites, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, UltraViewer Connection Log, UltraViewer Service Log, UltraViewer System Logs, UltraViewer User Logs, User Group Policy files, User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Viber Config Database, Viber Users Avatars Cache, Viber Users Backgrounds Cache, Viber Users Data Database, Viber Users Thumbnails Cache, Visited Links, Vivaldi Bookmarks, Vivaldi Calendar, Vivaldi Contacts, Vivaldi Cookies, Vivaldi Download Metadata, Vivaldi Favicons, Vivaldi History, Vivaldi Login Data, Vivaldi Network Action Predictor, Vivaldi Network Persistent State, Vivaldi Notes, Vivaldi Preferences, Vivaldi Sessions Folder, Vivaldi Top Sites, Vivaldi User Tracking, Vivaldi Visited Links, Vivaldi Web Data, WBEM, WBEM, WDI Trace Logs 1, WDI Trace Logs 1, WDI Trace Logs 2, WDI Trace Logs 2, WER Files, WER Files, WMI Trace Logs, WMI Trace Logs, Web Data, Webappstore, Webappstore XP, Webroot Program Data, WhatsApp Cache, WhatsApp Local Storage, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Quarantine, Windows Firewall Logs, Windows Firewall Logs, Windows Protect Folder, Windows Protect Folder, Windows Protect Folder, Windows.old RDP Cache Files, WindowsIndexSearch, XML, XML, XML, Xeox RMM Client Application logs, Yandex Autofill data, Yandex Bookmarks, Yandex Cookies, Yandex Favicons, Yandex History, Yandex Login Data, Yandex Network Action Predictor, Yandex Network Persistent State, Yandex Passman logs, Yandex Preferences, Yandex Sessions Folder, Yandex Shortcuts, Yandex Top Sites, Yandex Visited Links, Yandex Web Data, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt, ccSubSDK Database, leveldb (Skype for Desktop +v8), mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+), mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings, main.db (App &lt;v12), main.db Win7+, main.db XP, registrationInfo.xml, s4l-[username].db (App +v8), skype.db (App +v12)"
    type: bool
  - name: _Boot
    description: "$Boot (by Eric Zimmerman): $Boot"
    type: bool
  - name: _J
    description: "$J (by Eric Zimmerman and Andrew Rathbun): $J, $J, $Max, $Max"
    type: bool
  - name: _LogFile
    description: "$LogFile (by Eric Zimmerman): $LogFile"
    type: bool
  - name: _MFT
    description: "$MFT (by Eric Zimmerman): $MFT"
    type: bool
  - name: _MFTMirr
    description: "$MFTMirr (by Teo Kia Meng): $MFTMirr"
    type: bool
  - name: _SDS
    description: "$SDS (by Eric Zimmerman and Andrew Rathbun): $SDS, $SDS"
    type: bool
  - name: _T
    description: "$T (by Eric Zimmerman and Andrew Rathbun): $T, $T"
    type: bool
  - name: 1Password
    description: "1Password Password Manager (by Matt Dawson): 1Password Backup Databases, 1Password Database, 1Password Logs"
    type: bool
  - name: 4KVideoDownloader
    description: "4K Video Downloader (by Andrew Rathbun): 4K Video Downloader, 4K Video Downloader+"
    type: bool
  - name: AVG
    description: "AVG Antivirus Data (by Kirtan Shah and Dhiral Panjwani): AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON"
    type: bool
  - name: AceText
    description: "AceText (by Andrew Rathbun): AceText - Clipboard History"
    type: bool
  - name: AcronisTrueImage
    description: "Acronis True Image (by Andrew Rathbun): Acronis True Image - Database Files, Acronis True Image - Logs, Acronis True Image - Scripts Folder"
    type: bool
  - name: Action1
    description: "Action1 Application Logs (by Andrew Skatoff @DFIR_TNT): Action1 Client Application logs"
    type: bool
  - name: ActiveDirectoryNTDS
    description: "Active Directory NTDS (by Zawadi Done): NTDS"
    type: bool
  - name: ActiveDirectorySysvol
    description: "Active Directory Sysvol (by Zawadi Done): SYSVOL"
    type: bool
  - name: AgentRansack
    description: "Agent Ransack - Free File Searching Utility (by Andrew Rathbun): Agent Ransack Config Logs, Agent Ransack CrashReports Logs, Agent Ransack IndexLog Logs, Agent Ransack Logs"
    type: bool
  - name: Amcache
    description: "Amcache.hve (by Eric Zimmerman): Amcache, Amcache, Amcache transaction files, Amcache transaction files"
    type: bool
  - name: Ammyy
    description: "Ammyy Data (by Drew Ervin): Ammyy Program Data"
    type: bool
  - name: Antivirus
    description: "Antivirus (by Andrew Rathbun): AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, ComboFix, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, Cylance Optics Logs, Cylance Program Files Logs, Cylance ProgramData Logs, DetectionHistory, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Emsisoft Scan Logs, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, Local User Quarantine, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, RogueKiller Reports, SUPERAntiSpyware Logs, SYSTEM user quarantine, SecureAge Antvirus Logs, SentinelOne EDR Log, Sophos Logs, Sophos Logs (XP), Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Webroot Program Data, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Quarantine, ccSubSDK Database, registrationInfo.xml"
    type: bool
  - name: AnyDesk
    description: "AnyDesk (by Andrew Rathbun, Scott Hanson, and Nicole Jao): AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos"
    type: bool
  - name: ApacheAccessLog
    description: "Apache Access Log (by Hadar Yudovich): Apache Access Log"
    type: bool
  - name: AppCompatPCA
    description: "AppCompat PCA Folder (by Andrew Rathbun): AppCompat PCA Folder"
    type: bool
  - name: AppData
    description: "AppData (by Phill Moore): AppData"
    type: bool
  - name: AppXPackages
    description: "AppXPackages (by Nisarg Suthar): AppRepository for AppX, ProgramData Packages for AppX, SystemApps for AppX, UserSpecificPackages for AppX, WindowsApps for AppX"
    type: bool
  - name: ApplicationEvents
    description: "Windows Application Event Log (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP"
    type: bool
  - name: AsperaConnect
    description: "Aspera Connect Log Files (by Dennis Reneau): Aspera Client Logs, Aspera Server Logs"
    type: bool
  - name: AteraAgent
    description: "AteraAgent (by Andrew Rathbun): AteraAgent .ini files, AteraAgent Logs, AteraAgent Logs, AteraAgent Logs, AteraAgent Logs"
    type: bool
  - name: Avast
    description: "Avast Antivirus Data (by Drew Ervin and Dhiral Panjwani): Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs"
    type: bool
  - name: AviraAVLogs
    description: "Avira Logs (by Fabian Murer and Dhiral Panjwani): Avira Activity Logs, Avira Security Logs, Avira VPN Logs"
    type: bool
  - name: BCD
    description: "Boot Configuration Files (by Troy Larson): BCD, BCD Logs"
    type: bool
  - name: BITS
    description: "Microsoft BITS (Background Intelligent Transer Service) persistent files (by Jos Clephas): BITS files"
    type: bool
  - name: BitTorrent
    description: "BitTorrent (by Banaanhangwagen): TorrentClients - BitTorrent"
    type: bool
  - name: Bitdefender
    description: "Bitdefender Antivirus Data (by Drew Ervin, Ahmed Elshaer): Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files"
    type: bool
  - name: BoxDrive_Metadata
    description: "Box Cloud Storage Metadata (by Chad Tilbury): Box Drive Application Metadata, Box Sync Application Metadata"
    type: bool
  - name: BoxDrive_UserFiles
    description: "Box Cloud Storage Files (by Chad Tilbury): Box Drive User Files, Box Sync User Files"
    type: bool
  - name: BraveBrowser
    description: "Brave Browser (by Cassie Doemel): Bookmarks, Cookies, Current Session, Current Tabs, Download Metadata, Favicons, History, Login Data, Network Action Predictor, Network Persistent State, Preferences, Publisher Info DB/Brave Rewards, Quota Manager, Reporting and NEL, Secure Preferences, Sessions Folder, Shortcuts, Top Sites, Visited Links, Web Data"
    type: bool
  - name: BrowserCache
    description: "Browser Caches (by Bjorn Vanhaeren): Brave Cache Folder, Chrome Cache Folder, Chromium Edge Cache Folder, Edge WebcacheV01.dat, Firefox Cache Folder, IE 11 Cache, IE 9/10 Cache, IE Index.dat temp internet files"
    type: bool
  - name: CertUtil
    description: "Certutil (by NVISO (@NVISOsecurity)): INetCache, System CryptnetUrlCache, User CryptnetUrlCache"
    type: bool
  - name: Chrome
    description: "Chrome (by Eric Zimmerman and Andrew Rathbun): Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome Snapshots Folder, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Windows Protect Folder"
    type: bool
  - name: ChromeExtensions
    description: "Chrome Extension Files (by piesecurity): Chrome Extension Files, Chrome Extension Files XP"
    type: bool
  - name: ChromeFileSystem
    description: "Chrome HTML5 File System Contents (by Chad Tilbury): Chrome HTML5 File System Folder"
    type: bool
  - name: CiscoJabber
    description: "Jabber (by Andrew Bannon): Cisco Jabber Database"
    type: bool
  - name: ClipboardMaster
    description: "ClipboardMaster (by Andrew Rathbun): ClipboardMaster - Clipboard History - Backups, ClipboardMaster - Clipboard History - Images, ClipboardMaster - Clipboard History - Text"
    type: bool
  - name: CloudStorage_All
    description: "Cloud Storage Contents and Metadata (by Chad Tilbury and Andrew Rathbun): Box Drive Application Metadata, Box Drive User Files, Box Sync Application Metadata, Box Sync User Files, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox User Files, Google Drive Backup and Sync Metadata, Google Drive Backup and Sync User Files, Google Drive for Desktop Metadata, Idrive Backup Operations, Idrive Backup Schedule, Idrive Backup Summary, Idrive Cleanup Operations, Idrive Configuration, Idrive Delete Operations, Idrive Exclusion Configurations, Idrive Local Drives, Idrive Mapped Drives, Idrive Restore Operations, Idrive SQL Databse, Idrive Schedule History, Idrive Tracefile, Idrive User Details, OneDrive Metadata Logs, OneDrive Metadata Settings, OneDrive User Files, Rclone Config, SugarSync - My SugarSync (Default Location), SugarSync - Shared Folders (Default Location), SugarSync Log File, Windows Protect Folder, pCloud Database, pCloud Database Shared Memory File, pCloud Database WAL File"
    type: bool
  - name: CloudStorage_Metadata
    description: "Cloud Storage Metadata (by Chad Tilbury and Andrew Rathbun, Eric Capuano): Box Drive Application Metadata, Box Sync Application Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata, OneDrive Metadata Logs, OneDrive Metadata Settings, Rclone Config, Windows Protect Folder"
    type: bool
  - name: CloudStorage_OneDriveExplorer
    description: "OneDrive and other files used with OneDriveExplorer (by Brian Maloney): NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, OneDrive Metadata Logs, OneDrive Metadata Settings, RECYCLER - WinXP, RECYCLER - WinXP, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: CombinedLogs
    description: "Collect Event logs, Trace logs, Windows Firewall, PowerShell console logs, and .NET CLR UsageLogs (by Mike Cary, Mark Hallman added the USBDevicelogs target, Thomas DIOT (Qazeer) added the .NET CLR UsageLogs target): .NET CLR UsageLogs (system-scoped), .NET CLR UsageLogs (user-scoped), Delivery Optimization Trace Logs, Energy-NTKL Trace Logs, Event logs Win7+, Event logs Win7+, Event logs XP, PowerShell Console Log, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, SleepStudy Trace Logs, SleepStudy Trace Logs, WDI Trace Logs 1, WDI Trace Logs 1, WDI Trace Logs 2, WDI Trace Logs 2, WMI Trace Logs, WMI Trace Logs, Windows Firewall Logs, Windows Firewall Logs"
    type: bool
  - name: Combofix
    description: "ComboFix Antivirus Data (by Drew Ervin): ComboFix"
    type: bool
  - name: ConfluenceLogs
    description: "Confluence Log Files (by Eric Capuano): Confluence Wiki Log Files, Confluence Wiki Log Files"
    type: bool
  - name: Cybereason
    description: "Cybereason Sensor/Detection Logs (by piesecurity): Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs"
    type: bool
  - name: Cylance
    description: "Cylance Antivirus Logs (by Ron Rader): Cylance Optics Logs, Cylance Program Files Logs, Cylance ProgramData Logs"
    type: bool
  - name: DC__
    description: "DC++ (by Andrew Rathbun): DC++ Chat Logs"
    type: bool
  - name: DWAgent
    description: "DWAgent Log Files (by Ron Rader): DWAgent Log Files"
    type: bool
  - name: Debian
    description: "Debian on Windows Subsystem for Linux (by Matt Dawson): Debian WSL .bash_history, Debian WSL .bashrc, Debian WSL .profile, Debian WSL /etc/bash.bashrc, Debian WSL /etc/crontab, Debian WSL /etc/debian_version, Debian WSL /etc/fstab, Debian WSL /etc/group, Debian WSL /etc/hostname, Debian WSL /etc/hosts, Debian WSL /etc/os-release, Debian WSL /etc/passwd, Debian WSL /etc/profile, Debian WSL /etc/shadow, Debian WSL /etc/timezone, Debian WSL Apt Logs, Debian WSL User Crontabs, Debian WSL ext4.vhdx"
    type: bool
  - name: DirectoryOpus
    description: "Directory Opus (by Andrew Rathbun): Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus"
    type: bool
  - name: DirectoryTraversal_AudioFiles
    description: "Find audio files covering a multitude of formats (by Andrew Rathbun): Audio files"
    type: bool
  - name: DirectoryTraversal_ExcelDocuments
    description: "Find Excel and Excel alternative documents (by Andrew Rathbun): Excel and Excel-like Documents"
    type: bool
  - name: DirectoryTraversal_PDFDocuments
    description: "Find PDF and PDF alternative documents (by Andrew Rathbun): PDF and PDF-like Documents"
    type: bool
  - name: DirectoryTraversal_PictureFiles
    description: "Find picture files covering a multitude of formats (by Andrew Rathbun): Picture files"
    type: bool
  - name: DirectoryTraversal_SQLiteDatabases
    description: "Find files with common SQLite file extensions (by Andrew Rathbun): SQLite Files (.db* and .sqlite*)"
    type: bool
  - name: DirectoryTraversal_VideoFiles
    description: "Find video files covering a multitude of formats (by Andrew Rathbun): Video files"
    type: bool
  - name: DirectoryTraversal_WildCardExample
    description: "Find zip archives (by Eric Zimmerman): Zips"
    type: bool
  - name: DirectoryTraversal_WordDocuments
    description: "Find Word and Word alternative documents (by Andrew Rathbun): Word and Word-like Documents"
    type: bool
  - name: Discord
    description: "Discord Cache and LevelDB Files (by Christian Johansen and Matt Dawson): Discord Cache Files, Discord Local Storage LevelDB Files"
    type: bool
  - name: DoubleCommander
    description: "Double Commander (by Andrew Rathbun): Double Commander - FTP Log, Double Commander - doublecmd.xml, Double Commander - history.xml, Double Commander - multiarc.ini, Double Commander - pixmaps.txt, Double Commander - session.ini, Double Commander - shortcuts.scf"
    type: bool
  - name: Drivers
    description: "Windows Drivers (by Zawadi Done): Drivers"
    type: bool
  - name: Dropbox_Metadata
    description: "Dropbox Cloud Storage Metadata (by Chad Tilbury and Andrew Rathbun): Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Windows Protect Folder"
    type: bool
  - name: Dropbox_UserFiles
    description: "Dropbox Cloud Storage Files (by Chad Tilbury): Dropbox User Files"
    type: bool
  - name: EFCommander
    description: "EF Commander (by Andrew Rathbun): EF Commander - .ini File"
    type: bool
  - name: ESET
    description: "ESET Antivirus Data (by Drew Ervin, Phill Moore): ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Local User Quarantine, SYSTEM user quarantine"
    type: bool
  - name: Edge
    description: "Edge (by Phill Moore): Edge folder"
    type: bool
  - name: EdgeChromium
    description: "Microsoft Edge Chromium Artifacts (by Chad Tilbury and Andrew Rathbun): Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge WebAssistDatabase, Edge bookmarks, Windows Protect Folder"
    type: bool
  - name: EdgeChromiumExtensions
    description: "Edge Chromium Extension Files (by cardinsou): Edge Chromium Extension Files"
    type: bool
  - name: Emsisoft
    description: "Emsisoft Antivirus Logs (by blueskycyber): Emsisoft Scan Logs"
    type: bool
  - name: EncapsulationLogging
    description: "EncapsulationLogging (by Troy Larson): EncapsulationLogging, EncapsulationLogging, EncapsulationLogging Logs, EncapsulationLogging Logs"
    type: bool
  - name: EventLogs_RDP
    description: "Collect Win7+ RDP related Event logs (by Mark Hallman, esecrpm): Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+, Event logs Win7+"
    type: bool
  - name: EventLogs
    description: "Event logs (by Eric Zimmerman): Event logs Win7+, Event logs Win7+, Event logs XP"
    type: bool
  - name: EventTraceLogs
    description: "Event Trace Logs (by Mark Hallman): Delivery Optimization Trace Logs, Energy-NTKL Trace Logs, SleepStudy Trace Logs, SleepStudy Trace Logs, WDI Trace Logs 1, WDI Trace Logs 1, WDI Trace Logs 2, WDI Trace Logs 2, WMI Trace Logs, WMI Trace Logs"
    type: bool
  - name: EventTranscriptDB
    description: "EventTranscript.db (and other files related to Telemetry and Diagnostic Data) (by Andrew Rathbun and Josh Mitchell): EventTranscript.db, EventTranscript.db, Microsoft Office Diagnostic Logs"
    type: bool
  - name: Evernote
    description: "Evernote (by Matt Dawson): Evernote Accounts, Evernote Notebook Snippets, Evernote Notebooks"
    type: bool
  - name: Everything__VoidTools_
    description: "Everything (VoidTools) (by Andrew Rathbun): Everything (VoidTools), Everything (VoidTools) - .ini file, Everything (VoidTools) - Run History, Everything (VoidTools) - Search History"
    type: bool
  - name: EvidenceOfExecution
    description: "Evidence of execution related files (by Eric Zimmerman): Amcache, Amcache, Amcache transaction files, Amcache transaction files, AppCompat PCA Folder, Prefetch, Prefetch, RecentFileCache, RecentFileCache, Syscache, Syscache transaction files"
    type: bool
  - name: Exchange
    description: "Exchange Log Files (by Keith Twombley): Exchange TransportRoles log files, Exchange client access log files"
    type: bool
  - name: ExchangeClientAccess
    description: "Exchange Client Access Log Files (by Keith Twombley): Exchange client access log files"
    type: bool
  - name: ExchangeCve_2021_26855
    description: "Exchange Server Vulnerability *.Compiled Files (by Dennis Reneau): Exchange Server Modified Compiled Files, Exchange Server Modified Compiled Files, Exchange Server Modified Compiled Files, Exchange Server Modified Compiled Files"
    type: bool
  - name: ExchangeTransport
    description: "Exchange Transport Log Files (by Keith Twombley): Exchange TransportRoles log files"
    type: bool
  - name: FSecure
    description: "F-Secure Antivirus Data (by Drew Ervin): F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs"
    type: bool
  - name: FTPClients
    description: "FTP Clients (by Andrew Rathbun): FileZilla Log Files, FileZilla SQLite3 Log Files, FileZilla Server XML Log Files, FileZilla XML Log Files, WinSCP (.ini file)"
    type: bool
  - name: Fences
    description: "Fences (by Andrew Rathbun): Fences - Desktop Screenshots"
    type: bool
  - name: FileExplorerReplacements
    description: "File Explorer Replacements (by Andrew Rathbun): Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Directory Opus, Double Commander - FTP Log, Double Commander - doublecmd.xml, Double Commander - history.xml, Double Commander - multiarc.ini, Double Commander - pixmaps.txt, Double Commander - session.ini, Double Commander - shortcuts.scf, EF Commander - .ini File, Free Commander - Backup Settings, Free Commander - FTP Log, Free Commander - FTP Related Information, Free Commander - FreeCommander.fav.xml, Free Commander - FreeCommander.ftp.ini, Free Commander - FreeCommander.hist.ini, Free Commander - FreeCommander.ini, Midnight Commander -- All Configuation Files, Multi Commander - Application Folder, Multi Commander - Config Folder, Multi Commander - Log File, Multi Commander - Log Folder, Multi Commander - UserData Folder, One Commander - All Configuration Files, One Commander - Other Configuration Files, Q-Dir - .ini File, Q-Dir - .qdr file, SpeedCommander - .ini File, Tablacus Explorer - remember.xml, Tablacus Explorer - window.xml, Tablacus Explorer - window1.xml, Total Commander - .ini File, Total Commander - FTP .ini File, Total Commander - FTP Logs, Total Commander - File Tree, Total Commander - Frequent Directory Listing, Total Commander - Log File, Total Commander - Temp Files Created During Folder Traversal, XYplorer - .dat files, XYplorer - .ini file, XYplorer - .ini file for each respective pane, XYplorer - AutoBackup folder"
    type: bool
  - name: FileSystem
    description: "File system metadata (by Eric Zimmerman): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T"
    type: bool
  - name: FileZillaClient
    description: "FileZilla XML and SQLite Log Files (by Dennis Reneau): FileZilla SQLite3 Log Files, FileZilla XML Log Files"
    type: bool
  - name: FileZillaServer
    description: "FileZilla Server Logs (by Andrew Rathbun): FileZilla Log Files, FileZilla Server XML Log Files"
    type: bool
  - name: Firefox
    description: "Firefox (by Eric Zimmerman and Andrew Rathbun): Addons, Addons XP, Bookmarks, Bookmarks, Cookies, Cookies, Cookies XP, Downloads, Downloads XP, Extensions, Favicons, Favicons XP, Form history, Form history XP, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, Preferences, Protections, Search, Search XP, Sessionstore, Sessionstore Folder, Sessionstore XP, Signons, Signons XP, Storage Sync, Webappstore, Webappstore XP"
    type: bool
  - name: FreeCommander
    description: "FreeCommander XE (by Andrew Rathbun): Free Commander - Backup Settings, Free Commander - FTP Log, Free Commander - FTP Related Information, Free Commander - FreeCommander.fav.xml, Free Commander - FreeCommander.ftp.ini, Free Commander - FreeCommander.hist.ini, Free Commander - FreeCommander.ini"
    type: bool
  - name: FreeDownloadManager
    description: "Free Download Manager (by Matt Dawson): FDM Backup Info, FDM Database, FDM Database (userdata.zip)"
    type: bool
  - name: FreeFileSync
    description: "FreeFileSync (by Andrew Rathbun): FreeFileSync"
    type: bool
  - name: Freenet
    description: "Freenet (by Charlie Rubisoff): Freenet, Freenet, Freenet, Freenet, Freenet"
    type: bool
  - name: FrostWire
    description: "FrostWire (by Andrew Rathbun): FrostWire AppData, FrostWire AppData, FrostWire Downloads"
    type: bool
  - name: Gigatribe
    description: "Gigatribe Files (by Linus Nissi): Gigatribe Files Windows Vista/7/8/10, Gigatribe Files Windows XP, Gigatribe Files Windows XP"
    type: bool
  - name: GoogleDriveBackupSync_UserFiles
    description: "Google Backup and Sync Storage Files (by Chad Tilbury): Google Drive Backup and Sync User Files"
    type: bool
  - name: GoogleDrive_Metadata
    description: "Google Drive Metadata (by Chad Tilbury): Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata"
    type: bool
  - name: GoogleEarth
    description: "Google Earth (by Guus Beckers): Google Earth My Places Backup file, Google Earth My Places Backup file (XP), Google Earth My Places file, Google Earth My Places file (XP)"
    type: bool
  - name: GroupPolicy
    description: "Current Group Policy Enforcement (by piesecurity): Computer Group Policy files, Group Policy Files, Local Group Policy Files - Registry Policy Files, Local Group Policy Files - Registry Policy Files, Local Group Policy Files - Startup/Shutdown Scripts, Local Group Policy Files - Startup/Shutdown Scripts, Local Group Policy INI Files, User Group Policy files"
    type: bool
  - name: HeidiSQL
    description: "HeidiSQL (by Hyun Yi @hyuunnn): HeidiSQL (tabs.ini), HeidiSQL Backup files (*.sql)"
    type: bool
  - name: HexChat
    description: "HexChat (by Andrew Rathbun): HexChat Chat Logs"
    type: bool
  - name: HitmanPro
    description: "HitmanPro Antivirus Data (by Drew Ervin): HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs"
    type: bool
  - name: IISConfiguration
    description: "IIS (by NVISO (@NVISOsecurity)): IIS administration.config, IIS applicationHost.config, IIS redirection.config, web.config"
    type: bool
  - name: IISLogFiles
    description: "IIS Log Files (by Troy Larson): IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files"
    type: bool
  - name: IRCClients
    description: "IRC Clients (by Andrew Rathbun): HexChat Chat Logs, IceChat Chat Logs, mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+)"
    type: bool
  - name: ISLOnline
    description: "ISLOnline Remote Access Tool (by Thomas Burnette): ISL AlwaysOn - App Logs, ISL AlwaysOn - Configuration, ISL AlwaysOn - Email Configuration, ISL AlwaysOn Logs - Sessions, ISL AlwaysOn Logs - Sessions List, ISL Light Logs - Sessions, ISLOnline Logs - Session Configurations, ISLOnline Logs - Sessions - *.out"
    type: bool
  - name: IceChat
    description: "IceChat (by Andrew Rathbun): IceChat Chat Logs"
    type: bool
  - name: Idrive
    description: "Idrive Backup Artifacts (by Thomas Burnette): Idrive Backup Operations, Idrive Backup Schedule, Idrive Backup Summary, Idrive Cleanup Operations, Idrive Configuration, Idrive Delete Operations, Idrive Exclusion Configurations, Idrive Local Drives, Idrive Mapped Drives, Idrive Restore Operations, Idrive SQL Databse, Idrive Schedule History, Idrive Tracefile, Idrive User Details"
    type: bool
  - name: ImgBurn
    description: "ImgBurn (by Chuck Whitson): ImgBurn - Application Log File"
    type: bool
  - name: InternetExplorer
    description: "Internet Explorer (by Eric Zimmerman): IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Local Internet Explorer folder, Roaming Internet Explorer folder"
    type: bool
  - name: IrfanView
    description: "IrfanView (by Andrew Rathbun): IrfanView Configuration File"
    type: bool
  - name: JDownloader2
    description: "JDownloader 2 (by Matt Dawson): JDownloader 2.0 Download Lists, JDownloader 2.0 General Settings, JDownloader 2.0 Link Collector, JDownloader 2.0 Link Grabber Settings, JDownloader 2.0 Proxy Settings"
    type: bool
  - name: JavaWebCache
    description: "Java WebStart Cache - (IDX Files) (by piesecurity): Java WebStart Cache System level, Java WebStart Cache System level, Java WebStart Cache System level (SysWow64), Java WebStart Cache System level (SysWow64), Java WebStart Cache System level (SysWow64) - IE Protected Mode, Java WebStart Cache System level (SysWow64) - IE Protected Mode, Java WebStart Cache System level - IE Protected Mode, Java WebStart Cache System level - IE Protected Mode, Java WebStart Cache User Level - Default, Java WebStart Cache User Level - IE Protected Mode, Java WebStart Cache User Level - XP"
    type: bool
  - name: Kali
    description: "Kali on Windows Subsystem for Linux (by Matt Dawson): Kali WSL .bash_history, Kali WSL .bashrc, Kali WSL .profile, Kali WSL /etc/bash.bashrc, Kali WSL /etc/crontab, Kali WSL /etc/debian_version, Kali WSL /etc/fstab, Kali WSL /etc/group, Kali WSL /etc/hostname, Kali WSL /etc/hosts, Kali WSL /etc/os-release, Kali WSL /etc/passwd, Kali WSL /etc/profile, Kali WSL /etc/shadow, Kali WSL /etc/timezone, Kali WSL Apt Logs, Kali WSL User Crontabs, Kali WSL ext4.vhdx"
    type: bool
  - name: KapeTriage
    description: "KapeTriage collects most of the files needed for a DFIR Investigation. This Target pulls evidence from File System files, Registry Hives, Event Logs, Scheduled Tasks, Evidence of Execution, SRUM data, SUM data, Cloud metadata, WER, WBEM, Web Browser data (IE/Edge, Chrome, Mozilla history), LNK Files, JumpLists, 3rd party remote access software logs, 3rd party antivirus software logs, Windows 10/11 Timeline database, and $I Recycle Bin files. (by Scott Downie): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T, AVG AV Logs, AVG AV Logs (XP), AVG AV Report Logs (XP), AVG FileInfo DB, AVG Persistent Logs, AVG Report Logs, AVG lsdbj2 JSON, Action1 Client Application logs, ActivitiesCache.db, Addons, Addons XP, Amcache, Amcache, Amcache transaction files, Amcache transaction files, Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, AppCompat PCA Folder, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Avast AV Index, Avast AV Logs, Avast AV Logs (XP), Avast AV User Logs, Avast Icarus Logs, Avast Persistent Data Logs, Avira Activity Logs, Avira Security Logs, Avira VPN Logs, Bitdefender Endpoint Security Logs, Bitdefender Internet Security Logs, Bitdefender SQLite DB Files, Bookmarks, Bookmarks, Bookmarks, Box Drive Application Metadata, Box Sync Application Metadata, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome Snapshots Folder, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, ComboFix, Cookies, Cookies, Cookies, Cookies XP, Crash Dumps, Crash Dumps, Crash Dumps, Current Session, Current Tabs, Cybereason Anti-Ransomware Logs, Cybereason Application Control and NGAV Logs, Cybereason Sensor Communications and Anti-Malware Logs, Cylance Optics Logs, Cylance Program Files Logs, Cylance ProgramData Logs, DWAgent Log Files, Desktop LNK Files, Desktop LNK Files XP, DetectionHistory, Download Metadata, Downloads, Downloads XP, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, ESET NOD32 AV Logs, ESET NOD32 AV Logs, ESET NOD32 AV Logs (XP), ESET Remote Administrator Logs, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge WebAssistDatabase, Edge bookmarks, Edge folder, Emsisoft Scan Logs, Event logs Win7+, Event logs Win7+, Event logs XP, Extensions, F-Secure Logs, F-Secure Scheduled Scan Reports, F-Secure User Logs, Favicons, Favicons, Favicons XP, Form history, Form history XP, Google Drive Backup and Sync Metadata, Google Drive for Desktop Metadata, History, HitmanPro Alert Logs, HitmanPro Database, HitmanPro Logs, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, ISL AlwaysOn - App Logs, ISL AlwaysOn - Configuration, ISL AlwaysOn - Email Configuration, ISL AlwaysOn Logs - Sessions, ISL AlwaysOn Logs - Sessions List, ISL Light Logs - Sessions, ISLOnline Logs - Session Configurations, ISLOnline Logs - Sessions - *.out, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Level RMM Client Application logs, Local Internet Explorer folder, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, Local User Quarantine, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, Login Data, MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs, McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs, McAfee ePO Logs, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Net Monitor Client Config, Net Monitor Client Logs, Net Monitor Server Config, Net Monitor Server Data, Net Monitor Server Logs, Net Monitor Server Temp Folder, Network Action Predictor, Network Persistent State, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, OneDrive Metadata Logs, OneDrive Metadata Settings, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, PowerShell Console Log, Preferences, Preferences, Prefetch, Prefetch, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RECYCLER - WinXP, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, Rclone Config, RealVNC Log, RealVNC Log, RecentFileCache, RecentFileCache, Recycle Bin - Windows Vista+, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, Reporting and NEL, Restore point LNK Files XP, Roaming Internet Explorer folder, RogueKiller Reports, RustDesk logs, RustDesk logs, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM, SUM Database (.mdb files), SUPERAntiSpyware Logs, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, SYSTEM user quarantine, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Search, Search XP, Secure Preferences, SecureAge Antvirus Logs, SentinelOne EDR Log, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Shortcuts, Signons, Signons XP, Sophos Logs, Sophos Logs (XP), Splashtop Log Files, Splashtop Log Files in ProgramData, Start Menu LNK Files, Storage Sync, Supremo Connection Logs, Supremo File Transfer Inbox, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, Syscache, Syscache transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), TeamViewer Application Logs, TeamViewer Application User Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, TightVNC Application Logs, Top Sites, TotalAV Logs, TotalAV Logs, Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs, UltraViewer Connection Log, UltraViewer Service Log, UltraViewer System Logs, UltraViewer User Logs, User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files, VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+), Visited Links, Vivaldi Bookmarks, Vivaldi Calendar, Vivaldi Contacts, Vivaldi Cookies, Vivaldi Download Metadata, Vivaldi Favicons, Vivaldi History, Vivaldi Login Data, Vivaldi Network Action Predictor, Vivaldi Network Persistent State, Vivaldi Notes, Vivaldi Preferences, Vivaldi Sessions Folder, Vivaldi Top Sites, Vivaldi User Tracking, Vivaldi Visited Links, Vivaldi Web Data, WBEM, WBEM, WER Files, WER Files, Web Data, Webappstore, Webappstore XP, Webroot Program Data, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Quarantine, Windows Protect Folder, Windows Protect Folder, Windows Protect Folder, Windows.old RDP Cache Files, XML, XML, XML, Xeox RMM Client Application logs, Yandex Autofill data, Yandex Bookmarks, Yandex Cookies, Yandex Favicons, Yandex History, Yandex Login Data, Yandex Network Action Predictor, Yandex Network Persistent State, Yandex Passman logs, Yandex Preferences, Yandex Sessions Folder, Yandex Shortcuts, Yandex Top Sites, Yandex Visited Links, Yandex Web Data, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt, ccSubSDK Database, mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings, registrationInfo.xml"
    type: bool
  - name: Kaseya
    description: "Kaseya Data (by Drew Ervin and Andrew Rathbun): Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log"
    type: bool
  - name: Keepass
    description: "Keepass (by Vito Alfano): Keepass Application Details, Keepass Config Xml, Keepass User Config"
    type: bool
  - name: KeepassXC
    description: "KeepassXC (by Vito Alfano): Keepass Local Ini, Keepass Roaming Ini"
    type: bool
  - name: LNKFilesAndJumpLists
    description: "LNK Files and jump lists (by Eric Zimmerman, Andrew Rathbun, Yogesh Khatri): Desktop LNK Files, Desktop LNK Files XP, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Restore point LNK Files XP, Start Menu LNK Files"
    type: bool
  - name: Level
    description: "Level.io Application Logs (by Andrew Skatoff @DFIR_TNT): Level RMM Client Application logs"
    type: bool
  - name: LinuxOnWindowsProfileFiles
    description: "Linux on Windows Profile Files (by Troy Larson): .bash_history, .bash_logout, .bashrc, .profile"
    type: bool
  - name: LiveUserFiles
    description: "Live User Files (by Mark Hallman): User Files - Desktop, User Files - Documents, User Files - Downloads, User Files - Dropbox"
    type: bool
  - name: LogFiles
    description: "LogFiles (includes SUM) (by Fabian Murer): Error logging, LogFiles, LogFiles"
    type: bool
  - name: LogMeIn
    description: "LogMeIn Data (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, LogMeIn Application Logs, LogMeIn ProgramData Logs"
    type: bool
  - name: MOF
    description: "MOF files (WMI) (by Eric Zimmerman): MOF files"
    type: bool
  - name: MSSQLErrorLog
    description: "MS SQL ErrorLogs (by Troy Larson): MS SQL Errorlog, MS SQL Errorlogs"
    type: bool
  - name: MacriumReflect
    description: "Macrium Reflect (by Andrew Rathbun): Macrium Reflect, Macrium Reflect, Macrium Reflect"
    type: bool
  - name: Malwarebytes
    description: "Malwarebytes Data (by Drew Ervin &amp; Kirtan Shah): MalwareBytes Anti-Malware Logs, MalwareBytes Anti-Malware Scan Logs, MalwareBytes Anti-Malware Scan Results Logs, MalwareBytes Anti-Malware Service Logs"
    type: bool
  - name: ManageEngineLogs
    description: "ManageEngine Log Files (by Whitney Champion, Phill Moore): ManageEngine ADSelfService Plus Log Files, ManageEngine Desktop Central Log Files"
    type: bool
  - name: Mattermost
    description: "Mattermost (by Andrew Rathbun): Mattermost - Chat Logs"
    type: bool
  - name: McAfee
    description: "McAfee Log Files (by Sam Smoker): McAfee Desktop Protection Logs, McAfee Desktop Protection Logs XP, McAfee Endpoint Security Logs, McAfee Endpoint Security Logs, McAfee VirusScan Logs"
    type: bool
  - name: McAfee_ePO
    description: "McAfee ePO Log Files (by Doug Metz): McAfee ePO Logs"
    type: bool
  - name: MediaMonkey
    description: "MediaMonkey (by Andrew Rathbun): MediaMonkey - Media SQLite Database, MediaMonkey - MediaMonkey.ini"
    type: bool
  - name: Megasync
    description: "MegaSync Data Collection (by Vito Alfano): MegaSync Folder"
    type: bool
  - name: MemoryFiles
    description: "Memory Files (by Ahmed Elshaer, Teo Kia Meng): Small Memory Dump directory, Small Memory Dump directory, hiberfil.sys, pagefile.sys, swapfile.sys"
    type: bool
  - name: MessagingClients
    description: "Messaging and communication apps (by Gregor Wegberg): Cisco Jabber Database, Discord Cache Files, Discord Local Storage LevelDB Files, HexChat Chat Logs, IceChat Chat Logs, Mattermost - Chat Logs, Microsoft Store WhatsApp Cache, Microsoft Store WhatsApp Local Storage, Microsoft Teams Cache, Microsoft Teams Config, Microsoft Teams IndexedDB Cache, Microsoft Teams Local Storage Cache, Microsoft Teams Logs (Windows 11), Signal Attachments cache, Signal Database, Signal Logs, Signal config.json, Skype for Destkop v8+ Chromium Cache, Slack - Chat Logs, Slack Cache, Slack Electron Logs, Slack LevelDB Files, Slack Storage, Telegram app folder, Telegram downloaded files, Viber Config Database, Viber Users Avatars Cache, Viber Users Backgrounds Cache, Viber Users Data Database, Viber Users Thumbnails Cache, WhatsApp Cache, WhatsApp Local Storage, leveldb (Skype for Desktop +v8), mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+), main.db (App &lt;v12), main.db Win7+, main.db XP, s4l-[username].db (App +v8), skype.db (App +v12)"
    type: bool
  - name: MicrosoftOfficeBackstage
    description: "Microsoft Office Backstage (by Brian Maloney): Microsoft Office Backstage"
    type: bool
  - name: MicrosoftOneNote
    description: "Microsoft OneNote (by Andrew Rathbun): Microsoft OneNote - AccessibilityCheckerIndex, Microsoft OneNote - FullTextSearchIndex, Microsoft OneNote - RecentNotebooks_SeenURLs, Microsoft OneNote - RecentSearches, Microsoft OneNote - User NoteTags"
    type: bool
  - name: MicrosoftStickyNotes
    description: "Microsoft Sticky Notes (by Andrew Rathbun): Microsoft Sticky Notes - 1607 and later, Microsoft Sticky Notes - Windows 7, 8, and 10 version 1511 and earlier"
    type: bool
  - name: MicrosoftTeams
    description: "Microsoft Teams (by Matt Dawson and Andrew Rathbun): Microsoft Teams Cache, Microsoft Teams Config, Microsoft Teams IndexedDB Cache, Microsoft Teams Local Storage Cache, Microsoft Teams Logs (Windows 11)"
    type: bool
  - name: MicrosoftToDo
    description: "Microsoft To Do (by Andrew Rathbun): Microsoft To Do - SQLite Database of To Do tasks, Microsoft To Do - User Avatar"
    type: bool
  - name: MidnightCommander
    description: "Midnight Commander (by Andrew Rathbun): Midnight Commander -- All Configuation Files"
    type: bool
  - name: MiniTimelineCollection
    description: "MFT, Registry and Event Logs to generate a mini timeline (by Mari DeGrazia): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T, Event logs Win7+, Event logs Win7+, Event logs XP, Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: MultiCommander
    description: "Multi Commander (by Andrew Rathbun): Multi Commander - Application Folder, Multi Commander - Config Folder, Multi Commander - Log File, Multi Commander - Log Folder, Multi Commander - UserData Folder"
    type: bool
  - name: NETCLRUsageLogs
    description: ".NET CLR UsageLogs (by Matias Davaro, Thomas DIOT (Qazeer)): .NET CLR UsageLogs (system-scoped), .NET CLR UsageLogs (user-scoped)"
    type: bool
  - name: NGINXLogs
    description: "NGINX Log Files (by Eric Capuano): NGINX Log Files"
    type: bool
  - name: NZBGet
    description: "NZBGet (by Andrew Rathbun): Usenet Clients - NZBGet Log File, Usenet Clients - NZBGet NZBs"
    type: bool
  - name: Nessus
    description: "Nessus (by Andrew Rathbun): Nessus Logs, Nessus Logs"
    type: bool
  - name: NetMonitorforEmployeesProfessional
    description: "Net Monitor for Employees Pro (by Tristan PINCEAUX - CERT CWATCH - ALMOND): Net Monitor Client Config, Net Monitor Client Logs, Net Monitor Server Config, Net Monitor Server Data, Net Monitor Server Logs, Net Monitor Server Temp Folder"
    type: bool
  - name: NewsbinPro
    description: "Newsbin Pro (by Andrew Rathbun): Usenet Clients - Newsbin Pro"
    type: bool
  - name: Newsleecher
    description: "Newsleecher (by Andrew Rathbun): Usenet Clients - Newsleecher"
    type: bool
  - name: Nicotine__
    description: "Nicotine++ (by Andrew Rathbun): Nicotine++ Buddyfileindex.db, Nicotine++ Buddyfiles.db, Nicotine++ Buddymtimes.db, Nicotine++ Buddystreams.db, Nicotine++ Buddywordindex.db, Nicotine++ Config Files, Nicotine++ Downloads.json, Nicotine++ Incomplete Downloads, Nicotine++ Logs, Nicotine++ Uploads.json, Nicotine++ User Shares"
    type: bool
  - name: Notepad__
    description: "Notepad++ Backups, recently searched/replaced terms and recently opened documents (by Banaanhangwagen and Matt Dawson): Notepad++ Config, Notepad++ Session, Notepad++ Unsaved Edits"
    type: bool
  - name: Notepad
    description: "A Target to collect files that are currently open in Notepad (Windows 11+) (by Andrew Rathbun): Notepad Session Files"
    type: bool
  - name: Notion
    description: "Notion Note-Taking App (by Thomas Burnette): Notion Custom Dictionary, Notion Local Storage"
    type: bool
  - name: OfficeAutosave
    description: "Office Autosave (by Russ Taylor): Excel Autosave Location, Powerpoint Autosave Location, Publisher Autosave Location, Word Autosave Location"
    type: bool
  - name: OfficeDiagnostics
    description: "Office Diagnostics (by teddy-ROxPin): Office Diagnostics, Office Elevated Diagnostics"
    type: bool
  - name: OfficeDocumentCache
    description: "Office Document Cache (by Banaanhangwagen): Office Document Cache"
    type: bool
  - name: OneCommander
    description: "One Commander (by Andrew Rathbun): One Commander - All Configuration Files, One Commander - Other Configuration Files"
    type: bool
  - name: OneDrive_Metadata
    description: "Microsoft OneDrive Storage Metadata (by Chad Tilbury): OneDrive Metadata Logs, OneDrive Metadata Settings"
    type: bool
  - name: OneDrive_UserFiles
    description: "Microsoft OneDrive Storage Files (by Chad Tilbury): OneDrive User Files"
    type: bool
  - name: OpenSSHClient
    description: "OpenSSH Client config, known hosts and keys (by Matt Dawson): OpenSSH Config File, OpenSSH Default DSA Private Key, OpenSSH Default ECDSA Private Key, OpenSSH Default ECDSA-SK Private Key, OpenSSH Default ED25519 Private Key, OpenSSH Default ED25519-SK Private Key, OpenSSH Default RSA Private Key, OpenSSH Known Hosts, OpenSSH Public Keys"
    type: bool
  - name: OpenSSHServer
    description: "OpenSSH Server Config and Logs (by Matt Dawson): OpenSSH Authorized Administrator Keys, OpenSSH Host DSA Key, OpenSSH Host ECDSA Key, OpenSSH Host ED25519 Key, OpenSSH Host RSA Key, OpenSSH Server Config File, OpenSSH Server Logs, OpenSSH User Authorized Keys, OpenSSH User Authorized Keys 2"
    type: bool
  - name: OpenVPNClient
    description: "OpenVPN Client Config and Log (by Mathias Frank): OpenVPN Client Config, OpenVPN Client Config, OpenVPN Client Config"
    type: bool
  - name: Opera
    description: "Opera (by Andrew Rathbun): Opera - Local Folder, Opera - Roaming Folder"
    type: bool
  - name: OutlookPSTOST
    description: "Outlook PST and OST files (by Eric Zimmerman and Chad Tilbury): NST, OST, OST (2013 or 2016), OST XP, Outlook Attachment Temporary Storage, PST, PST (2013 or 2016), PST XP"
    type: bool
  - name: P2PClients
    description: "P2P Clients (by Andrew Rathbun): DC++ Chat Logs, FrostWire AppData, FrostWire AppData, FrostWire Downloads, Gigatribe Files Windows Vista/7/8/10, Gigatribe Files Windows XP, Gigatribe Files Windows XP, Shareaza Logs, Soulseek Chat Logs, Soulseek Search History/Shared Folders/Settings"
    type: bool
  - name: PeaZip
    description: "PeaZip (by Andrew Rathbun): PeaZip Configuration Files"
    type: bool
  - name: PerfLogs
    description: "Perflogs Folder Copy (by Vito Alfano): Perflogs"
    type: bool
  - name: PowerShell7Config
    description: "PowerShell 7 Runtime Config (by Andrew Rathbun): PowerShell 7 Config JSON"
    type: bool
  - name: PowerShellConsole
    description: "PowerShell Console Log File (by Mike Cary): PowerShell Console Log"
    type: bool
  - name: PowerShellTranscripts
    description: "PowerShell Transcripts (by Andrew Rathbun and Chad Tilbury): PowerShell Transcripts - Default Location, PowerShell Transcripts - Observed Location, PowerShell Transcripts - Observed Location, PowerShell Transcripts - Observed Location"
    type: bool
  - name: Prefetch
    description: "Prefetch files (by Eric Zimmerman): Prefetch, Prefetch"
    type: bool
  - name: ProgramData
    description: "ProgramData Folder Copy (by Vito Alfano): ProgramData"
    type: bool
  - name: ProtonVPN
    description: "ProtonVPN (by Andrew Rathbun): ProtonVPN - Connection Logs"
    type: bool
  - name: PuffinSecureBrowser
    description: "Puffin Secure Browser (by Andrew Rathbun): Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db"
    type: bool
  - name: PushNotification
    description: "Windows Push Notification Service (by Zawadi Done): WNS, WNS"
    type: bool
  - name: Q_Dir
    description: "Q-Dir (by Andrew Rathbun): Q-Dir - .ini File, Q-Dir - .qdr file"
    type: bool
  - name: QFinderPro__QNAP_
    description: "QFinderPro (QNAP) (by Andrew Rathbun): QFinderPro"
    type: bool
  - name: RDPCache
    description: "RDP Cache Files (by Hadar Yudovich): RDP Cache Files, RDP Cache Files, Windows.old RDP Cache Files"
    type: bool
  - name: RDPLogs
    description: "RDP Logs (by Drew Ervin): LocalSessionManager Event Logs, LocalSessionManager Event Logs, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs"
    type: bool
  - name: Radmin
    description: "Radmin Server/Viewer Logs and Chats (by Mathias Frank): Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats"
    type: bool
  - name: RcloneConf
    description: "Rclone config file (by Eric Capuano): Rclone Config"
    type: bool
  - name: RecentFileCache
    description: "RecentFileCache (by Eric Zimmerman): RecentFileCache, RecentFileCache"
    type: bool
  - name: RecycleBin
    description: "Recycle Bin DataAndInfo (by Mark Hallman / Joshua Hickman): RECYCLER - WinXP, RECYCLER - WinXP, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+"
    type: bool
  - name: RecycleBin_DataFiles
    description: "Recycle Bin Data Files (by Joshua Hickman, Andreas Hunkeler (@Karneades), Brian Maloney): RECYCLER - WinXP, Recycle Bin - Windows Vista+, Recycle Bin - Windows Vista+"
    type: bool
  - name: RecycleBin_InfoFiles
    description: "Recycle Bin Info Files (by Joshua Hickman, Andreas Hunkeler (@Karneades)): RECYCLER - WinXP, Recycle Bin - Windows Vista+"
    type: bool
  - name: RegistryHives
    description: "System and user related Registry hives (by Eric Zimmerman): Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: RegistryHivesMSIXApps
    description: "MSIX/APPX App Hives (by Zach Stanford / Mari DeGrazia): Registry.dat MSIX Hive, User.dat MSIX Hive, UserClasses.dat MSIX Hive"
    type: bool
  - name: RegistryHivesOther
    description: "Other Registry Hives (by Andrew Rathbun): BBI registry hive, BBI registry hive, BBI registry transaction files, BBI registry transaction files, BCD-Template registry hive, BCD-Template registry hive, BCD-Template registry transaction files, BCD-Template registry transaction files, COMPONENTS registry hive, COMPONENTS registry hive, COMPONENTS registry transaction files, COMPONENTS registry transaction files, DRIVERS registry hive, DRIVERS registry hive, DRIVERS registry transaction files, DRIVERS registry transaction files, ELAM registry hive, ELAM registry hive, ELAM registry transaction files, ELAM registry transaction files, VSMIDK registry hive, VSMIDK registry hive, VSMIDK registry transaction files, VSMIDK registry transaction files, userdiff registry hive, userdiff registry hive, userdiff registry transaction files, userdiff registry transaction files"
    type: bool
  - name: RegistryHivesSystem
    description: "System level/related Registry hives (by Eric Zimmerman / Mark Hallman): Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP)"
    type: bool
  - name: RegistryHivesUser
    description: "User Related Registry hives (by Eric Zimmerman / Mark Hallman): NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: RemoteAdmin
    description: "Composite target for files related to remote administration tools (by Drew Ervin, Mathias Frank, Andrew Rathbun): Action1 Client Application logs, Ammyy Program Data, AnyDesk Chat Logs - User Profile, AnyDesk Logs - ProgramData - *.conf, AnyDesk Logs - ProgramData - *.trace, AnyDesk Logs - ProgramData - connection_trace.txt, AnyDesk Logs - System User Account, AnyDesk Logs - User Profile - *.conf, AnyDesk Logs - User Profile - *.trace, AnyDesk Logs - User Profile - connection_trace.txt, AnyDesk Videos, Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, DWAgent Log Files, ISL AlwaysOn - App Logs, ISL AlwaysOn - Configuration, ISL AlwaysOn - Email Configuration, ISL AlwaysOn Logs - Sessions, ISL AlwaysOn Logs - Sessions List, ISL Light Logs - Sessions, ISLOnline Logs - Session Configurations, ISLOnline Logs - Sessions - *.out, Kaseya Agent Edge Service Logs, Kaseya Agent Endpoint Service Logs, Kaseya Agent Endpoint Service Logs (XP), Kaseya Agent Service Log, Kaseya Live Connect Logs, Kaseya Live Connect Logs (XP), Kaseya Setup Log, Kaseya Setup Log, Kaseya Setup Log, Level RMM Client Application logs, LocalSessionManager Event Logs, LocalSessionManager Event Logs, LogMeIn Application Logs, LogMeIn ProgramData Logs, Net Monitor Client Config, Net Monitor Client Logs, Net Monitor Server Config, Net Monitor Server Data, Net Monitor Server Logs, Net Monitor Server Temp Folder, RDP Cache Files, RDP Cache Files, RDPClient Event Logs, RDPClient Event Logs, RDPCoreTS Event Logs, RDPCoreTS Event Logs, Radmin Server 32bit Chats, Radmin Server 32bit Log, Radmin Server 64bit Chats, Radmin Server 64bit Log, Radmin Viewer Chats, RealVNC Log, RealVNC Log, RemoteConnectionManager Event Logs, RemoteConnectionManager Event Logs, RemoteUtilities Connection Logs, RemoteUtilities Install Log, RustDesk logs, RustDesk logs, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config, Splashtop Log Files, Splashtop Log Files in ProgramData, Supremo Connection Logs, Supremo File Transfer Inbox, TeamViewer Application Logs, TeamViewer Application User Logs, TeamViewer Configuration Files, TeamViewer Connection Logs, TightVNC Application Logs, UltraViewer Connection Log, UltraViewer Service Log, UltraViewer System Logs, UltraViewer User Logs, Windows.old RDP Cache Files, Xeox RMM Client Application logs, Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData, mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings"
    type: bool
  - name: RemoteUtilities_app
    description: "Remote Utilities (by Ryan McVicar): RemoteUtilities Connection Logs, RemoteUtilities Install Log"
    type: bool
  - name: RoamingProfile
    description: "User Related Registry Hives, LNK files, etc (by Scott Downie): Amcache, Amcache transaction files, Chrome Cookies, Chrome Cookies, Chrome Current Session, Chrome Current Session, Chrome Current Tabs, Chrome Current Tabs, Chrome Download Metadata, Chrome Download Metadata, Chrome Extension Cookies, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons, Chrome History, Chrome History, Chrome Last Session, Chrome Last Session, Chrome Last Tabs, Chrome Last Tabs, Chrome Login Data, Chrome Login Data, Chrome Media History, Chrome Media History, Chrome Network Action Predictor, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences, Chrome Quota Manager, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts, Chrome SyncData Database, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites, Chrome Trust Tokens, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links, Chrome Web Data, Chrome Web Data, Chrome bookmarks, Chrome bookmarks, Desktop LNK Files, Edge folder, Edge folder, Excel Autosave Location, LNK Files, LNK Files from Microsoft Office Recent, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry transaction files, Office Document Cache, Office Document Cache, PowerPoint Autosave Location, Publisher Autosave Location, Publisher Autosave Location, UsrClass.dat registry hive, UsrClass.dat registry transaction files, Windows Protect Folder, Windows Protect Folder, Word Autosave Location"
    type: bool
  - name: Robo_FTP
    description: "Robo-FTP (by Thomas Burnette): Robo-FTP Debug Logs, Robo-FTP Jobs, Robo-FTP PGP Keys, Robo-FTP SSH Keys, Robo-FTP SSL Certificates, Robo-FTP Script/Trace Logs, Robo-FTP User Debug Logs, Robo-FTP User PGP Keys, Robo-FTP User SSH Keys, Robo-FTP User SSL Certificates, Robo-FTP User Script/Trace Logs, Robo-FTP User Scripts, Robo-FTP User XML Config, Robo-FTP XML Config"
    type: bool
  - name: RogueKiller
    description: "RogueKiller Anti-Malware (by Adlice Software) (by Drew Ervin): RogueKiller Reports"
    type: bool
  - name: RustDesk
    description: "RustDesk (by Andrew Rathbun): RustDesk logs, RustDesk logs"
    type: bool
  - name: SABnbzd
    description: "SABnbzd (by Andrew Rathbun): Usenet Clients - SABnzbd Download Logs, Usenet Clients - SABnzbd History.db"
    type: bool
  - name: SCCMClientLogs
    description: "SCCM Client Log Files (by Andrew Rathbun): SCCM Client Log Files"
    type: bool
  - name: SDB
    description: "Shim SDB FIles (by Troy Larson): SDB Files, SDB Files, SDB Files x64, SDB Files x64"
    type: bool
  - name: SOFELK
    description: "SOF-ELK related files of interest (by Tony Knutson and Andrew Rathbun): $Boot, $J, $J, $LogFile, $MFT, $Max, $Max, $SDS, $SDS, $T, $T, Amcache, Amcache, Amcache transaction files, Amcache transaction files, AppCompat PCA Folder, Desktop LNK Files, Desktop LNK Files XP, Event logs Win7+, Event logs Win7+, Event logs XP, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Prefetch, Prefetch, RecentFileCache, RecentFileCache, Restore point LNK Files XP, Start Menu LNK Files, Syscache, Syscache transaction files"
    type: bool
  - name: SQLiteDatabases
    description: "SQLDatabases Target for use with SQLECmd Module (by Andrew Rathbun): 4K Video Downloader, ActivitiesCache.db, Addons, Bitdefender SQLite DB Files, Bookmarks, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Shortcuts, Chrome Shortcuts XP, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Cookies, Cookies, Downloads, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Dropbox Metadata, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Shortcuts, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge bookmarks, EventTranscript.db, EventTranscript.db, Favicons, FileZilla SQLite3 Log Files, Form history, Google File Stream Metadata, Google File Stream Metadata, Google File Stream Metadata, Google File Stream Metadata, IDrive Backed Up Files, Microsoft OneNote - AccessibilityCheckerIndex, Microsoft OneNote - FullTextSearchIndex, Microsoft OneNote - RecentNotebooks_SeenURLs, Microsoft OneNote - RecentSearches, Microsoft OneNote - User NoteTags, Microsoft Sticky Notes - 1607 and later, Microsoft To Do - SQLite Database of To Do tasks, Notion Local Storage, Permissions, Places, Protections, Robo-FTP Jobs, Search, Signons, Storage Sync, TeraCopy - History Databases, TeraCopy - Main Database, Update Store.db, Webappstore, Windows 10 Notification DB, Windows 10 Notification DB"
    type: bool
  - name: SRUM
    description: "System Resource Usage Monitor (SRUM) Data (by Mark Hallman): SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry transaction files, SOFTWARE registry transaction files, SRUM, SRUM"
    type: bool
  - name: SUM
    description: "SUM Database (by Andrew Rathbun): SUM Database (.mdb files)"
    type: bool
  - name: SUPERAntiSpyware
    description: "SUPERAntiSpyware Data (by Drew Ervin): SUPERAntiSpyware Logs"
    type: bool
  - name: SUSELinuxEnterpriseServer
    description: "SUSE Linux Enterprise Server on Windows Subsystem for Linux (by Matt Dawson): SUSE Linux Enterprise Server WSL .bash_history, SUSE Linux Enterprise Server WSL .bashrc, SUSE Linux Enterprise Server WSL .profile, SUSE Linux Enterprise Server WSL /etc/bash.bashrc, SUSE Linux Enterprise Server WSL /etc/fstab, SUSE Linux Enterprise Server WSL /etc/group, SUSE Linux Enterprise Server WSL /etc/hostname, SUSE Linux Enterprise Server WSL /etc/hosts, SUSE Linux Enterprise Server WSL /etc/os-release, SUSE Linux Enterprise Server WSL /etc/passwd, SUSE Linux Enterprise Server WSL /etc/profile, SUSE Linux Enterprise Server WSL /etc/shadow, SUSE Linux Enterprise Server WSL /etc/timezone, SUSE Linux Enterprise Server WSL ext4.vhdx"
    type: bool
  - name: ScheduledTasks
    description: "Scheduled tasks (*.job and XML) (by Eric Zimmerman): XML, XML, XML, at .job, at .job, at SchedLgU.txt, at SchedLgU.txt"
    type: bool
  - name: ScreenConnect
    description: "ScreenConnect Data (now known as ConnectWise Control) (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, ScreenConnect Session Database, ScreenConnect Session Database, ScreenConnect User Config"
    type: bool
  - name: SecureAge
    description: "SecureAge Antivirus Logs (by Andrew Rathbun): SecureAge Antvirus Logs"
    type: bool
  - name: SentinelOne
    description: "Sentinel One Logs (by Kirtan Shah): SentinelOne EDR Log"
    type: bool
  - name: ServerTriage
    description: "A compound target for gathering artifacts common to servers. (by Eric Capuano): Apache Access Log, Confluence Wiki Log Files, Confluence Wiki Log Files, Exchange TransportRoles log files, Exchange client access log files, FileZilla Log Files, FileZilla Server XML Log Files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, MS SQL Errorlog, MS SQL Errorlogs, ManageEngine ADSelfService Plus Log Files, ManageEngine Desktop Central Log Files, NGINX Log Files, OpenSSH Authorized Administrator Keys, OpenSSH Host DSA Key, OpenSSH Host ECDSA Key, OpenSSH Host ED25519 Key, OpenSSH Host RSA Key, OpenSSH Server Config File, OpenSSH Server Logs, OpenSSH User Authorized Keys, OpenSSH User Authorized Keys 2"
    type: bool
  - name: ShareX
    description: "ShareX (by Andrew Rathbun): ShareX"
    type: bool
  - name: Shareaza
    description: "Shareaza (by Andrew Rathbun): Shareaza Logs"
    type: bool
  - name: SiemensTIA
    description: "Copy Siemens TIA Settings (by Olaf Schwarz (@b00010111)): Siemens TIA Settings"
    type: bool
  - name: Signal
    description: "Signal (Please view this tkape file for documentation on decryption!) (by Matt Dawson): Signal Attachments cache, Signal Database, Signal Logs, Signal config.json"
    type: bool
  - name: SignatureCatalog
    description: "Obtain detached signature catalog files (by Mike Pilkington): SignatureCatalog, SignatureCatalog"
    type: bool
  - name: Skype
    description: "Skype (by Eric Zimmerman, Matt Dawson): Skype for Destkop v8+ Chromium Cache, leveldb (Skype for Desktop +v8), main.db (App &lt;v12), main.db Win7+, main.db XP, s4l-[username].db (App +v8), skype.db (App +v12)"
    type: bool
  - name: Slack
    description: "Slack (by Andrew Rathbun and Chad Tilbury): Slack - Chat Logs, Slack Cache, Slack Electron Logs, Slack LevelDB Files, Slack Storage"
    type: bool
  - name: Snagit
    description: "Snagit (by Andrew Rathbun): Snagit - Captures"
    type: bool
  - name: SnipAndSketch
    description: "Snip &amp; Sketch Cached Images (by Kevin Pagano): Snip &amp; Sketch"
    type: bool
  - name: Sophos
    description: "Sophos Data (by Drew Ervin): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Sophos Logs, Sophos Logs (XP)"
    type: bool
  - name: Soulseek
    description: "Soulseek (by Andrew Rathbun): Soulseek Chat Logs, Soulseek Search History/Shared Folders/Settings"
    type: bool
  - name: SpeedCommander
    description: "SpeedCommander (by Andrew Rathbun): SpeedCommander - .ini File"
    type: bool
  - name: Splashtop
    description: "Splashtop (by Andrew Rathbun, Yogesh Khatri): Splashtop Log Files, Splashtop Log Files in ProgramData"
    type: bool
  - name: StartupFolders
    description: "Startup Folders (by Jason Ballard): System-wide startup folder, User startup folders"
    type: bool
  - name: StartupInfo
    description: "StartupInfo XML Files (by Hadar Yudovich): StartupInfo XML Files, StartupInfo XML Files"
    type: bool
  - name: Steam
    description: "Steam (by Nisarg Suthar, SolitudePy): Steam Friend List and Username History file, Steam Friend List and Username History file, Steam Game Image files, Steam Game Image files, Steam Game Tray Icon files, Steam Game Tray Icon files, Steam Login Metadata file, Steam Login Metadata file, Steam Startup Times Log file, Steam Startup Times Log file, Steam User Avatar files, Steam User Avatar files"
    type: bool
  - name: SublimeText
    description: "Sublime Text 2/3/4 Auto Save Session (by Mathias Frank and Nisarg Suthar): SublimeText 2/3 Auto Save Session, SublimeText 4 Auto Save Session"
    type: bool
  - name: SugarSync
    description: "SugarSync (by Andrew Rathbun): SugarSync - My SugarSync (Default Location), SugarSync - Shared Folders (Default Location), SugarSync Log File"
    type: bool
  - name: SumatraPDF
    description: "SumatraPDF (by Andrew Rathbun): SumatraPDF Cache, SumatraPDF Settings - SessionData"
    type: bool
  - name: SupremoRemoteDesktop
    description: "Supremo Remote Desktop Control Logs (by Sandro Heckendorn): Supremo Connection Logs, Supremo File Transfer Inbox"
    type: bool
  - name: Symantec_AV_Logs
    description: "Symantec AV Logs (by Brian Maloney): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, Symantec Endpoint Protection Logs, Symantec Endpoint Protection Logs (XP), Symantec Endpoint Protection Quarantine, Symantec Endpoint Protection Quarantine (XP), Symantec Endpoint Protection User Logs, Symantec Event Log Win7+, Symantec Event Log Win7+, ccSubSDK Database, registrationInfo.xml"
    type: bool
  - name: Syscache
    description: "syscache.hve (by Phill Moore): Syscache, Syscache transaction files"
    type: bool
  - name: TablacusExplorer
    description: "Tablacus Explorer (by Andrew Rathbun): Tablacus Explorer - remember.xml, Tablacus Explorer - window.xml, Tablacus Explorer - window1.xml"
    type: bool
  - name: TeamViewerLogs
    description: "TeamViewer Logs (by Hadar Yudovich, Sam Smoker): TeamViewer Application Logs, TeamViewer Application User Logs, TeamViewer Configuration Files, TeamViewer Connection Logs"
    type: bool
  - name: Telegram
    description: "Telegram Desktop (by Simone Marinari): Telegram app folder, Telegram downloaded files"
    type: bool
  - name: TeraCopy
    description: "TeraCopy log history (by Kevin Pagano): TeraCopy"
    type: bool
  - name: ThumbCache
    description: "Thumbcache DB (by Eric Zimmerman): Thumbcache DB"
    type: bool
  - name: Thunderbird
    description: "Mozilla Thunderbird Email Client (by Matt Dawson): Mozilla Thunderbird Address Book, Mozilla Thunderbird Attachments, Mozilla Thunderbird Calendar Data, Mozilla Thunderbird Global Messages Database, Mozilla Thunderbird ImapMail INBOX, Mozilla Thunderbird Install Date, Mozilla Thunderbird Mail INBOX, Mozilla Thunderbird Profiles.ini, Mozilla Thunderbird logins.json, Mozilla Thunderbird places.sqlite, Mozilla Thunderbird prefs.js"
    type: bool
  - name: TorrentClients
    description: "Torrent Clients (by Andrew Rathbun): TorrentClients - BitTorrent, TorrentClients - qBittorrent, TorrentClients - qBittorrent, TorrentClients - qBittorrent, TorrentClients - qBittorrent, TorrentClients - uTorrent"
    type: bool
  - name: Torrents
    description: "Torrent Files (by Tony Knutson): Torrents"
    type: bool
  - name: TotalAV
    description: "TotalAV Antivirus Data (by Kirtan Shah): TotalAV Logs, TotalAV Logs"
    type: bool
  - name: TotalCommander
    description: "Total Commander (by Andrew Rathbun, Jessica Venturo and Chuck Whitson): Total Commander - .ini File, Total Commander - FTP .ini File, Total Commander - FTP Logs, Total Commander - File Tree, Total Commander - Frequent Directory Listing, Total Commander - Log File, Total Commander - Temp Files Created During Folder Traversal"
    type: bool
  - name: TreeSize
    description: "TreeSize - Scan History (by Andrew Rathbun): TreeSize - ScanHistory.XML"
    type: bool
  - name: TrendMicro
    description: "Trend Micro Data (by Drew Ervin): Trend Micro Logs, Trend Micro Security Agent Connection Logs, Trend Micro Security Agent Report Logs"
    type: bool
  - name: USBDetective
    description: "Collects files that can be input into USB Detective for parsing (by Kevin Pagano): Amcache, Amcache, Amcache transaction files, Amcache transaction files, Desktop LNK Files, Desktop LNK Files XP, Event logs Win7+, Event logs Win7+, Event logs XP, LNK Files from C:\ProgramData, LNK Files from Microsoft Office Recent, LNK Files from Recent, LNK Files from Recent (XP), Local Service registry hive, Local Service registry hive, Local Service registry transaction files, Local Service registry transaction files, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT registry hive, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT DEFAULT transaction files, NTUSER.DAT registry hive, NTUSER.DAT registry hive XP, NTUSER.DAT registry transaction files, Network Service registry hive, Network Service registry hive, Network Service registry transaction files, Network Service registry transaction files, RegBack registry transaction files, RegBack registry transaction files, Registry.dat MSIX Hive, Restore point LNK Files XP, SAM registry hive, SAM registry hive, SAM registry hive (RegBack), SAM registry hive (RegBack), SAM registry transaction files, SAM registry transaction files, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files, Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP, Start Menu LNK Files, System Profile registry hive, System Profile registry hive, System Profile registry transaction files, System Profile registry transaction files, System Restore Points Registry Hives (XP), User.dat MSIX Hive, UserClasses.dat MSIX Hive, UsrClass.dat registry hive, UsrClass.dat registry transaction files"
    type: bool
  - name: USBDevicesLogs
    description: "USB devices log files (by Eric Zimmerman, esecrpm): Setupapi.log Win7+, Setupapi.log Win7+, Setupapi.log XP"
    type: bool
  - name: Ubuntu
    description: "Ubuntu on Windows Subsystem for Linux (by Matt Dawson): Ubuntu WSL .bash_history, Ubuntu WSL .bashrc, Ubuntu WSL .profile, Ubuntu WSL /etc/bash.bashrc, Ubuntu WSL /etc/crontab, Ubuntu WSL /etc/fstab, Ubuntu WSL /etc/group, Ubuntu WSL /etc/hostname, Ubuntu WSL /etc/hosts, Ubuntu WSL /etc/os-release, Ubuntu WSL /etc/passwd, Ubuntu WSL /etc/profile, Ubuntu WSL /etc/shadow, Ubuntu WSL /etc/timezone, Ubuntu WSL Apt Logs, Ubuntu WSL User Crontabs, Ubuntu WSL ext4.vhdx"
    type: bool
  - name: Ultraviewer
    description: "UltraViewer (by Ryan McVicar, Sam Smoker): UltraViewer Connection Log, UltraViewer Service Log, UltraViewer System Logs, UltraViewer User Logs"
    type: bool
  - name: Usenet
    description: "Usenet (NZB) Files (by Andrew Rathbun): Usenet (NZB) Files"
    type: bool
  - name: UsenetClients
    description: "Usenet Clients (by Andrew Rathbun): Usenet Clients - NZBGet Log File, Usenet Clients - NZBGet NZBs, Usenet Clients - Newsbin Pro, Usenet Clients - Newsleecher, Usenet Clients - SABnzbd Download Logs, Usenet Clients - SABnzbd History.db"
    type: bool
  - name: VIPRE
    description: "VIPRE Data (by Drew Ervin): VIPRE Business Agent Logs, VIPRE Business User Logs (up to v4), VIPRE Business User Logs (v5-v6), VIPRE Business User Logs (v7+)"
    type: bool
  - name: VLC_Media_Player
    description: "VLC Media Player (by Matt Dawson): VLC Recently Opened Files, VLC Recorded Files"
    type: bool
  - name: VMware
    description: "Runs all VMware modules to collect VMware VM config files, logs and Virtual Hard Disks (by Matt Dawson): VDI, VHD, VHDX, VMDK, VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player), VMware - Virtual Machine Inventory"
    type: bool
  - name: VMwareInventory
    description: "VMware - Virtual Machine Inventory (by Andrew Rathbun): VMware - Virtual Machine Inventory"
    type: bool
  - name: VMwareMemory
    description: "VMware - Virtual Machine Memory (by Andrew Rathbun): VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player), VMware (Fusion/Workstation/Server/Player)"
    type: bool
  - name: VNCLogs
    description: "VNC Logs (by Phill Moore): Application Event Log Win7+, Application Event Log Win7+, Application Event Log XP, Application Event Log XP, RealVNC Log, RealVNC Log, TightVNC Application Logs"
    type: bool
  - name: Viber
    description: "ViberPC Messaging App (by Matt Dawson): Viber Config Database, Viber Users Avatars Cache, Viber Users Backgrounds Cache, Viber Users Data Database, Viber Users Thumbnails Cache"
    type: bool
  - name: VirtualBox
    description: "Runs all VirtualBox modules to collect Virtualbox VM config files, logs and Virtual Hard Disks (by Matt Dawson): VDI, VHD, VHDX, VMDK, VirtualBox, VirtualBox Backup Logs, VirtualBox Hardening Logs, VirtualBox Logs, VirtualBox VM backup configs, VirtualBox VM configs"
    type: bool
  - name: VirtualBoxConfig
    description: "Collects VirtualBox configuration files (by Matt Dawson): VirtualBox VM backup configs, VirtualBox VM configs"
    type: bool
  - name: VirtualBoxLogs
    description: "Collects VirtualBox log files (by Matt Dawson): VirtualBox Backup Logs, VirtualBox Hardening Logs, VirtualBox Logs"
    type: bool
  - name: VirtualBoxMemory
    description: "VirtualBox - Memory (by Andrew Rathbun): VirtualBox"
    type: bool
  - name: VirtualDisks
    description: "Virtual Disks (by Phill Moore): VDI, VHD, VHDX, VMDK"
    type: bool
  - name: VisualStudioCode
    description: "Visual Studio Code artifacts (by Sebastian Søgaard): VSCode Logs, VSCode Network Cookies, VSCode Network Persistent State, VSCode Opened Files, VSCode User Preferences, VSCode User extensions, VSCode User settings, VSCode Workspaces"
    type: bool
  - name: Vivaldi
    description: "Vivaldi Artifacts (by Sebastian Søgaard): Vivaldi Bookmarks, Vivaldi Calendar, Vivaldi Contacts, Vivaldi Cookies, Vivaldi Download Metadata, Vivaldi Favicons, Vivaldi History, Vivaldi Login Data, Vivaldi Network Action Predictor, Vivaldi Network Persistent State, Vivaldi Notes, Vivaldi Preferences, Vivaldi Sessions Folder, Vivaldi Top Sites, Vivaldi User Tracking, Vivaldi Visited Links, Vivaldi Web Data"
    type: bool
  - name: WBEM
    description: "Web-Based Enterprise Management (WBEM) (by Mark Hallman): WBEM, WBEM"
    type: bool
  - name: WER
    description: "Windows Error Reporting (by Troy Larson): Crash Dumps, Crash Dumps, Crash Dumps, WER Files, WER Files"
    type: bool
  - name: WSL
    description: "All Windows Subsystem for Linux targets (by Matt Dawson): Debian WSL .bash_history, Debian WSL .bashrc, Debian WSL .profile, Debian WSL /etc/bash.bashrc, Debian WSL /etc/crontab, Debian WSL /etc/debian_version, Debian WSL /etc/fstab, Debian WSL /etc/group, Debian WSL /etc/hostname, Debian WSL /etc/hosts, Debian WSL /etc/os-release, Debian WSL /etc/passwd, Debian WSL /etc/profile, Debian WSL /etc/shadow, Debian WSL /etc/timezone, Debian WSL Apt Logs, Debian WSL User Crontabs, Debian WSL ext4.vhdx, Kali WSL .bash_history, Kali WSL .bashrc, Kali WSL .profile, Kali WSL /etc/bash.bashrc, Kali WSL /etc/crontab, Kali WSL /etc/debian_version, Kali WSL /etc/fstab, Kali WSL /etc/group, Kali WSL /etc/hostname, Kali WSL /etc/hosts, Kali WSL /etc/os-release, Kali WSL /etc/passwd, Kali WSL /etc/profile, Kali WSL /etc/shadow, Kali WSL /etc/timezone, Kali WSL Apt Logs, Kali WSL User Crontabs, Kali WSL ext4.vhdx, SUSE Linux Enterprise Server WSL .bash_history, SUSE Linux Enterprise Server WSL .bashrc, SUSE Linux Enterprise Server WSL .profile, SUSE Linux Enterprise Server WSL /etc/bash.bashrc, SUSE Linux Enterprise Server WSL /etc/fstab, SUSE Linux Enterprise Server WSL /etc/group, SUSE Linux Enterprise Server WSL /etc/hostname, SUSE Linux Enterprise Server WSL /etc/hosts, SUSE Linux Enterprise Server WSL /etc/os-release, SUSE Linux Enterprise Server WSL /etc/passwd, SUSE Linux Enterprise Server WSL /etc/profile, SUSE Linux Enterprise Server WSL /etc/shadow, SUSE Linux Enterprise Server WSL /etc/timezone, SUSE Linux Enterprise Server WSL ext4.vhdx, Ubuntu WSL .bash_history, Ubuntu WSL .bashrc, Ubuntu WSL .profile, Ubuntu WSL /etc/bash.bashrc, Ubuntu WSL /etc/crontab, Ubuntu WSL /etc/fstab, Ubuntu WSL /etc/group, Ubuntu WSL /etc/hostname, Ubuntu WSL /etc/hosts, Ubuntu WSL /etc/os-release, Ubuntu WSL /etc/passwd, Ubuntu WSL /etc/profile, Ubuntu WSL /etc/shadow, Ubuntu WSL /etc/timezone, Ubuntu WSL Apt Logs, Ubuntu WSL User Crontabs, Ubuntu WSL ext4.vhdx, openSUSE WSL .bash_history, openSUSE WSL .bashrc, openSUSE WSL .profile, openSUSE WSL /etc/bash.bashrc, openSUSE WSL /etc/fstab, openSUSE WSL /etc/group, openSUSE WSL /etc/hostname, openSUSE WSL /etc/hosts, openSUSE WSL /etc/os-release, openSUSE WSL /etc/passwd, openSUSE WSL /etc/profile, openSUSE WSL /etc/shadow, openSUSE WSL /etc/timezone, openSUSE WSL ext4.vhdx"
    type: bool
  - name: WebBrowsers
    description: "Web browser history, bookmarks, etc. (by Eric Zimmerman): Addons, Addons XP, Bookmarks, Bookmarks, Bookmarks, Chrome Cookies, Chrome Cookies XP, Chrome Current Session, Chrome Current Session XP, Chrome Current Tabs, Chrome Current Tabs XP, Chrome Download Metadata, Chrome Extension Cookies, Chrome Favicons, Chrome Favicons XP, Chrome History, Chrome History XP, Chrome Last Session, Chrome Last Session XP, Chrome Last Tabs, Chrome Last Tabs XP, Chrome Login Data, Chrome Login Data XP, Chrome Media History, Chrome Network Action Predictor, Chrome Network Persistent State, Chrome Preferences, Chrome Preferences XP, Chrome Quota Manager, Chrome Reporting and NEL, Chrome Sessions Folder, Chrome Shortcuts, Chrome Shortcuts XP, Chrome Snapshots Folder, Chrome SyncData Database, Chrome Top Sites, Chrome Top Sites XP, Chrome Trust Tokens, Chrome Visited Links, Chrome Visited Links XP, Chrome Web Data, Chrome Web Data XP, Chrome bookmarks, Chrome bookmarks XP, Cookies, Cookies, Cookies, Cookies XP, Current Session, Current Tabs, Download Metadata, Downloads, Downloads XP, Edge Bookmarks, Edge Collections, Edge Cookies, Edge Current Session, Edge Current Tabs, Edge Favicons, Edge History, Edge Last Session, Edge Last Tabs, Edge Login Data, Edge Media History, Edge Network Action Predictor, Edge Preferences, Edge Sessions Folder, Edge Shortcuts, Edge Snapshots Folder, Edge SyncData Database, Edge Top Sites, Edge Visited Links, Edge Web Data, Edge WebAssistDatabase, Edge bookmarks, Edge folder, Extensions, Favicons, Favicons, Favicons XP, Form history, Form history XP, History, IE 11 Cookies, IE 11 Metadata, IE 9/10 Cookies, IE 9/10 Download History, IE 9/10 History, Index.dat History, Index.dat History subdirectory, Index.dat Office, Index.dat Office XP, Index.dat UserData, Index.dat cookies, Local Internet Explorer folder, Login Data, Network Action Predictor, Network Persistent State, Opera - Local Folder, Opera - Roaming Folder, Password, Password, Password, Password XP, Password XP, Password XP, Permissions, Places, Places XP, Preferences, Preferences, Protections, Publisher Info DB/Brave Rewards, Puffin - Autocomplete Data, Puffin - Cookies, Puffin - Image Cache, Puffin - Password (Encrypted), Puffin - Password Forms Data, Puffin - Subscription Data, Puffin - data.db, Quota Manager, Reporting and NEL, Roaming Internet Explorer folder, Search, Search XP, Secure Preferences, Sessions Folder, Sessionstore, Sessionstore Folder, Sessionstore XP, Shortcuts, Signons, Signons XP, Storage Sync, Top Sites, Visited Links, Vivaldi Bookmarks, Vivaldi Calendar, Vivaldi Contacts, Vivaldi Cookies, Vivaldi Download Metadata, Vivaldi Favicons, Vivaldi History, Vivaldi Login Data, Vivaldi Network Action Predictor, Vivaldi Network Persistent State, Vivaldi Notes, Vivaldi Preferences, Vivaldi Sessions Folder, Vivaldi Top Sites, Vivaldi User Tracking, Vivaldi Visited Links, Vivaldi Web Data, Web Data, Webappstore, Webappstore XP, Windows Protect Folder, Windows Protect Folder, Yandex Autofill data, Yandex Bookmarks, Yandex Cookies, Yandex Favicons, Yandex History, Yandex Login Data, Yandex Network Action Predictor, Yandex Network Persistent State, Yandex Passman logs, Yandex Preferences, Yandex Sessions Folder, Yandex Shortcuts, Yandex Top Sites, Yandex Visited Links, Yandex Web Data"
    type: bool
  - name: WebServers
    description: "Logs from all known web server applications and supporting services (by Eric Capuano): Apache Access Log, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, IIS log files, MS SQL Errorlog, MS SQL Errorlogs, NGINX Log Files"
    type: bool
  - name: Webroot
    description: "Webroot Antivirus (by Drew Ervin): Webroot Program Data"
    type: bool
  - name: WhatsApp
    description: "WhatsApp Local Files (by Matt Dawson, SolitudePy): Microsoft Store WhatsApp Cache, Microsoft Store WhatsApp Local Storage, WhatsApp Cache, WhatsApp Local Storage"
    type: bool
  - name: WhatsApp_Media
    description: "WhatsApp Shared Media Files (by SolitudePy): Microsoft Store WhatsApp Desktop Profile Pictures, Microsoft Store WhatsApp Shared Media"
    type: bool
  - name: WinDefendDetectionHist
    description: "Windows Defender Threat DetectionHistory files (by Jordan Klepser): DetectionHistory"
    type: bool
  - name: WinSCP
    description: "WinSCP (by Andrew Rathbun): WinSCP (.ini file)"
    type: bool
  - name: WindowsDefender
    description: "Windows Defender Data (by Drew Ervin): DetectionHistory, Windows Defender Event Logs, Windows Defender Event Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Logs, Windows Defender Quarantine"
    type: bool
  - name: WindowsFirewall
    description: "Windows Firewall Logs (by Mike Cary): Windows Firewall Logs, Windows Firewall Logs"
    type: bool
  - name: WindowsHello
    description: "Windows Hello (by Kevin Pagano): Cryptokeys, Masterkey, NGC, SECURITY registry hive, SECURITY registry hive, SECURITY registry hive (RegBack), SECURITY registry hive (RegBack), SECURITY registry transaction files, SECURITY registry transaction files, SOFTWARE registry hive, SOFTWARE registry hive, SOFTWARE registry hive (RegBack), SOFTWARE registry hive (RegBack), SOFTWARE registry transaction files, SOFTWARE registry transaction files, SYSTEM registry hive, SYSTEM registry hive, SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry hive (RegBack), SYSTEM registry transaction files, SYSTEM registry transaction files"
    type: bool
  - name: WindowsIndexSearch
    description: "Windows Index Search (by Mark Hallman): GatherLogs, WindowsIndexSearch"
    type: bool
  - name: WindowsNetwork
    description: "Windows Networks settings (by Zawadi Done): Network setting files"
    type: bool
  - name: WindowsNotificationsDB
    description: "Windows 10 Notification DB (by Hadar Yudovich): Windows 10 Notification DB, Windows 10 Notification DB"
    type: bool
  - name: WindowsOSUpgradeArtifacts
    description: "Windows OS Upgrade Artifacts (by Andrew Rathbun): FolderMoveLog.txt, HumanReadable.xml, MigLog.xml, Setupact.log, Update Store.db"
    type: bool
  - name: WindowsPowerDiagnostics
    description: "Windows Power Diagnostics (by Andrew Rathbun): Windows Power Diagnostics"
    type: bool
  - name: WindowsServerDNSAndDHCP
    description: "Windows Server DNS and DHCP log files (by Zawadi Done): DHCP files, DNS Netlogon files, DNS files"
    type: bool
  - name: WindowsSubsystemforAndroid
    description: "Windows Subsystem for Android (WSA) (by Andrew Rathbun): App download artifacts (ICO), App download artifacts (PNG), Appcompatdb.json, Diagnostic Logs for WSA, userdata.vhdx"
    type: bool
  - name: WindowsTelemetryDiagnosticsLegacy
    description: "Legacy Windows Telemetry and Diagnostics files (*.rbs) (by Andrew Rathbun and Josh Mitchell): Legacy .rbs files relating to Windows Telemetry and Diagnostics, Legacy .rbs files relating to Windows Telemetry and Diagnostics"
    type: bool
  - name: WindowsTimeline
    description: "ActivitiesCache.db collector (by Lee Whitfield): ActivitiesCache.db"
    type: bool
  - name: WindowsUpdate
    description: "Windows Update Logs (by Rick van Dreunen): Windows Component-Based Servicing logs, Windows Update Session Orchestrator logs, Windows Update logs"
    type: bool
  - name: WindowsYourPhone
    description: "Windows Your Phone (by Andrew Rathbun): Windows Your Phone - All Databases"
    type: bool
  - name: XPRestorePoints
    description: "XP Restore Points - System Volume Information directory (by Phill Moore): System Volume Information"
    type: bool
  - name: XYplorer
    description: "XYplorer (by Andrew Rathbun): XYplorer - .dat files, XYplorer - .ini file, XYplorer - .ini file for each respective pane, XYplorer - AutoBackup folder"
    type: bool
  - name: Xeox
    description: "Xeox Application Logs (by Andrew Skatoff @DFIR_TNT): Xeox RMM Client Application logs"
    type: bool
  - name: Yandex
    description: "Yandex Artifacts (by Sebastian Søgaard): Yandex Autofill data, Yandex Bookmarks, Yandex Cookies, Yandex Favicons, Yandex History, Yandex Login Data, Yandex Network Action Predictor, Yandex Network Persistent State, Yandex Passman logs, Yandex Preferences, Yandex Sessions Folder, Yandex Shortcuts, Yandex Top Sites, Yandex Visited Links, Yandex Web Data"
    type: bool
  - name: ZohoAssist
    description: "Zoho Assist artifacts (by Andrew Rathbun): Zoho Assist .conf files, Zoho Assist .conf files in  Program Files*, Zoho Assist .conf files in AppData\Local, Zoho Assist .txt files in  Program Files*, Zoho Assist log files in AppData\Local, Zoho Assist log files in Program Files*, Zoho Assist log files in ProgramData"
    type: bool
  - name: Zoom
    description: "Zoom client artifacts (by Ryan McVicar): Zoom client logs, Zoom client logs (Windows XP), Zoom client recordings, Zoom plugin (Outlook)"
    type: bool
  - name: iTunesBackup
    description: "iTunes Backups (by Tony Knutson): iTunes Backup Folder, iTunes Backup Folder, iTunes Backup Folder - iOS13"
    type: bool
  - name: mIRC
    description: "mIRC (by Andrew Rathbun): mIRC Chat Logs (2000/XP), mIRC Chat Logs (Vista+)"
    type: bool
  - name: mRemoteNG
    description: "mRemoteNG (by Markus Einarsson (@einarssonm)): mRemoteNG Connection Configuration and Backups, mRemoteNG Logs, mRemoteNG Program Settings"
    type: bool
  - name: openSUSE
    description: "openSUSE on Windows Subsystem for Linux (by Matt Dawson): openSUSE WSL .bash_history, openSUSE WSL .bashrc, openSUSE WSL .profile, openSUSE WSL /etc/bash.bashrc, openSUSE WSL /etc/fstab, openSUSE WSL /etc/group, openSUSE WSL /etc/hostname, openSUSE WSL /etc/hosts, openSUSE WSL /etc/os-release, openSUSE WSL /etc/passwd, openSUSE WSL /etc/profile, openSUSE WSL /etc/shadow, openSUSE WSL /etc/timezone, openSUSE WSL ext4.vhdx"
    type: bool
  - name: pCloudDatabase
    description: "pCloud Database (by Josh Hickman): pCloud Database, pCloud Database Shared Memory File, pCloud Database WAL File"
    type: bool
  - name: qBittorrent
    description: "qBittorrent (by Banaanhangwagen): TorrentClients - qBittorrent, TorrentClients - qBittorrent, TorrentClients - qBittorrent, TorrentClients - qBittorrent"
    type: bool
  - name: uTorrent
    description: "uTorrent (by Banaanhangwagen): TorrentClients - uTorrent"
    type: bool

  - name: KapeRules
    type: hidden
    description: A CSV file controlling the different Kape Target Rules
    default: |
      Id,Name,Category,Glob,Accessor,Comment
      1,$Boot,FileSystem,$Boot,ntfs,
      2,$J,FileSystem,$Extend/$UsnJrnl:$J,ntfs,
      3,$Max,FileSystem,$Extend/$UsnJrnl:$Max,ntfs,
      4,$J,FileSystem,$Extend/$J,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Targets are looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      5,$Max,FileSystem,$Extend/$Max,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Targets are looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      6,$LogFile,FileSystem,$LogFile,ntfs,
      7,$MFT,FileSystem,$MFT,ntfs,
      8,$MFTMirr,FileSystem,$MFTMirr,ntfs,$MFTMirr is a redundant copy of the first four (4) records of the MFT.
      9,$SDS,FileSystem,$Secure:$SDS,ntfs,
      10,$SDS,FileSystem,$Secure_$SDS,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Target is looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      11,$T,FileSystem,$Extend/$RmMetadata/$TxfLog/$Tops:$T,ntfs,
      12,$T,FileSystem,$Extend/$RmMetadata/$TxfLog/$T,ntfs,This is for the use case when you're running this Target against a mounted VHDX with these files already pulled from a live system. The above Target is looking for the files as an ADS whereas once they are already pulled they no longer match the ADS criteria and therefore are missed
      13,1Password Database,Apps,Users/*/AppData/Local/1password/data/1Password10.sqlite,lazy_ntfs,"Database which holds information about 1Password installation, such as accounts, categories, settings and more"
      14,1Password Backup Databases,Apps,Users/*/AppData/Local/1password/backups/1Password10.sqlite,lazy_ntfs,Backups of 1Password Database
      15,1Password Logs,Apps,Users/*/AppData/Local/1password/logs/*.log,lazy_ntfs,Log of usage of 1Password - can be useful for identifying periods of user activity
      16,4K Video Downloader,Apps,Users/*/AppData/Local/4kdownload.com/4K Video Downloader/4K Video Downloader/*.sqlite,lazy_ntfs,Grabs database(s) that stores user download history
      17,4K Video Downloader+,Apps,Users/*/AppData/Local/4kdownload.com/4K Video Downloader+/4K Video Downloader+/*.sqlite,lazy_ntfs,Grabs database(s) that stores user download history
      18,AVG AV Logs (XP),Antivirus,Documents and Settings/All Users/Application Data/AVG/Antivirus/log/**10,lazy_ntfs,
      19,AVG AV Report Logs (XP),Antivirus,Documents and Settings/All Users/Application Data/AVG/Antivirus/report/**10,lazy_ntfs,
      20,AVG AV Logs,Antivirus,ProgramData/AVG/Antivirus/log/**10,lazy_ntfs,
      21,AVG Report Logs,Antivirus,ProgramData/AVG/Antivirus/report/**10,lazy_ntfs,
      22,AVG Persistent Logs,Antivirus,ProgramData/AVG/Persistent Data/Antivirus/Logs/**10,lazy_ntfs,
      23,AVG FileInfo DB,Antivirus,ProgramData/AVG/Antivirus/**10/FileInfo2.db,lazy_ntfs,
      24,AVG lsdbj2 JSON,Antivirus,ProgramData/AVG/Antivirus/lsdb2.json,lazy_ntfs,
      25,AceText - Clipboard History,Apps,Users/*/Documents/*.atc,lazy_ntfs,Locates the Clipboard history for AceText
      26,Acronis True Image - Logs,Apps,ProgramData/Acronis/TrueImageHome/Logs/ti_demon/*,lazy_ntfs,Copies out all log files
      27,Acronis True Image - Database Files,Apps,ProgramData/Acronis/TrueImageHome/Database/archives.db*,lazy_ntfs,Copies out the Database folder which appears to have important information
      28,Acronis True Image - Scripts Folder,Apps,ProgramData/Acronis/TrueImageHome/Scripts/*,lazy_ntfs,Copies out all scripts files
      29,Action1 Client Application logs,ApplicationLogs,Windows/Action1/logs/*.log,lazy_ntfs,"Contains Application Log entries such as service start and incomming connections, and deployed scripts/jobs."
      30,NTDS,Active Directory,Windows/NTDS/**10,lazy_ntfs,
      31,SYSVOL,Active Directory,Windows/SYSVOL/**10,lazy_ntfs,
      32,Agent Ransack Config Logs,Software,Users/*/AppData/Roaming/Mythicsoft/AgentRansack/config/**10,lazy_ntfs,
      33,Agent Ransack CrashReports Logs,Software,Users/*/AppData/Roaming/Mythicsoft/AgentRansack/CrashReports/**10,lazy_ntfs,
      34,Agent Ransack IndexLog Logs,Software,Users/*/AppData/Roaming/Mythicsoft/AgentRansack/IndexLog/**10,lazy_ntfs,
      35,Agent Ransack Logs,Software,Users/*/AppData/Roaming/Mythicsoft/AgentRansack/logs/**10,lazy_ntfs,
      36,Amcache,ApplicationCompatibility,Windows/AppCompat/Programs/Amcache.hve,lazy_ntfs,
      37,Amcache,ApplicationCompatibility,Windows.old/Windows/AppCompat/Programs/Amcache.hve,lazy_ntfs,
      38,Amcache transaction files,ApplicationCompatibility,Windows/AppCompat/Programs/Amcache.hve.LOG*,lazy_ntfs,
      39,Amcache transaction files,ApplicationCompatibility,Windows.old/Windows/AppCompat/Programs/Amcache.hve.LOG*,lazy_ntfs,
      40,Ammyy Program Data,ApplicationLogs,ProgramData/Ammyy/**10,lazy_ntfs,"May not contain traditional log files, but presence of this folder may indicate historical usage"
      41,AnyDesk Logs - User Profile - *.trace,Communications,Users/*/AppData/Roaming/AnyDesk/*.trace,lazy_ntfs,Collects the trace logs for AnyDesk from a user profile
      42,AnyDesk Logs - ProgramData - *.trace,Communications,ProgramData/AnyDesk/*.trace,lazy_ntfs,Collects the trace logs for AnyDesk from ProgramData
      43,AnyDesk Logs - User Profile - *.conf,Communications,Users/*/AppData/Roaming/AnyDesk/*.conf,lazy_ntfs,Collects the conf logs for AnyDesk from a user profile
      44,AnyDesk Logs - ProgramData - *.conf,Communications,ProgramData/AnyDesk/*.conf,lazy_ntfs,Collects the conf logs for AnyDesk from ProgramData
      45,AnyDesk Videos,Communications,Users/*/Videos/AnyDesk/*.anydesk,lazy_ntfs,Collects any session recordings made by the user while using AnyDesk
      46,AnyDesk Logs - User Profile - connection_trace.txt,Communications,Users/*/AppData/Roaming/AnyDesk/connection_trace.txt,lazy_ntfs,Collects the connection trace log from user profile
      47,AnyDesk Logs - ProgramData - connection_trace.txt,Communications,ProgramData/AnyDesk/connection_trace.txt,lazy_ntfs,Collects the connection trace log from ProgramData
      48,AnyDesk Logs - System User Account,Communications,Windows/SysWOW64/config/systemprofile/AppData/Roaming/AnyDesk/*,lazy_ntfs,Collects the logs associated with the System user account
      49,AnyDesk Chat Logs - User Profile,Communications,Users/*/AppData/Roaming/AnyDesk/chat/*.txt,lazy_ntfs,Collects chat logs associated with the user profile
      50,Apache Access Log,Webservers,**10/access.log,lazy_ntfs,
      51,AppCompat PCA Folder,AppCompat,Windows/appcompat/pca,lazy_ntfs,
      52,AppData,UserData,Users/*/AppData/**10,lazy_ntfs,
      53,WindowsApps for AppX,Apps,Program Files/WindowsApps/Deleted*/**10,lazy_ntfs,Locates all the user AppX package directories which were installed through Microsoft Store and updated/uninstalled by the user.
      54,SystemApps for AppX,Apps,Windows/SystemApps/**10,lazy_ntfs,Locates all the system AppX package directories which were installed by the system.
      55,UserSpecificPackages for AppX,Apps,Users/*/AppData/Local/Packages/**10,lazy_ntfs,Locates all the user and system AppX package directories which are user specific on the system.
      56,AppRepository for AppX,Apps,ProgramData/Microsoft/Windows/AppRepository/Packages/**10/StateRepository-*.srd,lazy_ntfs,Locates the StateRepository .srd databases.
      57,ProgramData Packages for AppX,Apps,ProgramData/Packages/**10,lazy_ntfs,Locates the ProgramData AppX package directories.
      58,Application Event Log XP,EventLogs,Windows/System32/config/AppEvent.evt,lazy_ntfs,
      59,Application Event Log XP,EventLogs,Windows.old/Windows/System32/config/AppEvent.evt,lazy_ntfs,
      60,Application Event Log Win7+,EventLogs,Windows/System32/winevt/logs/application.evtx,lazy_ntfs,
      61,Application Event Log Win7+,EventLogs,Windows.old/Windows/System32/winevt/logs/application.evtx,lazy_ntfs,
      62,Aspera Client Logs,FileDownload,Users/*/AppData/Local/Aspera/Aspera Connect/var/log/**10/*.log,lazy_ntfs,
      63,Aspera Server Logs,FileDownload,Users/*/.aspera/connect/var/log/**10/*.log,lazy_ntfs,
      64,AteraAgent .ini files,Software,Program Files/ATERA Networks/AteraAgent/**10/*.ini,lazy_ntfs,Collects logs for AteraAgent
      65,AteraAgent Logs,Software,Program Files/ATERA Networks/AteraAgent/**10/*.txt,lazy_ntfs,Collects logs for AteraAgent
      66,AteraAgent Logs,Software,Program Files/ATERA Networks/AteraAgent/**10/*.db,lazy_ntfs,Collects logs for AteraAgent
      67,AteraAgent Logs,Software,Program Files/ATERA Networks/AteraAgent/**10/*.config,lazy_ntfs,Collects logs for AteraAgent
      68,AteraAgent Logs,Software,Program Files/ATERA Networks/AteraAgent/**10/*.cfg,lazy_ntfs,Collects logs for AteraAgent
      69,Avast AV Logs (XP),Antivirus,Documents And Settings/All Users/Application Data/Avast Software/Avast/Log/**10,lazy_ntfs,
      70,Avast AV Logs,Antivirus,ProgramData/Avast Software/Avast/Log/**10,lazy_ntfs,
      71,Avast AV User Logs,Antivirus,Users/*/Avast Software/Avast/Log/**10,lazy_ntfs,
      72,Avast AV Index,Antivirus,ProgramData/Avast Software/Avast/Chest/index.xml,lazy_ntfs,
      73,Avast Persistent Data Logs,Antivirus,ProgramData/Avast Software/Persistent Data/Avast/Logs/**10,lazy_ntfs,
      74,Avast Icarus Logs,Antivirus,ProgramData/Avast Software/Icarus/Logs/**10,lazy_ntfs,
      75,Avira Activity Logs,Antivirus,ProgramData/Avira/Antivirus/LOGFILES/**10,lazy_ntfs,Collects the scan logs of Avira Antivirus
      76,Avira Security Logs,Antivirus,ProgramData/Avira/Security/Logs/**10,lazy_ntfs,
      77,Avira VPN Logs,Antivirus,ProgramData/Avira/VPN/**10,lazy_ntfs,Collects the VPN logs
      78,BCD,Registry,Boot/BCD,lazy_ntfs,
      79,BCD Logs,Registry,Boot/BCD.LOG*,lazy_ntfs,
      80,BITS files,Persistence,ProgramData/Microsoft/Network/Downloader/**10,lazy_ntfs,
      81,TorrentClients - BitTorrent,FileDownload,Users/*/AppData/Roaming/BitTorrent/*.dat,lazy_ntfs,
      82,Bitdefender Endpoint Security Logs,Antivirus,ProgramData/Bitdefender/Endpoint Security/Logs/**10,lazy_ntfs,
      83,Bitdefender Internet Security Logs,Antivirus,ProgramData/Bitdefender/Desktop/Profiles/Logs/**10,lazy_ntfs,
      84,Bitdefender SQLite DB Files,Antivirus,Program Files*/Bitdefender*/**10/regex:*.+/.(db|db-wal|db-shm),ntfs,Bitdefender SQLite databases
      85,Box Drive Application Metadata,Apps,Users/*/AppData/Local/Box/Box/**10,lazy_ntfs,
      86,Box Sync Application Metadata,Apps,Users/*/AppData/Local/Box Sync/**10,lazy_ntfs,
      87,Box Drive User Files,Apps,Users/*/Box/**10,lazy_ntfs,Caution! This target will collect Box Drive contents from the local drive AND on-demand cloud files. Ensure your scope of authority permits cloud collections before use or isolate system from network
      88,Box Sync User Files,Apps,Users/*/Box Sync/**10,lazy_ntfs,
      89,Bookmarks,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Bookmarks*,lazy_ntfs,
      90,Cookies,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Cookies*,lazy_ntfs,
      91,Current Session,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Current Session,lazy_ntfs,
      92,Current Tabs,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Current Tabs,lazy_ntfs,
      93,Download Metadata,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/DownloadMetadata,lazy_ntfs,
      94,Favicons,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Favicons*,lazy_ntfs,
      95,History,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/History*,lazy_ntfs,
      96,Sessions Folder,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/Default/Sessions/*,lazy_ntfs,
      97,Login Data,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Login Data,lazy_ntfs,
      98,Network Action Predictor,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Network Action Predictor,lazy_ntfs,
      99,Network Persistent State,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Network Persistent State,lazy_ntfs,
      100,Preferences,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Preferences,lazy_ntfs,
      101,Quota Manager,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/QuotaManager,lazy_ntfs,
      102,Reporting and NEL,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Reporting and NEL,lazy_ntfs,
      103,Shortcuts,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Shortcuts*,lazy_ntfs,
      104,Publisher Info DB/Brave Rewards,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/publisher_info_db*,lazy_ntfs,"SQLite Database related to ""Brave Rewards"" containing an event_log table"
      105,Top Sites,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Top Sites*,lazy_ntfs,
      106,Visited Links,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Visited Links*,lazy_ntfs,
      107,Web Data,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Web Data*,lazy_ntfs,
      108,Secure Preferences,Communications,Users/*/AppData/Local/BraveSoftware/Brave-Browser/User Data/*/Secure Preferences*,lazy_ntfs,Contains additional preferences data
      109,Chrome Cache Folder,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Cache/**10,lazy_ntfs,
      110,Chromium Edge Cache Folder,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Cache/**10,lazy_ntfs,
      111,Firefox Cache Folder,Communications,Users/*/AppData/Local/Mozilla/Firefox/Profiles/*/**10,lazy_ntfs,
      112,IE 9/10 Cache,Communications,Users/*/AppData/Local/Microsoft/Windows/Temporary Internet Files/**10,lazy_ntfs,
      113,IE Index.dat temp internet files,Communications,Documents and Settings/*/Local Settings/Temporary Internet Files/Content.IE5/index.dat,lazy_ntfs,
      114,IE 11 Cache,Communications,Users/*/AppData/Local/Microsoft/Windows/INetCache/**10,lazy_ntfs,
      115,Edge WebcacheV01.dat,Communications,Users/*/AppData/Local/Microsoft/Windows/WebCache/*,lazy_ntfs,
      116,Brave Cache Folder,Communications,Users/%users%/AppData/Local/BraveSoftware/Brave-Browser/User Data/Default/Cache/Cache_Data/**10,lazy_ntfs,
      117,System CryptnetUrlCache,FileKnowledge,Windows/System32/config/systemprofile/AppData/LocalLow/Microsoft/CryptnetUrlCache/**10,lazy_ntfs,
      118,User CryptnetUrlCache,FileKnowledge,Users/*/AppData/LocalLow/Microsoft/CryptnetUrlCache/**10,lazy_ntfs,
      119,INetCache,FileKnowledge,Users/*/AppData/Local/Microsoft/Windows/INetCache/IE/**10,lazy_ntfs,
      120,Chrome bookmarks XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Bookmarks*,lazy_ntfs,
      121,Chrome Cookies XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Cookies*,lazy_ntfs,
      122,Chrome Current Session XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Current Session,lazy_ntfs,
      123,Chrome Current Tabs XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Current Tabs,lazy_ntfs,
      124,Chrome Favicons XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Favicons*,lazy_ntfs,
      125,Chrome History XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/History*,lazy_ntfs,
      126,Chrome Last Session XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Last Session,lazy_ntfs,
      127,Chrome Last Tabs XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Last Tabs,lazy_ntfs,
      128,Chrome Login Data XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Login Data,lazy_ntfs,
      129,Chrome Preferences XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Preferences,lazy_ntfs,
      130,Chrome Shortcuts XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Shortcuts*,lazy_ntfs,
      131,Chrome Top Sites XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Top Sites*,lazy_ntfs,
      132,Chrome Visited Links XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Visited Links,lazy_ntfs,
      133,Chrome Web Data XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Web Data*,lazy_ntfs,
      134,Chrome bookmarks,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Bookmarks*,lazy_ntfs,
      135,Chrome Cookies,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/**10/Cookies*,lazy_ntfs,
      136,Chrome Current Session,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Session,lazy_ntfs,
      137,Chrome Current Tabs,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Tabs,lazy_ntfs,
      138,Chrome Download Metadata,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/DownloadMetadata,lazy_ntfs,
      139,Chrome Extension Cookies,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Extension Cookies,lazy_ntfs,
      140,Chrome Favicons,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Favicons*,lazy_ntfs,
      141,Chrome History,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/History*,lazy_ntfs,
      142,Chrome Last Session,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Session,lazy_ntfs,
      143,Chrome Last Tabs,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Tabs,lazy_ntfs,
      144,Chrome Sessions Folder,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Sessions/*,lazy_ntfs,
      145,Chrome Login Data,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Login Data,lazy_ntfs,
      146,Chrome Media History,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Media History*,lazy_ntfs,
      147,Chrome Network Action Predictor,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Action Predictor,lazy_ntfs,
      148,Chrome Network Persistent State,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Persistent State,lazy_ntfs,
      149,Chrome Preferences,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Preferences,lazy_ntfs,
      150,Chrome Quota Manager,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/QuotaManager,lazy_ntfs,
      151,Chrome Reporting and NEL,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Reporting and NEL,lazy_ntfs,
      152,Chrome Shortcuts,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Shortcuts*,lazy_ntfs,
      153,Chrome Top Sites,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Top Sites*,lazy_ntfs,
      154,Chrome Trust Tokens,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Trust Tokens*,lazy_ntfs,
      155,Chrome SyncData Database,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Sync Data/SyncData.sqlite3,lazy_ntfs,
      156,Chrome Visited Links,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Visited Links,lazy_ntfs,
      157,Chrome Web Data,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Web Data*,lazy_ntfs,
      158,Windows Protect Folder,FileSystem,Users/*/AppData/Roaming/Microsoft/Protect/*/**10,lazy_ntfs,Required for offline decryption
      159,Chrome Snapshots Folder,Communications,Users/*/AppData/Local/Google/Chrome/User Data/Snapshots/*/**10,lazy_ntfs,Grabs folder that appears to have snapshots of Chrome SQLite DBs organized by version #.
      160,Chrome Extension Files,Communication,Users/*/AppData/Local/Google/Chrome/User Data/*/Extensions/**10,lazy_ntfs,
      161,Chrome Extension Files XP,Communications,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Extensions/**10,lazy_ntfs,
      162,Chrome HTML5 File System Folder,Communication,Users/*/AppData/Local/Google/Chrome/User Data/*/File System/**10,lazy_ntfs,
      163,Cisco Jabber Database,Communications,Users/*/AppData/Local/Cisco/Unified Communications/Jabber/CSF/History/*.db,lazy_ntfs,The Cisco Jabber process needs to be killed before database can be copied.
      164,ClipboardMaster - Clipboard History - Text,Apps,Users/*/AppData/Roaming/Jumping Bytes/ClipboardMaster/Clipboard.clm4,lazy_ntfs,Locates the user’s clipboard history (text) for ClipboardMaster
      165,ClipboardMaster - Clipboard History - Images,Apps,Users/*/AppData/Roaming/Jumping Bytes/ClipboardMaster/pics/**10,lazy_ntfs,Locates the user’s clipboard history (images) for ClipboardMaster
      166,ClipboardMaster - Clipboard History - Backups,Apps,Users/*/AppData/Roaming/Jumping Bytes/ClipboardMaster/Clipboard.clm4.ba*,lazy_ntfs,Locates the user’s clipboard history (backups) for ClipboardMaster
      167,ComboFix,Antivirus,ComboFix.txt,lazy_ntfs,
      168,Confluence Wiki Log Files,Logs,Atlassian/Application Data/Confluence/logs/*.log*,lazy_ntfs,
      169,Confluence Wiki Log Files,Logs,Program Files/Atlassian/Confluence/logs/*.log,lazy_ntfs,
      170,Cybereason Anti-Ransomware Logs,Antivirus,ProgramData/crs1/Logs/**10,lazy_ntfs,
      171,Cybereason Sensor Communications and Anti-Malware Logs,Antivirus,ProgramData/apv2/Logs/**10,lazy_ntfs,
      172,Cybereason Application Control and NGAV Logs,Antivirus,ProgramData/crb1/Logs/**10,lazy_ntfs,
      173,Cylance ProgramData Logs,Antivirus,ProgramData/Cylance/Desktop/**10,lazy_ntfs,
      174,Cylance Optics Logs,Antivirus,ProgramData/Cylance/Optics/Log/**10,lazy_ntfs,
      175,Cylance Program Files Logs,Antivirus,Program Files/Cylance/Desktop/log/**10,lazy_ntfs,
      176,DC++ Chat Logs,FileDownload,Users/*/AppData/Local/DC++/Logs/**10,lazy_ntfs,Locates DC++ hub/chat logs and copies them. Current as of version 0.868.
      177,DWAgent Log Files,Logs,ProgramData/DWAgent*/*.log*,lazy_ntfs,
      178,Debian WSL /etc/debian_version,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/debian_version,lazy_ntfs,
      179,Debian WSL /etc/fstab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/fstab,lazy_ntfs,
      180,Debian WSL /etc/os-release,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/os-release,lazy_ntfs,
      181,Debian WSL /etc/passwd,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/passwd,lazy_ntfs,
      182,Debian WSL /etc/group,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/group,lazy_ntfs,
      183,Debian WSL /etc/shadow,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/shadow,lazy_ntfs,
      184,Debian WSL /etc/timezone,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/timezone,lazy_ntfs,
      185,Debian WSL /etc/hostname,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/hostname,lazy_ntfs,
      186,Debian WSL /etc/hosts,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/hosts,lazy_ntfs,
      187,Debian WSL /etc/crontab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/crontab,lazy_ntfs,
      188,Debian WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/bash.bashrc,lazy_ntfs,
      189,Debian WSL /etc/profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/etc/profile,lazy_ntfs,
      190,Debian WSL .bash_history,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/**10/.bash_history,lazy_ntfs,
      191,Debian WSL .bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/**10/.bashrc,lazy_ntfs,
      192,Debian WSL .profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/**10/.profile,lazy_ntfs,
      193,Debian WSL User Crontabs,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/var/spool/cron/crontabs/**10,lazy_ntfs,
      194,Debian WSL Apt Logs,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/rootfs/var/log/apt/**10/*.log,lazy_ntfs,
      195,Debian WSL ext4.vhdx,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/TheDebianProject.DebianGNULinux_*/LocalState/ext4.vhdx,lazy_ntfs,
      196,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/MRU/rename_folders.osd,lazy_ntfs,Locates .osd file which contains names of folders that have been renamed manually by the user.
      197,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/MRU/rename_files.osd,lazy_ntfs,Locates .osd file which contains names of files that have been renamed manually by the user.
      198,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/MRU/find_contains.osd,lazy_ntfs,Locates .osd file which contains search queries initiated by the user during a search for files with contents related to the search query.
      199,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/MRU/find_name.osd,lazy_ntfs,Locates .osd file which contains search queries initiated by the user during a search for files with a filename related to the search query.
      200,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/MRU/find_path.osd,lazy_ntfs,Locates .osd file which contains file paths related to user activity - not exactly sure how these are generated at this time.
      201,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/recent.osd,lazy_ntfs,Locates .osd file which contains file paths related to recent user activity. Effectively the DOpus Shellbags-equivalent. Appears to be for last 10 folder visited within the Lister.
      202,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/State Data/backupconfig.osd,lazy_ntfs,Locates .osd file which contains file paths related to the location of the backup settings files for Directory Opus.
      203,Directory Opus,Apps,Users/*/AppData/Local/GPSoftware/Directory Opus/Thumbnail Cache/*,lazy_ntfs,Locates .osd file which contains file paths related to the location of the backup settings files for Directory Opus.
      204,Directory Opus,Apps,Users/*/AppData/Roaming/GPSoftware/Directory Opus/Logs/*,lazy_ntfs,Locates .txt files that will be named with the IP address of the FTP server Directory Opus was used to connect to. All-activity.txt will simply be a combination of all other .txt files present in this directory.
      205,Audio files,Multimedia,**10/regex:*.+/.(3gp|aa|aac|act|aiff|alac|amr|ape|au|awb|dss|dvf|flac|gsm|iklax|ivs|m4a|m4b|m4p|mmf|mp3|mpc|msv|nmf|ogg|oga|mogg|opus|ra|rm|raw|rf64|sln|tta|voc|vox|wav|wma|wv|webm),ntfs,Covers most (if not all) audio file formats
      206,Excel and Excel-like Documents,Documents,**10/regex:*.+/.(xls|xlsx|csv|tsv|xlt|xlm|xlsm|xltx|xltm|xlsb|xla|xlam|xll|xlw|ods|fodp|qpw),ntfs,"Covers all document file formats for Excel, OpenOffice, LibreOffice, Apache OpenOffice, WPS Office, SoftMaker Office, and more"
      207,PDF and PDF-like Documents,Documents,**10/regex:*.+/.(pdf|xps|oxps),ntfs,Covers all PDF and PDF-like document formats
      208,Picture files,Multimedia,**10/regex:*.+/.(ai|bmp|bpg|cdr|cpc|eps|exr|flif|gif|heif|ilbm|ima|jp2|j2k|jpf|jpm|jpg2|j2c|jpc|jpx|mj2jpeg|jpg|jxl|kra|ora|pcx|pgf|pgm|png|pnm|ppm|psb|psd|psp|svg|tga|tiff|webp|xaml|xcf),ntfs,Covers most (if not all) picture file formats
      209,SQLite Files (.db* and .sqlite*),Databases,**10/regex:*.+/.(db*|sqlite*|),ntfs,Covers all common file extensions for SQLite databases
      210,Video files,Multimedia,**10/regex:*.+/.(3g2|3gp|amv|asf|avi|drc|flv|f4v|f4p|f4a|f4b|gif|gifv|m4v|mkv|mov|qt|mp4|m4p|mpg|mpeg|m2v|mp2|mpe|mpv|mts|m2ts|ts|mxf|nsv|ogv|ogg|rm|rmvb|roq|svi|viv|vob|webm|wmv|yuv),ntfs,Covers most (if not all) video file formats
      211,Zips,Archives,**10/*.zip,lazy_ntfs,This is an example of how to walk a drive for a file mask. Probably do not want to use this one as is
      212,Word and Word-like Documents,Documents,**10/regex:*.+/.(doc|docx|docm|dotx|dotm|docb|dot|wbk|odt|fodt|rtf|wp*|tmd),ntfs,"Covers all document file formats for Word, OpenOffice, LibreOffice, Apache OpenOffice, WPS Office, SoftMaker Office, and more"
      213,Discord Cache Files,Communications,Users/*/AppData/Roaming/discord/cache/**10,lazy_ntfs,Gets cached data from Discord app
      214,Discord Local Storage LevelDB Files,Communications,Users/*/AppData/Roaming/discord/local storage/leveldb/**10,lazy_ntfs,Gets LevelDB database from Discord app
      215,Double Commander - history.xml,Apps,Users/*/AppData/Roaming/doublecmd/history.xml,lazy_ntfs,Locates an .xml file that contains Shellbags-equivalent artifacts that are sorted in temporal order from bottom to top.
      216,Double Commander - doublecmd.xml,Apps,Users/*/AppData/Roaming/doublecmd/doublecmd.xml,lazy_ntfs,Locates an .xml file that contains Shellbags-equivalent artifacts that are sorted in temporal order from top to bottom.
      217,Double Commander - FTP Log,Apps,Users/*/AppData/Roaming/doublecmd/doublecmd*.log,lazy_ntfs,Locates log files that'll be named with the following naming convention: doublecmd_2021-04-03.log.
      218,Double Commander - multiarc.ini,Apps,Users/*/AppData/Roaming/doublecmd/multiarc.ini,lazy_ntfs,
      219,Double Commander - session.ini,Apps,Users/*/AppData/Roaming/doublecmd/session.ini,lazy_ntfs,
      220,Double Commander - pixmaps.txt,Apps,Users/*/AppData/Roaming/doublecmd/pixmaps.txt,lazy_ntfs,
      221,Double Commander - shortcuts.scf,Apps,Users/*/AppData/Roaming/doublecmd/shortcuts.scf,lazy_ntfs,
      222,Drivers,Drivers,Windows/system32/drivers/**10/*.sys,lazy_ntfs,
      223,Dropbox Metadata,Apps,Users/*/AppData/Local/Dropbox/info.json,lazy_ntfs,Getting individual files because folder may contain very large extraneous files. Info.json contains user's Dropbox folder location
      224,Dropbox Metadata,Apps,Users/*/AppData/Local/Dropbox/host.db,lazy_ntfs,SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64.
      225,Dropbox Metadata,Apps,Users/*/AppData/Local/Dropbox/machine_storage/tray-thumbnails.db,lazy_ntfs,SQLite database containing references to image files at one time present in a user’s Dropbox instance.
      226,Dropbox Metadata,Apps,Users/*/AppData/Local/Dropbox/host.dbx,lazy_ntfs,"SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
      227,Windows Protect Folder,FileSystem,Users/*/AppData/Roaming/Microsoft/Protect/*/**10,lazy_ntfs,Required for offline decryption of Dropbox databases
      228,Dropbox Metadata,Apps,Users/*/AppData/Local/Dropbox/instance*/**10,lazy_ntfs,instance folder holds multiple SQLite databases related to Dropbox activity and contents
      229,Dropbox User Files,Apps,Users/*/Dropbox*/**10,lazy_ntfs,"Default storage location for Dropbox Personal and Business (when using wildcard), but can be user-defined. Check info.json file in user Dropbox metadata files to identify default folder."
      230,EF Commander - .ini File,Apps,Users/*/AppData/Roaming/EFSoftware/*,lazy_ntfs,Locates folder where all configuration files reside
      231,ESET NOD32 AV Logs (XP),Antivirus,Documents and Settings/All Users/Application Data/ESET/ESET NOD32 Antivirus/Logs/**10,lazy_ntfs,
      232,ESET NOD32 AV Logs,Antivirus,ProgramData/ESET/ESET NOD32 Antivirus/Logs/**10,lazy_ntfs,Parser available at https://github.com/laciKE/EsetLogParser
      233,ESET NOD32 AV Logs,Antivirus,ProgramData/ESET/ESET Security/Logs/**10,lazy_ntfs,
      234,ESET Remote Administrator Logs,Antivirus,ProgramData/ESET/RemoteAdministrator/Agent/EraAgentApplicationData/Logs,lazy_ntfs,Remote Administrator logs include information on tasks executed on the target.
      235,Local User Quarantine,Antivirus,Users/*/AppData/Local/ESET/ESET Security/Quarantine/**10,lazy_ntfs,
      236,SYSTEM user quarantine,Antivirus,/Windows/System32/config/systemprofile/AppData/Local/ESET/ESET Security/Quarantine/**10,lazy_ntfs,
      237,Edge folder,Communications,Users/*/AppData/Local/Packages/Microsoft.MicrosoftEdge_8wekyb3d8bbwe/**10,lazy_ntfs,
      238,Edge bookmarks,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Bookmarks*,lazy_ntfs,
      239,Edge Collections,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Collections/collectionsSQLite,lazy_ntfs,
      240,Edge Cookies,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/**10/Cookies*,lazy_ntfs,
      241,Edge Current Session,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Current Session,lazy_ntfs,
      242,Edge Current Tabs,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Current Tabs,lazy_ntfs,
      243,Edge Favicons,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Favicons*,lazy_ntfs,
      244,Edge History,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/History*,lazy_ntfs,
      245,Edge Last Session,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Last Session,lazy_ntfs,
      246,Edge Last Tabs,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Last Tabs,lazy_ntfs,
      247,Edge Sessions Folder,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Sessions/*,lazy_ntfs,
      248,Edge Login Data,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Login Data,lazy_ntfs,
      249,Edge Media History,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Media History*,lazy_ntfs,
      250,Edge Network Action Predictor,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Network Action Predictor,lazy_ntfs,
      251,Edge Preferences,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Preferences,lazy_ntfs,
      252,Edge Shortcuts,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Shortcuts*,lazy_ntfs,
      253,Edge Top Sites,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Top Sites*,lazy_ntfs,
      254,Edge SyncData Database,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Sync Data/SyncData.sqlite3,lazy_ntfs,
      255,Edge Bookmarks,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Bookmarks*,lazy_ntfs,
      256,Edge Visited Links,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Visited Links,lazy_ntfs,
      257,Edge Web Data,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Web Data*,lazy_ntfs,
      258,Edge WebAssistDatabase,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/*/WebAssistDatabase*,lazy_ntfs,
      259,Windows Protect Folder,FileSystem,Users/*/AppData/Roaming/Microsoft/Protect/*/**10,lazy_ntfs,Required for offline DPAPI decryption
      260,Edge Snapshots Folder,Communications,Users/*/AppData/Local/Microsoft/Edge/User Data/Snapshots/*/**10,lazy_ntfs,"Grabs folder that appears to have snapshots of Edge Chromium SQLite DBs organized by version #. In testing, there were 3 previous versions of Edge Chromium separated into different folders"
      261,Edge Chromium Extension Files,Communication,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Extensions/**10,lazy_ntfs,
      262,Emsisoft Scan Logs,ApplicationLogs,ProgramData/Emsisoft/Reports/scan*.txt,lazy_ntfs,Can contain file detection and quarantine info
      263,EncapsulationLogging,Executables,Windows/Appcompat/Programs/EncapsulationLogging.hve,lazy_ntfs,
      264,EncapsulationLogging,Executables,Windows.old/Windows/Appcompat/Programs/EncapsulationLogging.hve,lazy_ntfs,
      265,EncapsulationLogging Logs,Executables,Windows/Appcompat/Programs/EncapsulationLogging.hve.log*,lazy_ntfs,
      266,EncapsulationLogging Logs,Executables,Windows.old/Windows/Appcompat/Programs/EncapsulationLogging.hve.log*,lazy_ntfs,
      267,Event logs Win7+,EventLogs,Windows/System32/winevt/logs/System.evtx,lazy_ntfs,
      268,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/logs/System.evtx,lazy_ntfs,
      269,Event logs Win7+,EventLogs,Windows/System32/winevt/logs/Security.evtx,lazy_ntfs,
      270,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/logs/Security.evtx,lazy_ntfs,
      271,Event logs Win7+,EventLogs,Windows/System32/winevt/Logs/Microsoft-Windows-TerminalServices-RDPClient%4Operational.evtx,lazy_ntfs,
      272,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/Logs/Microsoft-Windows-TerminalServices-RDPClient%4Operational.evtx,lazy_ntfs,
      273,Event logs Win7+,EventLogs,Windows/System32/winevt/Logs/Microsoft-Windows-RemoteDesktopServices-RdpCoreTS%4Operational.evtx,lazy_ntfs,
      274,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/Logs/Microsoft-Windows-RemoteDesktopServices-RdpCoreTS%4Operational.evtx,lazy_ntfs,
      275,Event logs Win7+,EventLogs,Windows/System32/winevt/Logs/Microsoft-Windows-TerminalServices-RemoteConnectionManager%4Operational.evtx,lazy_ntfs,
      276,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/Logs/Microsoft-Windows-TerminalServices-RemoteConnectionManager%4Operational.evtx,lazy_ntfs,
      277,Event logs Win7+,EventLogs,Windows/System32/winevt/Logs/Microsoft-Windows-TerminalServices-LocalSessionManager%4Operational.evtx,lazy_ntfs,
      278,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/Logs/Microsoft-Windows-TerminalServices-LocalSessionManager%4Operational.evtx,lazy_ntfs,
      279,Event logs XP,EventLogs,Windows/System32/config/*.evt,lazy_ntfs,
      280,Event logs Win7+,EventLogs,Windows/System32/winevt/logs/*.evtx,lazy_ntfs,
      281,Event logs Win7+,EventLogs,Windows.old/Windows/System32/winevt/logs/*.evtx,lazy_ntfs,
      282,WDI Trace Logs 1,Event Trace Logs,Windows/System32/WDI/LogFiles/*.etl*,lazy_ntfs,
      283,WDI Trace Logs 1,Event Trace Logs,Windows.old/Windows/System32/WDI/LogFiles/*.etl*,lazy_ntfs,
      284,WDI Trace Logs 2,Event Trace Logs,Windows/System32/WDI/{*/**10,lazy_ntfs,
      285,WDI Trace Logs 2,Event Trace Logs,Windows.old/Windows/System32/WDI/{*/**10,lazy_ntfs,
      286,WMI Trace Logs,Event Trace Logs,Windows/System32/LogFiles/WMI/**10,lazy_ntfs,
      287,WMI Trace Logs,Event Trace Logs,Windows.old/Windows/System32/LogFiles/WMI/**10,lazy_ntfs,
      288,SleepStudy Trace Logs,Event Trace Logs,Windows/System32/SleepStudy/**10,lazy_ntfs,
      289,SleepStudy Trace Logs,Event Trace Logs,Windows.old/Windows/System32/SleepStudy/**10,lazy_ntfs,
      290,Energy-NTKL Trace Logs,Event Trace Logs,ProgramData/Microsoft/Windows/PowerEfficiency Diagnostics/energy-ntkl.etl,lazy_ntfs,
      291,Delivery Optimization Trace Logs,Event Trace Logs,Windows/ServiceProfiles/NetworkService/AppData/Local/Microsoft/Windows/DeliveryOptimization/Logs/*.etl*,lazy_ntfs,
      292,EventTranscript.db,SystemEvents,ProgramData/Microsoft/Diagnosis/EventTranscript/EventTranscript.db*,lazy_ntfs,
      293,EventTranscript.db,SystemEvents,Windows.old/ProgramData/Microsoft/Diagnosis/EventTranscript/EventTranscript.db*,lazy_ntfs,
      294,Microsoft Office Diagnostic Logs,SystemEvents,Users/%User%/AppData/Local/Temp/Diagnostics/**10,lazy_ntfs,
      295,Evernote Accounts,App,Users/*/AppData/Local/Evernote/Evernote/Databases/**10/.accounts,lazy_ntfs,Holds username and email of accounts
      296,Evernote Notebooks,App,Users/*/AppData/Local/Evernote/Evernote/Databases/**10/*.exb,lazy_ntfs,SQLite Database of the notes
      297,Evernote Notebook Snippets,App,Users/*/AppData/Local/Evernote/Evernote/Databases/**10/*.exb.snippets,lazy_ntfs,Note 'Snippets'
      298,Everything (VoidTools),FileSystem,Users/*/AppData/Local/Everything/Everything.db,lazy_ntfs,Copies out Everything.db
      299,Everything (VoidTools) - Run History,FileSystem,Users/*/AppData/Roaming/Everything/Run History.csv,lazy_ntfs,Copies out a CSV containing the history of items ran from Everything's search results window
      300,Everything (VoidTools) - Search History,FileSystem,Users/*/AppData/Roaming/Everything/Search History.csv,lazy_ntfs,Copies out a CSV containing the history of items searched for within Everything with timestamps
      301,Everything (VoidTools) - .ini file,FileSystem,Users/*/AppData/Roaming/Everything/Everything.ini,lazy_ntfs,Copies out the .ini file for Everything
      302,Exchange client access log files,Logs,Program Files/Microsoft/Exchange Server/*/Logging/**10/*.log,lazy_ntfs,Highly dependent on Exchange configuration
      303,Exchange Server Modified Compiled Files,Apps,Windows/Microsoft.NET/Framework*/v*/Temporary ASP.NET Files/**10/Regex:*./b[a-zA-Z0-9_-]{8}/b.compiled,ntfs,Highly dependent on Exchange configuration
      304,Exchange Server Modified Compiled Files,Apps,inetpub/wwwroot/aspnet_client/**10/Regex:*./b[a-zA-Z0-9_-]{8}/b.compiled,ntfs,Highly dependent on Exchange configuration
      305,Exchange Server Modified Compiled Files,Apps,inetpub/wwwroot/aspnet_client/system_web/**10/Regex:*./b[a-zA-Z0-9_-]{8}/b.compiled,ntfs,Highly dependent on Exchange configuration
      306,Exchange Server Modified Compiled Files,Apps,Program Files/Microsoft/Exchange Server/V15/FrontEnd/HttpProxy/owa/auth/**10/Regex:*./b[a-zA-Z0-9_-]{8}/b.compiled,ntfs,Highly dependent on Exchange configuration
      307,Exchange TransportRoles log files,Logs,Program Files/Microsoft/Exchange Server/*/TransportRoles/Logs/**10/*.log,lazy_ntfs,Highly dependent on Exchange configuration
      308,F-Secure Logs,Antivirus,ProgramData/F-Secure/Log/**10,lazy_ntfs,
      309,F-Secure User Logs,Antivirus,Users/*/AppData/Local/F-Secure/Log/**10,lazy_ntfs,
      310,F-Secure Scheduled Scan Reports,Antivirus,ProgramData/F-Secure/Antivirus/ScheduledScanReports/**10,lazy_ntfs,
      311,Fences - Desktop Screenshots,Apps,Users/*/AppData/Roaming/Stardock/Fences/Backups,lazy_ntfs,Locates all screenshots taken automatically by the Fences application
      312,FileZilla XML Log Files,Logs,Users/*/AppData/Roaming/FileZilla/*.xml*,lazy_ntfs,
      313,FileZilla SQLite3 Log Files,Logs,Users/*/AppData/Roaming/FileZilla/*.sqlite3*,lazy_ntfs,
      314,FileZilla Server XML Log Files,Logs,Users/*/AppData/Roaming/FileZilla Server/*.xml*,lazy_ntfs,
      315,FileZilla Log Files,Logs,Program Files (x86)/FileZilla Server/Logs/*.log*,lazy_ntfs,
      316,Addons,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/addons.sqlite*,lazy_ntfs,
      317,Bookmarks,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/weave/bookmarks.sqlite*,lazy_ntfs,
      318,Bookmarks,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/bookmarkbackups/**10,lazy_ntfs,
      319,Cookies,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/cookies.sqlite*,lazy_ntfs,
      320,Cookies,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/firefox_cookies.sqlite*,lazy_ntfs,
      321,Downloads,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/downloads.sqlite*,lazy_ntfs,
      322,Extensions,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/extensions.json,lazy_ntfs,
      323,Favicons,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/favicons.sqlite*,lazy_ntfs,
      324,Form history,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/formhistory.sqlite*,lazy_ntfs,
      325,Permissions,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/permissions.sqlite*,lazy_ntfs,
      326,Places,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/places.sqlite*,lazy_ntfs,
      327,Protections,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/protections.sqlite*,lazy_ntfs,
      328,Search,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/search.sqlite*,lazy_ntfs,
      329,Signons,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/signons.sqlite*,lazy_ntfs,
      330,Storage Sync,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/storage-sync.sqlite*,lazy_ntfs,
      331,Webappstore,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/webappstore.sqlite*,lazy_ntfs,
      332,Password,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/key*.db,lazy_ntfs,
      333,Password,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/signon*.*,lazy_ntfs,
      334,Password,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/logins.json,lazy_ntfs,
      335,Preferences,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/prefs.js,lazy_ntfs,
      336,Sessionstore,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/sessionstore*,lazy_ntfs,
      337,Sessionstore Folder,Communications,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/sessionstore-backups/**10,lazy_ntfs,
      338,Places XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/places.sqlite*,lazy_ntfs,
      339,Downloads XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/downloads.sqlite*,lazy_ntfs,
      340,Form history XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/formhistory.sqlite*,lazy_ntfs,
      341,Cookies XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/cookies.sqlite*,lazy_ntfs,
      342,Signons XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/signons.sqlite*,lazy_ntfs,
      343,Webappstore XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/webappstore.sqlite*,lazy_ntfs,
      344,Favicons XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/favicons.sqlite*,lazy_ntfs,
      345,Addons XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/addons.sqlite*,lazy_ntfs,
      346,Search XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/search.sqlite*,lazy_ntfs,
      347,Password XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/key*.db,lazy_ntfs,
      348,Password XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/signon*.*,lazy_ntfs,
      349,Password XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/logins.json,lazy_ntfs,
      350,Sessionstore XP,Communications,Documents and Settings/*/Application Data/Mozilla/Firefox/Profiles/*/sessionstore*,lazy_ntfs,
      351,Free Commander - FreeCommander.ini,Apps,Users/*/AppData/Local/FreeCommanderXE/Settings/FreeCommander.ini,lazy_ntfs,Locates an .ini file that contains Shellbags-equivalent artifacts.
      352,Free Commander - FreeCommander.ftp.ini,Apps,Users/*/AppData/Local/FreeCommanderXE/Settings/FreeCommander.ftp.ini,lazy_ntfs,Locates an .ini file that contains the file path to the FTP log for Free Commander.
      353,Free Commander - FreeCommander.hist.ini,Apps,Users/*/AppData/Local/FreeCommanderXE/Settings/FreeCommander.hist.ini,lazy_ntfs,Locates an .ini file that contains Shellbags-equivalent artifacts that are sorted in temporal order from top to bottom for both left and right directory browsers.
      354,Free Commander - FreeCommander.fav.xml,Apps,Users/*/AppData/Local/FreeCommanderXE/Settings/FreeCommander.fav.xml,lazy_ntfs,Locates an .xml file that contains favorited files/folder by the user.
      355,Free Commander - Backup Settings,Apps,Users/*/AppData/Local/FreeCommanderXE/Settings/Bkp_Settings*/**10,lazy_ntfs,"Locates an exact copy of the above files which will have a timestamped folder name, i.e. Bkp_Settings-YYYY-MM-DD HH-MM-SS."
      356,Free Commander - FTP Log,Apps,Users/*/AppData/Local/Temp/fc*.log,lazy_ntfs,Locates log file(s) that have a default naming convention of fc_ftplog_20210403 but can be modified by the user.
      357,Free Commander - FTP Related Information,Apps,Users/*/AppData/Local/Temp/FreeCommander*/**10,lazy_ntfs,Locates a folder that may be named randomly that contains more FTP related information as well as .tmp files that are created while the user is traversing folders during an active FTP session. These files are deleted upon program exit.
      358,FDM Database,App,Users/*/AppData/Local/Free Download Manager/**10/fdm.sqlite,lazy_ntfs,"fdm.sqlite shows Torrents, downloads, folder history, auth credentials and more. Will also pull fdm.sqlite in db_backup/"
      359,FDM Backup Info,App,Users/*/AppData/Local/Free Download Manager/backup/backup.info,lazy_ntfs,"Backup info file - can change backup name from userdata.zip, so could give indication of file name"
      360,FDM Database (userdata.zip),App,Users/*/AppData/Local/Free Download Manager/backup/userdata.zip,lazy_ntfs,fdm.sqlite can also appear in the backup folder in a compressed userdata.zip file
      361,FreeFileSync,Apps,Users/*/AppData/Roaming/FreeFileSync/Logs,lazy_ntfs,Copies out all log files
      362,Freenet,File Downloads,Users/*/AppData/Local/Freenet/node*,lazy_ntfs,
      363,Freenet,File Downloads,Users/*/AppData/Local/Freenet/*completed.list.downloads,lazy_ntfs,
      364,Freenet,File Downloads,Users/*/AppData/Local/Freenet/*completed.list.uploads,lazy_ntfs,
      365,Freenet,File Downloads,Users/*/AppData/Local/Freenet/*.bak,lazy_ntfs,
      366,Freenet,File Downloads,Users/*/AppData/Local/Freenet/downloads/**10,lazy_ntfs,
      367,FrostWire Downloads,FileDownload,Users/*/Documents/FrostWire/Torrent Data/**10,lazy_ntfs,Locates files downloaded that land in the default location as specified by FrostWire
      368,FrostWire AppData,FileDownload,Users/*/.frostwire5/frostwire.props,lazy_ntfs,Locates a file that contains important information about the instance of FrostWire on the user's system
      369,FrostWire AppData,FileDownload,Users/*/.frostwire5/itunes.props,lazy_ntfs,Locates a file that contains important information about the instance of FrostWire on the user's system
      370,Gigatribe Files Windows Vista/7/8/10,FileDownload,Users/*/AppData/Local/Shalsoft/**10,lazy_ntfs,Locates Gigatribe files and copies them
      371,Gigatribe Files Windows XP,FileDownload,Documents and Settings/*/*/Application Data/Gigatribe/**10,lazy_ntfs,Locates Gigatribe files and copies them. Different path depending on the Operating System language. In Swedish the location is C:\Documents and Settings\&lt;username&gt;\Lokala Inställningar\Application Data\Gigatribe
      372,Gigatribe Files Windows XP,FileDownload,Documents and Settings/*/*/Application Data/Shalsoft/**10,lazy_ntfs,Locates Gigatribe files and copies them. Different path depending on the Operating System language. In Swedish the location is C:\Documents and Settings\&lt;username&gt;\Lokala Inställningar\Application Data\Shalsoft
      373,Google Drive Backup and Sync User Files,Apps,Users/*/Google Drive*/**10,lazy_ntfs,Older Google Drive Backup and Sync application only
      374,Google Drive Backup and Sync Metadata,Apps,Users/*/AppData/Local/Google/Drive/**10,lazy_ntfs,Older version of Google Drive
      375,Google Drive for Desktop Metadata,Apps,Users/*/AppData/Local/Google/DriveFS/**10,lazy_ntfs,Metadata folder the same for both newer Google Drive for Desktop and older Google File Stream application
      376,Google Earth My Places file,Apps,Users/*/AppData/LocalLow/Google/GoogleEarth/myplaces.kml,lazy_ntfs,File which holds favorited locations
      377,Google Earth My Places Backup file,Apps,Users/*/AppData/LocalLow/Google/GoogleEarth/myplaces.backup.kml,lazy_ntfs,Backup file which holds favorited locations
      378,Google Earth My Places file (XP),Apps,Documents and Settings/*/Application Data/Google/GoogleEarth/myplaces.kml,lazy_ntfs,File which holds favorited locations
      379,Google Earth My Places Backup file (XP),Apps,Documents and Settings/*/Application Data/Google/GoogleEarth/myplaces.backup.kml,lazy_ntfs,Backup file which holds favorited locations
      380,Group Policy Files,Communication,Windows/System32/grouppolicy/**10,lazy_ntfs,
      381,Computer Group Policy files,Communication,ProgramData/Microsoft/Group Policy/History/**10,lazy_ntfs,
      382,User Group Policy files,Communication,Users/*/AppData/Local/Microsoft/Group Policy/History/**10,lazy_ntfs,
      383,Local Group Policy INI Files,Communication,Windows.old/Windows/System32/grouppolicy/*.ini,lazy_ntfs,
      384,Local Group Policy Files - Registry Policy Files,Communication,Windows/System32/grouppolicy/*.pol,lazy_ntfs,
      385,Local Group Policy Files - Registry Policy Files,Communication,Windows.old/Windows/System32/grouppolicy/*.pol,lazy_ntfs,
      386,Local Group Policy Files - Startup/Shutdown Scripts,Communication,Windows/System32/grouppolicy/*/Scripts/**10,lazy_ntfs,
      387,Local Group Policy Files - Startup/Shutdown Scripts,Communication,Windows.old/Windows/System32/grouppolicy/*/Scripts/**10,lazy_ntfs,
      388,HeidiSQL Backup files (*.sql),Apps,Users/*/AppData/Roaming/HeidiSQL/Backups/*,lazy_ntfs,
      389,HeidiSQL (tabs.ini),Apps,Users/*/AppData/Roaming/HeidiSQL/tabs.ini,lazy_ntfs,
      390,HexChat Chat Logs,Communications,Users/*/AppData/Roaming/HexChat/logs/**10,lazy_ntfs,
      391,HitmanPro Logs,Antivirus,ProgramData/HitmanPro/Logs/**10,lazy_ntfs,
      392,HitmanPro Alert Logs,Antivirus,ProgramData/HitmanPro.Alert/Logs/**10,lazy_ntfs,
      393,HitmanPro Database,Antivirus,ProgramData/HitmanPro.Alert/excalibur.db,lazy_ntfs,SQLite DB
      394,IIS applicationHost.config,Apps,Windows/System32/inetsrv/config/applicationHost.config,lazy_ntfs,This configuration file stores the settings for all your Web sites and applications.
      395,IIS administration.config,Apps,Windows/System32/inetsrv/config/administration.config,lazy_ntfs,This configuration file stores the settings for IIS management.
      396,IIS redirection.config,Apps,Windows/System32/inetsrv/config/redirection.config,lazy_ntfs,This configuration file contains the settings that indicate the location where the centralized configuration files are stored.
      397,web.config,Apps,inetpub/wwwroot/**10/web.config,lazy_ntfs,The web.config is a file that is read by IIS and the ASP.NET Core Module to configure an app hosted with IIS.
      398,IIS log files,Logs,Windows/System32/LogFiles/W3SVC*/*.log,lazy_ntfs,
      399,IIS log files,Logs,Windows.old/Windows/System32/LogFiles/W3SVC*/*.log,lazy_ntfs,
      400,IIS log files,Logs,inetpub/logs/LogFiles/*.log,lazy_ntfs,
      401,IIS log files,Logs,inetpub/logs/LogFiles/W3SVC*/*.log,lazy_ntfs,
      402,IIS log files,Logs,Resources/Directory/*/LogFiles/Web/W3SVC*/*.log,lazy_ntfs,
      403,IIS log files,Logs,Windows/system32/LogFiles/HTTPERR/*.log,lazy_ntfs,
      404,ISLOnline Logs - Sessions - *.out,Communications,Users/*/AppData/Local/ISL Online Cache/ISL Light Client/*/ISLClient.out,lazy_ntfs,Collects client session logs for one or more sessions
      405,ISLOnline Logs - Session Configurations,Communications,Users/*/AppData/Local/ISL Online Cache/ISL Light Client/*/conf/*,lazy_ntfs,Configurations for ISL Light sessions
      406,ISL AlwaysOn Logs - Sessions List,Communications,Program Files (x86)/ISL Online/ISL AlwaysOn/session.xml,lazy_ntfs,Collects an xml file listing all sessions for ISL AlwaysOn (Unattended Access)
      407,ISL AlwaysOn Logs - Sessions,Communications,Program Files (x86)/ISL Online/ISL AlwaysOn/sessions/*/trace.out,lazy_ntfs,Detailed log for each session for ISL AlwaysOn (Unattended Access)
      408,ISL AlwaysOn - App Logs,Communications,Program Files (x86)/ISL Online/ISL AlwaysOn/*.out,lazy_ntfs,Application logs containg various artifacts.
      409,ISL Light Logs - Sessions,Communications,Users/*/AppData/Local/ISL Online Cache/ISL Light/*/trace.out,lazy_ntfs,Collects client session logs for one or more sessions
      410,ISL AlwaysOn - Email Configuration,Communications,Program Files (x86)/ISL Online/ISL AlwaysOn/status/tray,lazy_ntfs,This file includes the email of the logged in user for ISL AlwaysOn (Unattended Access)
      411,ISL AlwaysOn - Configuration,Communications,Program Files (x86)/ISL Online/ISL AlwaysOn/StaticConfiguration.ini,lazy_ntfs,"Configuration information (port, http/htpps) for ISL AlwaysOn (Unattended Access)"
      412,IceChat Chat Logs,Communications,Users/*/AppData/Local/IceChat Networks/IceChat/Logs/**10,lazy_ntfs,
      413,Idrive Cleanup Operations,Apps,ProgramData/IDrive/IBCOMMON/*/Session/Archive Cleanup/**10/*,lazy_ntfs,Contains individual log files for each archive cleanup operation
      414,Idrive Backup Operations,Apps,ProgramData/IDrive/IBCOMMON/*/Session/Backup/**10/*,lazy_ntfs,Contains individual log files for each backup operation
      415,Idrive Delete Operations,Apps,ProgramData/IDrive/IBCOMMON/*/Session/Delete/**10/*,lazy_ntfs,Contains individual log files for each delete operation
      416,Idrive Restore Operations,Apps,ProgramData/IDrive/IBCOMMON/*/Session/Restore/*,lazy_ntfs,Contains individual log files for each restore operation
      417,Idrive Backup Summary,Apps,ProgramData/IDrive/IBCOMMON/*/Session/LOGXML/*xml,lazy_ntfs,Contains summary of each backup session
      418,Idrive Tracefile,Apps,ProgramData/IDrive/IBCOMMON/*/Tracefile.txt/Tracefile.txt,lazy_ntfs,Application log which includes error logs for failed uploads
      419,Idrive Mapped Drives,Apps,ProgramData/IDrive/IBCOMMON/IDMappedDrives.txt,lazy_ntfs,List of mapped drives for backup
      420,Idrive Backup Schedule,Apps,ProgramData/IDrive/IBCOMMON/schedule.xml,lazy_ntfs,Backup schedule configurations
      421,Idrive Schedule History,Apps,ProgramData/IDrive/IBCOMMON/Sch_Trace.txt,lazy_ntfs,History of schedule configurations
      422,Idrive Configuration,Apps,ProgramData/IDrive/IBCOMMON/idrive.ini,lazy_ntfs,List of Idrive configuration options
      423,Idrive Local Drives,Apps,ProgramData/IDrive/IBCOMMON/get_Alldrives.txt,lazy_ntfs,List of all local drives
      424,Idrive Exclusion Configurations,Apps,ProgramData/IDrive/IBCOMMON/Exclude*,lazy_ntfs,Files pertaining to exclusion configurations
      425,Idrive User Details,Apps,ProgramData/IDrive/IBCOMMON/AutoComp.ini,lazy_ntfs,"Idrive username, Scheduler notification emails, local username"
      426,Idrive SQL Databse,Apps,ProgramData/IDrive/IBCOMMON/*/LDBNEW/*/*.ibds,lazy_ntfs,Sql database of local files that are backed up
      427,ImgBurn - Application Log File,Apps,Users/*/AppData/Roaming/ImgBurn/Log Files/ImgBurn.log,lazy_ntfs,Contains the ImgBurn application log file.
      428,Index.dat History,Communications,Documents and Settings/*/Local Settings/History/History.IE5/index.dat,lazy_ntfs,
      429,Index.dat History subdirectory,Communications,Documents and Settings/*/Local Settings/History/History.IE5/*/index.dat,lazy_ntfs,
      430,Index.dat cookies,Communications,Documents and Settings/*/Cookies/index.dat,lazy_ntfs,
      431,Index.dat UserData,Communications,Documents and Settings/*/Application Data/Microsoft/Internet Explorer/UserData/index.dat,lazy_ntfs,
      432,Index.dat Office XP,Communications,Documents and Settings/*/Application Data/Microsoft/Office/Recent/index.dat,lazy_ntfs,
      433,Index.dat Office,Communications,Users/*/AppData/Roaming/Microsoft/Office/Recent/index.dat,lazy_ntfs,
      434,Local Internet Explorer folder,Communications,Users/*/AppData/Local/Microsoft/Internet Explorer/**10,lazy_ntfs,
      435,Roaming Internet Explorer folder,Communications,Users/*/AppData/Roaming/Microsoft/Internet Explorer/**10,lazy_ntfs,
      436,IE 9/10 History,Communications,Users/*/AppData/Local/Microsoft/Windows/History/**10,lazy_ntfs,
      437,IE 9/10 Cookies,Communications,Users/*/AppData/Local/Microsoft/Windows/Cookies/**10,lazy_ntfs,
      438,IE 9/10 Download History,Communications,Users/*/AppData/Local/Microsoft/Windows/IEDownloadHistory/**10,lazy_ntfs,
      439,IE 11 Metadata,Communications,Users/*/AppData/Local/Microsoft/Windows/WebCache/*,lazy_ntfs,
      440,IE 11 Cookies,Communications,Users/*/AppData/Local/Microsoft/Windows/INetCookies/**10,lazy_ntfs,
      441,IrfanView Configuration File,FileKnowledge,Users/*/AppData/Roaming/IrfanView/i_view32.ini,lazy_ntfs,
      442,JDownloader 2.0 Download Lists,App,Users/*/AppData/Local/JDownloader 2.0/cfg/**10/downloadList*.zip,lazy_ntfs,"Zip folder which contains several files (00,00_00 and extraInfo) which list the download folder, the time it was created, the name of the download, origin URL, referral URL and more"
      443,JDownloader 2.0 Link Collector,App,Users/*/AppData/Local/JDownloader 2.0/cfg/**10/linkcollector*.zip,lazy_ntfs,"Zip folder which contains several files (0X,0X_00 and extraInfo) which list the websites crawled for links, the referral URLs, timestamps and more"
      444,JDownloader 2.0 General Settings,App,Users/*/AppData/Local/JDownloader 2.0/cfg/**10/org.jdownloader.settings.GeneralSettings.json,lazy_ntfs,General user config for JDownloader 2.0. Holds default download folder.
      445,JDownloader 2.0 Link Grabber Settings,App,Users/*/AppData/Local/JDownloader 2.0/cfg/**10/org.jdownloader.gui.views.linkgrabber.addlinksdialog.LinkgrabberSettings.json,lazy_ntfs,Linkgrabber Settings for JDownloader 2.0. Holds latest download destination folder.
      446,JDownloader 2.0 Proxy Settings,App,Users/*/AppData/Local/JDownloader 2.0/cfg/**10/org.jdownloader.settings.InternetConnectionSettings.customproxylist.json,lazy_ntfs,Proxy configuration for JDownloader 2.0
      447,Java WebStart Cache User Level - Default,Communication,Users/*/AppData/Local/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      448,Java WebStart Cache User Level - IE Protected Mode,Communication,Users/*/AppData/LocalLow/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      449,Java WebStart Cache System level,Communication,Windows/System32/config/systemprofile/AppData/Local/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      450,Java WebStart Cache System level,Communication,Windows.old/Windows/System32/config/systemprofile/AppData/Local/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      451,Java WebStart Cache System level - IE Protected Mode,Communication,Windows/System32/config/systemprofile/AppData/LocalLow/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      452,Java WebStart Cache System level - IE Protected Mode,Communication,Windows.old/Windows/System32/config/systemprofile/AppData/LocalLow/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      453,Java WebStart Cache System level (SysWow64),Communication,Windows/SysWOW64/config/systemprofile/AppData/Local/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      454,Java WebStart Cache System level (SysWow64),Communication,Windows.old/Windows/SysWOW64/config/systemprofile/AppData/Local/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      455,Java WebStart Cache System level (SysWow64) - IE Protected Mode,Communication,Windows/SysWOW64/config/systemprofile/AppData/LocalLow/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      456,Java WebStart Cache System level (SysWow64) - IE Protected Mode,Communication,Windows.old/Windows/SysWOW64/config/systemprofile/AppData/LocalLow/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      457,Java WebStart Cache User Level - XP,Communications,Documents and Settings/*/Application Data/Sun/Java/Deployment/cache/*/*/*.idx,lazy_ntfs,
      458,Kali WSL /etc/debian_version,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/debian_version,lazy_ntfs,
      459,Kali WSL /etc/fstab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/fstab,lazy_ntfs,
      460,Kali WSL /etc/os-release,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/os-release,lazy_ntfs,
      461,Kali WSL /etc/passwd,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/passwd,lazy_ntfs,
      462,Kali WSL /etc/group,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/group,lazy_ntfs,
      463,Kali WSL /etc/shadow,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/shadow,lazy_ntfs,
      464,Kali WSL /etc/timezone,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/timezone,lazy_ntfs,
      465,Kali WSL /etc/hostname,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/hostname,lazy_ntfs,
      466,Kali WSL /etc/hosts,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/hosts,lazy_ntfs,
      467,Kali WSL /etc/crontab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/crontab,lazy_ntfs,
      468,Kali WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/bash.bashrc,lazy_ntfs,
      469,Kali WSL /etc/profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/etc/profile,lazy_ntfs,
      470,Kali WSL .bash_history,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/**10/.bash_history,lazy_ntfs,
      471,Kali WSL .bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/**10/.bashrc,lazy_ntfs,
      472,Kali WSL .profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/**10/.profile,lazy_ntfs,
      473,Kali WSL User Crontabs,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/var/spool/cron/crontabs/**10,lazy_ntfs,
      474,Kali WSL Apt Logs,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/rootfs/var/log/apt/**10/*.log,lazy_ntfs,
      475,Kali WSL ext4.vhdx,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/KaliLinux.54290C8133FEE_*/LocalState/ext4.vhdx,lazy_ntfs,
      476,Kaseya Live Connect Logs (XP),ApplicationLogs,Documents and Settings/*/Application Data/Kaseya/Log/**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      477,Kaseya Live Connect Logs,ApplicationLogs,Users/*/AppData/Local/Kaseya/Log/KaseyaLiveConnect/**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      478,Kaseya Agent Endpoint Service Logs (XP),ApplicationLogs,Documents and Settings/All Users/Application Data/Kaseya/Log/Endpoint/**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      479,Kaseya Agent Endpoint Service Logs,ApplicationLogs,ProgramData/Kaseya/Log/Endpoint/**10,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      480,Kaseya Agent Service Log,ApplicationLogs,Program Files*/Kaseya/*/agentmon.log*,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229009708-Live-Connect-Log-File-Locations
      481,Kaseya Setup Log,ApplicationLogs,Users/*/AppData/Local/Temp/KASetup.log,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229011448
      482,Kaseya Setup Log,ApplicationLogs,Windows/Temp/KASetup.log,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229011448
      483,Kaseya Setup Log,ApplicationLogs,Windows.old/Windows/Temp/KASetup.log,lazy_ntfs,https://helpdesk.kaseya.com/hc/en-gb/articles/229011448
      484,Kaseya Agent Edge Service Logs,ApplicationLogs,ProgramData/Kaseya/Log/KaseyaEdgeServices/**10,lazy_ntfs,https://www.huntress.com/blog/rapid-response-kaseya-vsa-mass-msp-ransomware-incident
      485,Keepass User Config,App,Users/*/AppData/Roaming/KeePass/*.xml,lazy_ntfs,Collecting Keepass User Configuration File
      486,Keepass Config Xml,App,Program Files/KeePass Password Safe*/*.xml,lazy_ntfs,Collecting Keepass Configuration File
      487,Keepass Application Details,App,Program Files/KeePass Password Safe*/*.config,lazy_ntfs,Collecting Keepass Application Details
      488,Keepass Local Ini,App,Users/*/AppData/Local/KeePassXC/*.ini,lazy_ntfs,
      489,Keepass Roaming Ini,App,Users/*/AppData/Roaming/KeePassXC/*.ini,lazy_ntfs,
      490,LNK Files from Recent,LNKFiles,Users/*/AppData/Roaming/Microsoft/Windows/Recent/**10,lazy_ntfs,Also includes automatic and custom jumplist directories
      491,LNK Files from Microsoft Office Recent,LNKFiles,Users/*/AppData/Roaming/Microsoft/Office/Recent/**10,lazy_ntfs,
      492,Start Menu LNK Files,LNKFiles,Users/*/AppData/Roaming/Microsoft/Windows/Start Menu/Programs/*.LNK,lazy_ntfs,
      493,LNK Files from Recent (XP),LNKFiles,Documents and Settings/*/Recent/**10,lazy_ntfs,
      494,Desktop LNK Files XP,LNKFiles,Documents and Settings/*/Desktop/*.LNK,lazy_ntfs,
      495,Desktop LNK Files,LNKFiles,Users/*/Desktop/*.LNK,lazy_ntfs,
      496,Restore point LNK Files XP,LNKFiles,System Volume Information/_restore*/RP*/*.LNK,lazy_ntfs,
      497,LNK Files from C:\ProgramData,LNKFiles,ProgramData/Microsoft/Windows/Start Menu/Programs/*.LNK,lazy_ntfs,
      498,Level RMM Client Application logs,ApplicationLogs,Program Files/Level/*.log,lazy_ntfs,Contains Application Log entries such as service start and incoming connections.
      499,.bash_history,Windows Linux Profile,Users/*/AppData/Local/Packages/*/LocalState/rootfs/home/*/.bash_history,lazy_ntfs,
      500,.bash_logout,Windows Linux Profile,Users/*/AppData/Local/Packages/*/LocalState/rootfs/home/*/.bash_logout,lazy_ntfs,
      501,.bashrc,Windows Linux Profile,Users/*/AppData/Local/Packages/*/LocalState/rootfs/home/*/.bashrc,lazy_ntfs,
      502,.profile,Windows Linux Profile,Users/*/AppData/Local/Packages/*/LocalState/rootfs/home/*/.profile,lazy_ntfs,
      503,User Files - Desktop,LiveUserFiles,Users/*/Desktop/**10,lazy_ntfs,
      504,User Files - Documents,LiveUserFiles,Users/*/Documents/**10,lazy_ntfs,
      505,User Files - Downloads,LiveUserFiles,Users/*/Downloads/**10,lazy_ntfs,
      506,User Files - Dropbox,LiveUserFiles,Users/*/Dropbox*/**10,lazy_ntfs,
      507,LogFiles,Logs,Windows/System32/LogFiles/**10,lazy_ntfs,
      508,LogFiles,Logs,Windows.old/Windows/System32/LogFiles/**10,lazy_ntfs,
      509,Error logging,Misc,windows/PFRO.log,lazy_ntfs,
      510,LogMeIn ProgramData Logs,ApplicationLogs,ProgramData/LogMeIn/Logs/**10,lazy_ntfs,
      511,LogMeIn Application Logs,ApplicationLogs,Users/*/AppData/Local/temp/LogMeInLogs/**10,lazy_ntfs,"Contains RemoteAssist (formerly GoToAssist), GoToMeeting, and other GoTo* logs"
      512,MOF files,WMI,**10/*.MOF,lazy_ntfs,
      513,MS SQL Errorlog,SQL Exploitation,Program Files/Microsoft SQL Server/*/MSSQL/LOG/ERRORLOG,lazy_ntfs,
      514,MS SQL Errorlogs,SQL Exploitation,Program Files/Microsoft SQL Server/*/MSSQL/LOG/ERRORLOG.*,lazy_ntfs,
      515,Macrium Reflect,Apps,ProgramData/Macrium/Macrium Service/*,lazy_ntfs,Copies out all log files
      516,Macrium Reflect,Apps,ProgramData/Macrium/Reflect/*,lazy_ntfs,Copies out the Reflect folder which contains many important logs
      517,Macrium Reflect,Apps,ProgramData/Macrium/Reflect Launcher,lazy_ntfs,Copies out the Reflect folder which contains many important logs
      518,MalwareBytes Anti-Malware Logs,Antivirus,ProgramData/Malwarebytes/Malwarebytes Anti-Malware/Logs/mbam-log-*.xml,lazy_ntfs,
      519,MalwareBytes Anti-Malware Service Logs,Antivirus,ProgramData/Malwarebytes/MBAMService/logs/mbamservice.log*,lazy_ntfs,
      520,MalwareBytes Anti-Malware Scan Logs,Antivirus,Users/*/AppData/Roaming/Malwarebytes/Malwarebytes Anti-Malware/Logs/**10,lazy_ntfs,
      521,MalwareBytes Anti-Malware Scan Results Logs,Antivirus,ProgramData/Malwarebytes/MBAMService/ScanResults/**10,lazy_ntfs,
      522,ManageEngine Desktop Central Log Files,Logs,ManageEngine/DesktopCentral_Server/logs/**10,lazy_ntfs,
      523,ManageEngine ADSelfService Plus Log Files,Logs,ManageEngine/ADSelfService Plus/logs/**10,lazy_ntfs,
      524,Mattermost - Chat Logs,Apps,Users/*/AppData/Roaming/Mattermost/IndexedDB/**10,lazy_ntfs,Locates Mattermost logs and copies them
      525,McAfee Desktop Protection Logs XP,Antivirus,Users/All Users/Application Data/McAfee/DesktopProtection/**10,lazy_ntfs,
      526,McAfee Desktop Protection Logs,Antivirus,ProgramData/McAfee/DesktopProtection/**10,lazy_ntfs,
      527,McAfee Endpoint Security Logs,Antivirus,ProgramData/McAfee/Endpoint Security/Logs/**10,lazy_ntfs,
      528,McAfee Endpoint Security Logs,Antivirus,ProgramData/McAfee/Endpoint Security/Logs_Old/**10,lazy_ntfs,
      529,McAfee VirusScan Logs,Antivirus,ProgramData/Mcafee/VirusScan/**10,lazy_ntfs,
      530,McAfee ePO Logs,Antivirus,ProgramData/McAfee/Endpoint Security/Logs/**10,lazy_ntfs,
      531,MediaMonkey - Media SQLite Database,Apps,Users/*/AppData/Roaming/MediaMonkey/MM.DB,lazy_ntfs,Locates SQLite DB that contains a complete enumeration of the user's media collection within MediaMonkey
      532,MediaMonkey - MediaMonkey.ini,Apps,Users/*/AppData/Roaming/MediaMonkey/MediaMonkey.ini,lazy_ntfs,Locates .ini file which contains information about the user's MediaMonkey application instance
      533,MegaSync Folder,ApplicationLogs,Users/*/AppData/Local/Mega Limited/MEGAsync/**10,lazy_ntfs,
      534,hiberfil.sys,Memory,hiberfil.sys,lazy_ntfs,
      535,pagefile.sys,Memory,pagefile.sys,lazy_ntfs,
      536,swapfile.sys,Memory,swapfile.sys,lazy_ntfs,
      537,Small Memory Dump directory,Memory,Windows/Minidump/*.dmp,lazy_ntfs,https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/small-memory-dump
      538,Small Memory Dump directory,Memory,Windows.old/Windows/Minidump/*.dmp,lazy_ntfs,https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/small-memory-dump
      539,Microsoft Office Backstage,FileKnowledge,Users/*/AppData/Local/Microsoft/Office/*/BackstageinAppNavCache/**10,lazy_ntfs,
      540,Microsoft OneNote - FullTextSearchIndex,Apps,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/*/FullTextSearchIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's text content
      541,Microsoft OneNote - RecentNotebooks_SeenURLs,Apps,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/Notifications/RecentNotebooks_SeenURLs,lazy_ntfs,Grabs a file that appears to record recently seen OneNote notebooks
      542,Microsoft OneNote - AccessibilityCheckerIndex,Apps,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/16.0/AccessibilityCheckerIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's version sync error history
      543,Microsoft OneNote - User NoteTags,Apps,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/16.0/NoteTags/*LiveId.db,lazy_ntfs,Grabs a database that stores the user specified tags within OneNote to be used application-wide
      544,Microsoft OneNote - RecentSearches,Apps,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/16.0/RecentSearches/RecentSearches.db,lazy_ntfs,Grabs a database that stores the user's recent searches within OneNote
      545,"Microsoft Sticky Notes - Windows 7, 8, and 10 version 1511 and earlier",Apps,Users/*/AppData/Roaming/Microsoft/StickyNotes/StickyNotes.snt,lazy_ntfs,
      546,Microsoft Sticky Notes - 1607 and later,Apps,Users/*/AppData/Local/Packages/Microsoft.MicrosoftStickyNotes*/LocalState/plum.sqlite*,lazy_ntfs,
      547,Microsoft Teams IndexedDB Cache,Apps,Users/*/AppData/Roaming/Microsoft/Teams/IndexedDB/https_teams.microsoft.com_0.indexeddb.leveldb/**10,lazy_ntfs,"LevelDB database which can contain inbound/outbound chat messages, call history and more"
      548,Microsoft Teams Local Storage Cache,Apps,Users/*/AppData/Roaming/Microsoft/Teams/Local Storage/leveldb/**10,lazy_ntfs,"LevelDB database which can contain meeting history, file transfer logs and more"
      549,Microsoft Teams Cache,Apps,Users/*/AppData/Roaming/Microsoft/Teams/Cache/**10,lazy_ntfs,Chromium cache which can be viewed with Nirsoft's ChromeCacheView
      550,Microsoft Teams Config,Apps,Users/*/AppData/Roaming/Microsoft/Teams/desktop-config.json,lazy_ntfs,JSON config file for Teams
      551,Microsoft Teams Logs (Windows 11),Apps,Users/%User%/AppData/Local/Packages/MicrosoftTeams_8wekyb3d8bbwe/LocalCache/Microsoft/MSTeams/Logs,lazy_ntfs,Lots of log files for MS Teams
      552,Microsoft To Do - SQLite Database of To Do tasks,Apps,Users/*/AppData/Local/Packages/Microsoft.Todos_8wekyb3d8bbwe/LocalState/AccountsRoot/*/todosqlite.db*,lazy_ntfs,
      553,Microsoft To Do - User Avatar,Apps,Users/*/AppData/Local/Packages/Microsoft.Todos_8wekyb3d8bbwe/LocalState/AccountsRoot/4c444a17ebb042fb92df97d00d1c802a/avatars/UserAvatar.jpg,lazy_ntfs,
      554,Midnight Commander -- All Configuation Files,Apps,Users/*/Midnight Commander/*,lazy_ntfs,Locates folder where all configuration files reside
      555,Multi Commander - Application Folder,Apps,Users/*/AppData/Local/MultiCommander*/**10,lazy_ntfs,Locates the contents of the Application folder.
      556,Multi Commander - Config Folder,Apps,Users/*/AppData/Roaming/MultiCommander*/Config/**10,lazy_ntfs,Locates the contents of the Config folder.
      557,Multi Commander - Log Folder,Apps,Users/*/AppData/Roaming/MultiCommander*/Logs/**10,lazy_ntfs,Locates log file(s) related to user activity within Multi Commander.
      558,Multi Commander - UserData Folder,Apps,Users/*/AppData/Roaming/MultiCommander*/UserData/**10,lazy_ntfs,Locates the contents of the UserData folder.
      559,Multi Commander - Log File,Apps,Users/*/AppData/Roaming/MultiCommander*/**10/*MultiCommander.log,lazy_ntfs,Locates log file(s) associated with Milti Commander. Commonly in YYYY-MM-DD (numbers)-MultiCommander.log naming convention.
      560,.NET CLR UsageLogs (user-scoped),.NET CLR UsageLogs,Users/*/AppData/Local/Microsoft/CLR_*/**10/*.log,lazy_ntfs,
      561,.NET CLR UsageLogs (system-scoped),.NET CLR UsageLogs,Windows*/System32/config/systemprofile/AppData/Local/Microsoft/CLR_*/**10/*.log,lazy_ntfs,
      562,NGINX Log Files,Logs,nginx/logs/*.log,lazy_ntfs,
      563,Usenet Clients - NZBGet Log File,FileDownload,ProgramData/NZBGet/nzbget.log,lazy_ntfs,Locates NZBGet download log file
      564,Usenet Clients - NZBGet NZBs,FileDownload,ProgramData/NZBGet/nzb/*,lazy_ntfs,Locates NZBGet NZB files that were used by the user
      565,Nessus Logs,Nessus,ProgramData/Tenable/Nessus/conf/**10,lazy_ntfs,
      566,Nessus Logs,Nessus Logs,ProgramData/Tenable/Nessus/nessus/logs/**10,lazy_ntfs,
      567,Net Monitor Server Logs,ApplicationLogs,ProgramData/Net Monitor for Employees Pro/log/*/**10,lazy_ntfs,Contains Net Monitor server logs
      568,Net Monitor Server Data,Communication,ProgramData/Net Monitor for Employees Pro/data/**10,lazy_ntfs,Contains Net Monitor server data - Indicates what have been seen as the attacker
      569,Net Monitor Server Config,Apps,ProgramData/Net Monitor for Employees Pro/config/**10,lazy_ntfs,Contains Net Monitor server config
      570,Net Monitor Server Temp Folder,Apps,ProgramData/Net Monitor for Employees Pro/tmp/**10,lazy_ntfs,
      571,Net Monitor Client Logs,ApplicationLogs,Program Files*/Net Monitor for Employees Pro/log/**10,lazy_ntfs,Contains Net Monitor client logs
      572,Net Monitor Client Config,ApplicationLogs,Program Files*/Net Monitor for Employees Pro/config/**10,lazy_ntfs,Contains Net Monitor client config
      573,Usenet Clients - Newsbin Pro,FileDownload,Users/*/AppData/Local/Newsbin/Downloaded.db3,lazy_ntfs,Locates Newsbin Pro download log database
      574,Usenet Clients - Newsleecher,FileDownload,Users/*/AppData/Roaming/NewsLeecher/downloaded.dat,lazy_ntfs,Locates Newsleecher download .dat file
      575,Nicotine++ Logs,FileDownload,Users/%User%/AppData/Roaming/nicotine/logs/**10,lazy_ntfs,"Locates Nicotine++ chat logs, room logs, transfer logs, and debug logs (if enabled)"
      576,Nicotine++ Incomplete Downloads,FileDownload,Users/%User%/AppData/Roaming/nicotine/incomplete/**10,lazy_ntfs,Locates files that did not finish downloading
      577,Nicotine++ Buddyfiles.db,FileDownload,Users/%User%/AppData/Roaming/nicotine/buddyfiles.db/**10,lazy_ntfs,Locates a DB that appears to include shared files from a user's buddy list
      578,Nicotine++ Buddystreams.db,FileDownload,Users/%User%/AppData/Roaming/nicotine/buddystreams.db/**10,lazy_ntfs,Locates a DB that appears to include shared files from a user's buddy list
      579,Nicotine++ Buddymtimes.db,FileDownload,Users/%User%/AppData/Roaming/nicotine/buddymtimes.db/**10,lazy_ntfs,"Locates a DB that appears to enumerate which files the user is sharing to their buddy list, from a folder level"
      580,Nicotine++ Buddyfileindex.db,FileDownload,Users/%User%/AppData/Roaming/nicotine/buddyfileindex.db/**10,lazy_ntfs,"Locates a DB that appears to enumerate which files the user is sharing to their buddy list, from a file level"
      581,Nicotine++ Buddywordindex.db,FileDownload,Users/%User%/AppData/Roaming/nicotine/buddywordindex.db/**10,lazy_ntfs,Unknown what this is for at this time
      582,Nicotine++ Config Files,FileDownload,Users/%User%/AppData/Roaming/nicotine/config/**10,lazy_ntfs,Locates config files
      583,Nicotine++ User Shares,FileDownload,Users/%User%/AppData/Roaming/nicotine/usershares/**10,lazy_ntfs,Locates a DB that appears to store a list of files per user that they are sharing within Nicotine++. Note: this requires the user to right-click -&gt; browse files shared by that user
      584,Nicotine++ Downloads.json,FileDownload,Users/%User%/AppData/Roaming/nicotine/downloads.json*,lazy_ntfs,Locates downloads.json
      585,Nicotine++ Uploads.json,FileDownload,Users/%User%/AppData/Roaming/nicotine/uploads.json*,lazy_ntfs,Locates uploads.json
      586,Notepad++ Unsaved Edits,Text Editor,Users/*/AppData/Roaming/Notepad++/backup/**10,lazy_ntfs,Locates non-saved Notepad++ files and copies them.
      587,Notepad++ Config,Text Editor,Users/*/AppData/Roaming/Notepad++/config.xml,lazy_ntfs,"Retrieves config.xml which contains recently searched terms, replaced terms and recently opened documents"
      588,Notepad++ Session,Text Editor,Users/*/AppData/Roaming/Notepad++/session.xml,lazy_ntfs,Retrieves session.xml which contains session date
      589,Notepad Session Files,Windows Notepad,Users/*/AppData/Local/Packages/Microsoft.WindowsNotepad_8wekyb3d8bbwe/LocalState/TabState/*.bin,lazy_ntfs,Contains .bin files which consist of the files opened in each tab in Windows Notepad
      590,Notion Local Storage,App,Users/*/AppData/Roaming/Notion/notion.db,lazy_ntfs,"Local storage file containing all pages, databases, users, etc."
      591,Notion Custom Dictionary,App,Users/*/AppData/Roaming/Notion/Partitions/notion/Custom Dictionary.txt,lazy_ntfs,
      592,Word Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/Word/**10,lazy_ntfs,
      593,Excel Autosave Location,ApplicationCompatibility,Users/*/AppData/Roaming/Microsoft/Excel/**10,lazy_ntfs,
      594,Powerpoint Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/Powerpoint/**10,lazy_ntfs,
      595,Publisher Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/Publisher/**10,lazy_ntfs,
      596,Office Diagnostics,Execution,Users/*/AppData/Local/Diagnostics/PCW.debugreport.xml,lazy_ntfs,Payloads for CVE-2022-30190 ('Follina') will be in this log
      597,Office Elevated Diagnostics,Execution,Users/*/AppData/Local/ElevatedDiagnostics/PCW.debugreport.xml,lazy_ntfs,Payloads for CVE-2022-30190 ('Follina') will be in this log
      598,Office Document Cache,FileKnowledge,Users/*/AppData/Local/Microsoft/Office/*/OfficeFileCache/**10,lazy_ntfs,
      599,One Commander - All Configuration Files,Apps,Users/*/OneCommander/*,lazy_ntfs,Locates folder where all configuration files reside
      600,One Commander - Other Configuration Files,Apps,Users/*/AppData/Local/Apps/2.0/*/*/onec*/**10,lazy_ntfs,Locates folder where all configuration files reside
      601,OneDrive Metadata Logs,Apps,Users/*/AppData/Local/Microsoft/OneDrive/logs/**10,lazy_ntfs,
      602,OneDrive Metadata Settings,Apps,Users/*/AppData/Local/Microsoft/OneDrive/settings/**10,lazy_ntfs,
      603,OneDrive User Files,Apps,Users/*/OneDrive*/**10,lazy_ntfs,Caution -- This target will collect OneDrive contents from the local drive AND on-demand cloud files. Ensure your scope of authority permits cloud collections before use or isolate system from network.
      604,OpenSSH Config File,Apps,Users/*/.ssh/config,lazy_ntfs,"Config file can hold usernames, IP addresses and ports, key locations and configured shortcuts for servers e.g. ssh web-server"
      605,OpenSSH Known Hosts,Apps,Users/*/.ssh/known_hosts,lazy_ntfs,"Known hosts file can hold a list of connected FQDNs/IP Addresses and ports if they are non-default, as well as public key fingerprints"
      606,OpenSSH Public Keys,Apps,Users/*/.ssh/*.pub,lazy_ntfs,"Gets all public keys (*.pub). It is more difficult to find private keys as they typically do not have a file extension. However, the .pub files should be able to help find the private keys as they are typically named the same."
      607,OpenSSH Default RSA Private Key,Apps,Users/*/.ssh/id_rsa,lazy_ntfs,Default name for an auto-generated SSH RSA private key
      608,OpenSSH Default ECDSA Private Key,Apps,Users/*/.ssh/id_ecdsa,lazy_ntfs,Default name for an auto-generated SSH ECDSA private key
      609,OpenSSH Default ECDSA-SK Private Key,Apps,Users/*/.ssh/id_ecdsa_sk,lazy_ntfs,Default name for an auto-generated SSH ECDSA private key using a Security Key
      610,OpenSSH Default ED25519 Private Key,Apps,Users/*/.ssh/id_ed25519,lazy_ntfs,Default name for an auto-generated SSH ED25519 private key
      611,OpenSSH Default ED25519-SK Private Key,Apps,Users/*/.ssh/id_ed25519_sk,lazy_ntfs,Default name for an auto-generated SSH ED25519 private key using a Security Key
      612,OpenSSH Default DSA Private Key,Apps,Users/*/.ssh/id_dsa,lazy_ntfs,Default name for an auto-generated SSH DSA private key
      613,OpenSSH Server Config File,Apps,ProgramData/ssh/sshd_config,lazy_ntfs,Config file can hold information on allowed/denied users
      614,OpenSSH Server Logs,Apps,ProgramData/ssh/logs/*,lazy_ntfs,OpenSSH server logs
      615,OpenSSH Host ECDSA Key,Apps,ProgramData/ssh/ssh_host_ecdsa_key,lazy_ntfs,Retrieves the host ECDSA key
      616,OpenSSH Host ED25519 Key,Apps,ProgramData/ssh/ssh_host_ed25519_key,lazy_ntfs,Retrieves the host ED25519 key
      617,OpenSSH Host DSA Key,Apps,ProgramData/ssh/ssh_host_dsa_key,lazy_ntfs,Retrieves the host DSA key
      618,OpenSSH Host RSA Key,Apps,ProgramData/ssh/ssh_host_rsa_key,lazy_ntfs,Retrieves the host RSA key
      619,OpenSSH User Authorized Keys,Apps,Users/*/.ssh/authorized_keys,lazy_ntfs,Retrieves the user's authorised public keys
      620,OpenSSH User Authorized Keys 2,Apps,Users/*/.ssh/authorized_keys2,lazy_ntfs,Retrieves the user's authorised public keys from the second file
      621,OpenSSH Authorized Administrator Keys,Apps,ProgramData/ssh/administrators_authorized_keys,lazy_ntfs,Retrieves the administrator group's authorised public keys
      622,OpenVPN Client Config,ApplicationLogs,Users/*/OpenVPN/config/**10,lazy_ntfs,Contains OpenVPN Configs (Profiles)
      623,OpenVPN Client Config,ApplicationLogs,Program Files*/OpenVPN/config/**10,lazy_ntfs,Contains OpenVPN Configs(Profiles)
      624,OpenVPN Client Config,ApplicationLogs,Users/*/OpenVPN/log/*.log,lazy_ntfs,Contains OpenVPN Logs for each Config(Profile)
      625,Opera - Local Folder,Communications,Users/*/AppData/Local/Opera Software/Opera Stable/**10,lazy_ntfs,Grabs entire contents of the Opera AppData\Local folder
      626,Opera - Roaming Folder,Communications,Users/*/AppData/Roaming/Opera Software/Opera Stable/**10,lazy_ntfs,Grabs entire contents of the Opera AppData\Roaming folder
      627,PST XP,Communications,Documents and Settings/*/Local Settings/Application Data/Microsoft/Outlook/*.pst,lazy_ntfs,
      628,OST XP,Communications,Documents and Settings/*/Local Settings/Application Data/Microsoft/Outlook/*.ost,lazy_ntfs,
      629,PST (2013 or 2016),Communications,Users/*/Documents/Outlook Files/*.pst,lazy_ntfs,
      630,OST (2013 or 2016),Communications,Users/*/Documents/Outlook Files/*.ost,lazy_ntfs,
      631,PST,Communications,Users/*/AppData/Local/Microsoft/Outlook/*.pst,lazy_ntfs,"Outlook Data File: POP accounts, archives, older installations"
      632,OST,Communications,Users/*/AppData/Local/Microsoft/Outlook/*.ost,lazy_ntfs,"Offline Outlook Data File: M365, Exchange, IMAP"
      633,NST,Communications,Users/*/AppData/Local/Microsoft/Outlook/*.nst,lazy_ntfs,Outlook Group Storage File: Group conversations and calendar
      634,Outlook Attachment Temporary Storage,Communications,Users/*/AppData/Local/Microsoft/Windows/INetCache/Content.Outlook/**10,lazy_ntfs,Outlook temporary storage folder for user attachments
      635,PeaZip Configuration Files,FileKnowledge,Users/*/AppData/Roaming/PeaZip/**10,lazy_ntfs,
      636,Perflogs,Application,PerfLogs/**10,lazy_ntfs,
      637,PowerShell 7 Config JSON,PowerShell,Program Files/PowerShell/7/powershell.config.json,lazy_ntfs,
      638,PowerShell Console Log,PowerShellConsoleLog,Users/*/AppData/Roaming/Microsoft/Windows/PowerShell/PSReadline/*_history.txt,lazy_ntfs,
      639,PowerShell Transcripts - Default Location,PowerShellTranscripts,Users/*/Documents/20*/PowerShell_transcript.*.txt,lazy_ntfs,
      640,PowerShell Transcripts - Observed Location,PowerShellTranscripts,Windows/SysWOW64/*/PowerShell_transcript.*.txt,lazy_ntfs,
      641,PowerShell Transcripts - Observed Location,PowerShellTranscripts,Program Files/Amazon/Ec2ConfigService/Scripts/*/PowerShell_transcript.*.txt,lazy_ntfs,
      642,PowerShell Transcripts - Observed Location,PowerShellTranscripts,Windows/System32/*/PowerShell_transcript.*.txt,lazy_ntfs,
      643,Prefetch,Prefetch,Windows/prefetch/*.pf,lazy_ntfs,
      644,Prefetch,Prefetch,Windows.old/Windows/prefetch/*.pf,lazy_ntfs,
      645,ProgramData,Application Data,ProgramData/**10,lazy_ntfs,
      646,ProtonVPN - Connection Logs,ApplicationLogs,Users/*/AppData/Local/ProtonVPN/Logs,lazy_ntfs,Locates ProtonVPN connection logs.
      647,Puffin - data.db,Communications,Users/*/AppData/Local/PuffinSecureBrowser/data.db,lazy_ntfs,Grabs an important database file that contains browser history
      648,Puffin - Autocomplete Data,Communications,Users/*/AppData/Local/PuffinSecureBrowser/autocompletes.dat,lazy_ntfs,Grabs a file that stores autocomplete data
      649,Puffin - Password Forms Data,Communications,Users/*/AppData/Local/PuffinSecureBrowser/passwordForms.dat,lazy_ntfs,Grabs a file that stores some saved password data
      650,Puffin - Password (Encrypted),Communications,Users/*/AppData/Local/PuffinSecureBrowser/credential.dat,lazy_ntfs,Grabs a file that stores passwords in an encrypted format
      651,Puffin - Subscription Data,Communications,Users/*/AppData/Local/PuffinSecureBrowser/subscription,lazy_ntfs,Grabs a file that stores the user's email address that's associated with their Puffin subscription
      652,Puffin - Cookies,Communications,Users/*/AppData/Local/PuffinSecureBrowser/cookies.dat,lazy_ntfs,Grabs a file that stores information related to cookies
      653,Puffin - Image Cache,Communications,Users/*/AppData/Local/PuffinSecureBrowser/image_cache/**10,lazy_ntfs,Grabs a directory that caches images from websites visited
      654,WNS,WNS,Users/%user/AppData/Local/Microsoft/Windows/Notifications/appdb.dat,lazy_ntfs,
      655,WNS,WNS,Users/%user/AppData/Local/Microsoft/Windows/Notifications/wpndatabase.db,lazy_ntfs,
      656,Q-Dir - .ini File,Apps,Users/*/AppData/Roaming/Q-Dir/Q-Dir.ini,lazy_ntfs,Locates .ini file associated with Q-Dir which stores useful user activity information.
      657,Q-Dir - .qdr file,Apps,Users/*/AppData/Roaming/Q-Dir/start.qdr,lazy_ntfs,"Locates .qdr file associated with Q-Dir which stores useful user activity information, including the last 4 folders opened (encoded, unfortunately)."
      658,QFinderPro,Apps,Users/*/AppData/Local/QNAP/QfinderPro,lazy_ntfs,Locates a JSON file that provides network location information for any QNAP connected devices.
      659,RDP Cache Files,FileSystem,Users/*/AppData/Local/Microsoft/Terminal Server Client/Cache/*,lazy_ntfs,
      660,Windows.old RDP Cache Files,FileSystem,Windows.old/Users/*/AppData/Local/Microsoft/Terminal Server Client/Cache/*,lazy_ntfs,
      661,RDP Cache Files,FileSystem,Documents and Settings/*/Local Settings/Application Data/Microsoft/Terminal Server Client/Cache/*,lazy_ntfs,
      662,RemoteConnectionManager Event Logs,EventLogs,Windows/System32/winevt/logs/Microsoft-Windows-TerminalServices-RemoteConnectionManager*,lazy_ntfs,
      663,RemoteConnectionManager Event Logs,EventLogs,Windows.old/Windows/System32/winevt/logs/Microsoft-Windows-TerminalServices-RemoteConnectionManager*,lazy_ntfs,
      664,LocalSessionManager Event Logs,EventLogs,Windows/System32/winevt/logs/Microsoft-Windows-TerminalServices-LocalSessionManager*,lazy_ntfs,
      665,LocalSessionManager Event Logs,EventLogs,Windows.old/Windows/System32/winevt/logs/Microsoft-Windows-TerminalServices-LocalSessionManager*,lazy_ntfs,
      666,RDPClient Event Logs,EventLogs,Windows/System32/winevt/logs/Microsoft-Windows-TerminalServices-RDPClient*,lazy_ntfs,
      667,RDPClient Event Logs,EventLogs,Windows.old/Windows/System32/winevt/logs/Microsoft-Windows-TerminalServices-RDPClient*,lazy_ntfs,
      668,RDPCoreTS Event Logs,EventLogs,Windows/System32/winevt/logs/Microsoft-Windows-RemoteDesktopServices-RdpCoreTS*,lazy_ntfs,Can be used to correlate RDP logon failures by originating IP
      669,RDPCoreTS Event Logs,EventLogs,Windows.old/Windows/System32/winevt/logs/Microsoft-Windows-RemoteDesktopServices-RdpCoreTS*,lazy_ntfs,Can be used to correlate RDP logon failures by originating IP
      670,Radmin Server 32bit Log,ApplicationLogs,Windows/SysWOW64/rserver30/Radm_log.htm,lazy_ntfs,Contains Application Log entries such as service start and incomming connections.
      671,Radmin Server 64bit Log,ApplicationLogs,Windows/System32/rserver30/Radm_log.htm,lazy_ntfs,Contains Application Log entries such as service start and incomming connections.
      672,Radmin Server 32bit Chats,ApplicationLogs,Windows/SysWOW64/rserver30/CHATLOGS/*/*.htm,lazy_ntfs,Previous chat logs
      673,Radmin Server 64bit Chats,ApplicationLogs,Windows/System32/rserver30/CHATLOGS/*/*.htm,lazy_ntfs,Previous chat logs
      674,Radmin Viewer Chats,ApplicationLogs,Users/*/Documents/ChatLogs/*/*.htm,lazy_ntfs,Previous chat logs
      675,Rclone Config,Apps,**10/rclone.conf,lazy_ntfs,
      676,RecentFileCache,ApplicationCompatability,Windows/AppCompat/Programs/RecentFileCache.bcf,lazy_ntfs,
      677,RecentFileCache,ApplicationCompatability,Windows.old/Windows/AppCompat/Programs/RecentFileCache.bcf,lazy_ntfs,
      678,Recycle Bin - Windows Vista+,FileDeletion,$Recycle.Bin/**10/$R*,lazy_ntfs,
      679,Recycle Bin - Windows Vista+,FileDeletion,$Recycle.Bin/*/$R*/**10,lazy_ntfs,
      680,RECYCLER - WinXP,FileDeletion,RECYCLE*/**10/D*,lazy_ntfs,
      681,Recycle Bin - Windows Vista+,FileDeletion,$Recycle.Bin/**10/$I*,lazy_ntfs,
      682,RECYCLER - WinXP,FileDeletion,RECYCLE*/**10/INFO2,lazy_ntfs,
      683,Registry.dat MSIX Hive,Registry,Users/*/AppData/Local/Packages/*/SystemAppData/Helium/Registry.dat*,lazy_ntfs,
      684,User.dat MSIX Hive,Registry,Users/*/AppData/Local/Packages/*/SystemAppData/Helium/User.dat*,lazy_ntfs,
      685,UserClasses.dat MSIX Hive,Registry,Users/*/AppData/Local/Packages/*/SystemAppData/Helium/UserClasses.dat*,lazy_ntfs,
      686,BBI registry hive,Registry,Windows/System32/config/BBI,lazy_ntfs,
      687,BBI registry hive,Registry,Windows.old/Windows/System32/config/BBI,lazy_ntfs,
      688,BBI registry transaction files,Registry,Windows/System32/config/BBI.LOG*,lazy_ntfs,
      689,BBI registry transaction files,Registry,Windows.old/System32/config/BBI.LOG*,lazy_ntfs,
      690,BCD-Template registry hive,Registry,Windows/System32/config/BCD-Template,lazy_ntfs,
      691,BCD-Template registry hive,Registry,Windows.old/Windows/System32/config/BCD-Template,lazy_ntfs,
      692,BCD-Template registry transaction files,Registry,Windows/System32/config/BCD-Template.LOG*,lazy_ntfs,
      693,BCD-Template registry transaction files,Registry,Windows.old/System32/config/BCD-Template.LOG*,lazy_ntfs,
      694,COMPONENTS registry hive,Registry,Windows/System32/config/COMPONENTS,lazy_ntfs,
      695,COMPONENTS registry hive,Registry,Windows.old/Windows/System32/config/COMPONENTS,lazy_ntfs,
      696,COMPONENTS registry transaction files,Registry,Windows/System32/config/COMPONENTS.LOG*,lazy_ntfs,
      697,COMPONENTS registry transaction files,Registry,Windows.old/System32/config/COMPONENTS.LOG*,lazy_ntfs,
      698,DRIVERS registry hive,Registry,Windows/System32/config/DRIVERS,lazy_ntfs,
      699,DRIVERS registry hive,Registry,Windows.old/Windows/System32/config/DRIVERS,lazy_ntfs,
      700,DRIVERS registry transaction files,Registry,Windows/System32/config/DRIVERS.LOG*,lazy_ntfs,
      701,DRIVERS registry transaction files,Registry,Windows.old/System32/config/DRIVERS.LOG*,lazy_ntfs,
      702,ELAM registry hive,Registry,Windows/System32/config/ELAM,lazy_ntfs,
      703,ELAM registry hive,Registry,Windows.old/Windows/System32/config/ELAM,lazy_ntfs,
      704,ELAM registry transaction files,Registry,Windows/System32/config/ELAM.LOG*,lazy_ntfs,
      705,ELAM registry transaction files,Registry,Windows.old/System32/config/ELAM.LOG*,lazy_ntfs,
      706,userdiff registry hive,Registry,Windows/System32/config/userdiff,lazy_ntfs,
      707,userdiff registry hive,Registry,Windows.old/Windows/System32/config/userdiff,lazy_ntfs,
      708,userdiff registry transaction files,Registry,Windows/System32/config/userdiff.LOG*,lazy_ntfs,
      709,userdiff registry transaction files,Registry,Windows.old/System32/config/userdiff.LOG*,lazy_ntfs,
      710,VSMIDK registry hive,Registry,Windows/System32/config/VSMIDK,lazy_ntfs,
      711,VSMIDK registry hive,Registry,Windows.old/Windows/System32/config/VSMIDK,lazy_ntfs,
      712,VSMIDK registry transaction files,Registry,Windows/System32/config/VSMIDK.LOG*,lazy_ntfs,
      713,VSMIDK registry transaction files,Registry,Windows.old/System32/config/VSMIDK.LOG*,lazy_ntfs,
      714,SAM registry transaction files,Registry,Windows/System32/config/SAM.LOG*,lazy_ntfs,
      715,SAM registry transaction files,Registry,Windows.old/Windows/System32/config/SAM.LOG*,lazy_ntfs,
      716,SECURITY registry transaction files,Registry,Windows/System32/config/SECURITY.LOG*,lazy_ntfs,
      717,SECURITY registry transaction files,Registry,Windows.old/Windows/System32/config/SECURITY.LOG*,lazy_ntfs,
      718,SOFTWARE registry transaction files,Registry,Windows/System32/config/SOFTWARE.LOG*,lazy_ntfs,
      719,SOFTWARE registry transaction files,Registry,Windows.old/Windows/System32/config/SOFTWARE.LOG*,lazy_ntfs,
      720,SYSTEM registry transaction files,Registry,Windows/System32/config/SYSTEM.LOG*,lazy_ntfs,
      721,SYSTEM registry transaction files,Registry,Windows.old/Windows/System32/config/SYSTEM.LOG*,lazy_ntfs,
      722,SAM registry hive,Registry,Windows/System32/config/SAM,lazy_ntfs,
      723,SAM registry hive,Registry,Windows.old/Windows/System32/config/SAM,lazy_ntfs,
      724,SECURITY registry hive,Registry,Windows/System32/config/SECURITY,lazy_ntfs,
      725,SECURITY registry hive,Registry,Windows.old/Windows/System32/config/SECURITY,lazy_ntfs,
      726,SOFTWARE registry hive,Registry,Windows/System32/config/SOFTWARE,lazy_ntfs,
      727,SOFTWARE registry hive,Registry,Windows.old/Windows/System32/config/SOFTWARE,lazy_ntfs,
      728,SYSTEM registry hive,Registry,Windows/System32/config/SYSTEM,lazy_ntfs,
      729,SYSTEM registry hive,Registry,Windows.old/Windows/System32/config/SYSTEM,lazy_ntfs,
      730,RegBack registry transaction files,Registry,Windows/System32/config/RegBack/*.LOG*,lazy_ntfs,
      731,RegBack registry transaction files,Registry,Windows.old/Windows/System32/config/RegBack/*.LOG*,lazy_ntfs,
      732,SAM registry hive (RegBack),Registry,Windows/System32/config/RegBack/SAM,lazy_ntfs,
      733,SAM registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SAM,lazy_ntfs,
      734,SECURITY registry hive (RegBack),Registry,Windows/System32/config/RegBack/SECURITY,lazy_ntfs,
      735,SECURITY registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SECURITY,lazy_ntfs,
      736,SOFTWARE registry hive (RegBack),Registry,Windows/System32/config/RegBack/SOFTWARE,lazy_ntfs,
      737,SOFTWARE registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SOFTWARE,lazy_ntfs,
      738,SYSTEM registry hive (RegBack),Registry,Windows/System32/config/RegBack/SYSTEM,lazy_ntfs,
      739,SYSTEM registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SYSTEM,lazy_ntfs,
      740,SYSTEM registry hive (RegBack),Registry,Windows/System32/config/RegBack/SYSTEM1,lazy_ntfs,
      741,SYSTEM registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SYSTEM1,lazy_ntfs,
      742,System Profile registry hive,Registry,Windows/System32/config/systemprofile/NTUSER.DAT,lazy_ntfs,
      743,System Profile registry hive,Registry,Windows.old/Windows/System32/config/systemprofile/NTUSER.DAT,lazy_ntfs,
      744,System Profile registry transaction files,Registry,Windows/System32/config/systemprofile/NTUSER.DAT.LOG*,lazy_ntfs,
      745,System Profile registry transaction files,Registry,Windows.old/Windows/System32/config/systemprofile/NTUSER.DAT.LOG*,lazy_ntfs,
      746,Local Service registry hive,Registry,Windows/ServiceProfiles/LocalService/NTUSER.DAT,lazy_ntfs,
      747,Local Service registry hive,Registry,Windows.old/Windows/ServiceProfiles/LocalService/NTUSER.DAT,lazy_ntfs,
      748,Local Service registry transaction files,Registry,Windows/ServiceProfiles/LocalService/NTUSER.DAT.LOG*,lazy_ntfs,
      749,Local Service registry transaction files,Registry,Windows.old/Windows/ServiceProfiles/LocalService/NTUSER.DAT.LOG*,lazy_ntfs,
      750,Network Service registry hive,Registry,Windows/ServiceProfiles/NetworkService/NTUSER.DAT,lazy_ntfs,
      751,Network Service registry hive,Registry,Windows.old/Windows/ServiceProfiles/NetworkService/NTUSER.DAT,lazy_ntfs,
      752,Network Service registry transaction files,Registry,Windows/ServiceProfiles/NetworkService/NTUSER.DAT.LOG*,lazy_ntfs,
      753,Network Service registry transaction files,Registry,Windows.old/Windows/ServiceProfiles/NetworkService/NTUSER.DAT.LOG*,lazy_ntfs,
      754,System Restore Points Registry Hives (XP),Registry,System Volume Information/_restore*/RP*/snapshot/_REGISTRY_*,lazy_ntfs,
      755,NTUSER.DAT registry hive XP,Registry,Documents and Settings/*/NTUSER.DAT,lazy_ntfs,
      756,NTUSER.DAT registry hive,Registry,Users/*/NTUSER.DAT,lazy_ntfs,
      757,NTUSER.DAT registry transaction files,Registry,Users/*/NTUSER.DAT.LOG*,lazy_ntfs,
      758,NTUSER.DAT DEFAULT registry hive,Registry,Windows/System32/config/DEFAULT,lazy_ntfs,
      759,NTUSER.DAT DEFAULT registry hive,Registry,Windows.old/Windows/System32/config/DEFAULT,lazy_ntfs,
      760,NTUSER.DAT DEFAULT transaction files,Registry,Windows/System32/config/DEFAULT.LOG*,lazy_ntfs,
      761,NTUSER.DAT DEFAULT transaction files,Registry,Windows.old/Windows/System32/config/DEFAULT.LOG*,lazy_ntfs,
      762,UsrClass.dat registry hive,Registry,Users/*/AppData/Local/Microsoft/Windows/UsrClass.dat,lazy_ntfs,
      763,UsrClass.dat registry transaction files,Registry,Users/*/AppData/Local/Microsoft/Windows/UsrClass.dat.LOG*,lazy_ntfs,
      764,RemoteUtilities Connection Logs,Remote Access,Program Files*/Remote Utilities - Host/Logs/rut_log_*.html,lazy_ntfs,Includes connection log files
      765,RemoteUtilities Install Log,Remote Access,ProgramData/Remote Utilities/install.log,lazy_ntfs,Includes Install log file
      766,NTUSER.DAT registry hive,Registry,**10/NTUSER.DAT,lazy_ntfs,
      767,NTUSER.DAT registry transaction files,Registry,**10/NTUSER.DAT.LOG*,lazy_ntfs,
      768,NTUSER.DAT DEFAULT registry hive,Registry,**10/DEFAULT,lazy_ntfs,
      769,NTUSER.DAT DEFAULT transaction files,Registry,**10/DEFAULT.LOG*,lazy_ntfs,
      770,UsrClass.dat registry hive,Registry,**10/UsrClass.dat,lazy_ntfs,
      771,UsrClass.dat registry transaction files,Registry,**10/UsrClass.dat.LOG*,lazy_ntfs,
      772,LNK Files,LNKFiles,**10/*.LNK,lazy_ntfs,
      773,Word Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/Word/*,lazy_ntfs,
      774,Excel Autosave Location,ApplicationCompatibility,Users/*/AppData/Roaming/Microsoft/Excel/*,lazy_ntfs,
      775,PowerPoint Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/PowerPoint/*,lazy_ntfs,
      776,Publisher Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/Publisher/*,lazy_ntfs,
      777,Publisher Autosave Location,FileKnowledge,Users/*/AppData/Roaming/Microsoft/Word/*,lazy_ntfs,
      778,Office Document Cache,FileKnowledge,Users/*/AppData/Local/Microsoft/Office/*/OfficeFileCache/*,lazy_ntfs,
      779,Office Document Cache,FileKnowledge,Users/*/AppData/Local/Microsoft/Office/*/OfficeFileCache/*,lazy_ntfs,
      780,Chrome bookmarks,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Bookmarks*,lazy_ntfs,
      781,Chrome bookmarks,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Bookmarks*,lazy_ntfs,
      782,Chrome Cookies,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/**10/Cookies*,lazy_ntfs,
      783,Chrome Cookies,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/**10/Cookies*,lazy_ntfs,
      784,Chrome Current Session,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Session,lazy_ntfs,
      785,Chrome Current Session,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Session,lazy_ntfs,
      786,Chrome Current Tabs,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Tabs,lazy_ntfs,
      787,Chrome Current Tabs,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Tabs,lazy_ntfs,
      788,Chrome Download Metadata,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Download Metadata,lazy_ntfs,
      789,Chrome Download Metadata,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Download Metadata,lazy_ntfs,
      790,Chrome Extension Cookies,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Extension Cookies,lazy_ntfs,
      791,Chrome Extension Cookies,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Extension Cookies,lazy_ntfs,
      792,Chrome Favicons,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Favicons*,lazy_ntfs,
      793,Chrome Favicons,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Favicons*,lazy_ntfs,
      794,Chrome History,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/History*,lazy_ntfs,
      795,Chrome History,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/History*,lazy_ntfs,
      796,Chrome Last Session,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Session,lazy_ntfs,
      797,Chrome Last Session,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Session,lazy_ntfs,
      798,Chrome Last Tabs,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Tabs,lazy_ntfs,
      799,Chrome Last Tabs,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Tabs,lazy_ntfs,
      800,Chrome Sessions Folder,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Sessions/*,lazy_ntfs,
      801,Chrome Sessions Folder,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Sessions/*,lazy_ntfs,
      802,Chrome Login Data,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Login Data,lazy_ntfs,
      803,Chrome Login Data,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Login Data,lazy_ntfs,
      804,Chrome Media History,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Media History*,lazy_ntfs,
      805,Chrome Media History,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Media History*,lazy_ntfs,
      806,Chrome Network Action Predictor,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Action Predictor,lazy_ntfs,
      807,Chrome Network Action Predictor,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Action Predictor,lazy_ntfs,
      808,Chrome Network Persistent State,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Persistent State,lazy_ntfs,
      809,Chrome Network Persistent State,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Persistent State,lazy_ntfs,
      810,Chrome Preferences,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Preferences,lazy_ntfs,
      811,Chrome Preferences,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Preferences,lazy_ntfs,
      812,Chrome Quota Manager,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/QuotaManager,lazy_ntfs,
      813,Chrome Quota Manager,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/QuotaManager,lazy_ntfs,
      814,Chrome Reporting and NEL,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Reporting and NEL,lazy_ntfs,
      815,Chrome Reporting and NEL,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Reporting and NEL,lazy_ntfs,
      816,Chrome Shortcuts,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Shortcuts*,lazy_ntfs,
      817,Chrome Shortcuts,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Shortcuts*,lazy_ntfs,
      818,Chrome Top Sites,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Top Sites*,lazy_ntfs,
      819,Chrome Top Sites,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Top Sites*,lazy_ntfs,
      820,Chrome Trust Tokens,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Trust Tokens*,lazy_ntfs,
      821,Chrome Trust Tokens,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Trust Tokens*,lazy_ntfs,
      822,Chrome SyncData Database,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Sync Data/SyncData.sqlite3,lazy_ntfs,
      823,Chrome SyncData Database,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Sync Data/SyncData.sqlite3,lazy_ntfs,
      824,Chrome Visited Links,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Visited Links,lazy_ntfs,
      825,Chrome Visited Links,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Visited Links,lazy_ntfs,
      826,Chrome Web Data,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Web Data*,lazy_ntfs,
      827,Chrome Web Data,Communications,Users/*/AppData/Local/Google/Chrome/User Data/*/Web Data*,lazy_ntfs,
      828,Windows Protect Folder,FileSystem,Users/*/AppData/Roaming/Microsoft/Protect/*/**10,lazy_ntfs,Required for offline decryption
      829,Windows Protect Folder,FileSystem,Users/*/AppData/Roaming/Microsoft/Protect/*/**10,lazy_ntfs,Required for offline decryption
      830,Edge folder,Communications,Users/*/AppData/Local/Packages/Microsoft.MicrosoftEdge_8wekyb3d8bbwe/**10,lazy_ntfs,
      831,Edge folder,Communications,Users/*/AppData/Local/Packages/Microsoft.MicrosoftEdge_8wekyb3d8bbwe/**10,lazy_ntfs,
      832,Amcache,ApplicationCompatibility,**10/Amcache.hve,lazy_ntfs,
      833,Amcache transaction files,ApplicationCompatibility,**10/Amcache.hve.LOG*,lazy_ntfs,
      834,LNK Files from Recent,LNKFiles,Users/*/AppData/Roaming/Microsoft/Windows/Recent/**10,lazy_ntfs,
      835,LNK Files from Recent,LNKFiles,Users/*/AppData/Roaming/Microsoft/Windows/Recent/**10,lazy_ntfs,
      836,LNK Files from Microsoft Office Recent,LNKFiles,Users/*/AppData/Roaming/Microsoft/Office/Recent/**10,lazy_ntfs,
      837,LNK Files from Microsoft Office Recent,LNKFiles,Users/*/AppData/Roaming/Microsoft/Office/Recent/**10,lazy_ntfs,
      838,Desktop LNK Files,LNKFiles,**10/*.LNK,lazy_ntfs,
      839,Robo-FTP User Scripts,Apps,Program Files/Robo-FTP 3.12/UserData/*/Scripts/*.s,lazy_ntfs,Custom scripts created by each user
      840,Robo-FTP User Debug Logs,Apps,Program Files/Robo-FTP 3.12/UserData/*/Debug/*.log,lazy_ntfs,"Debug logs generated for each user, if enabled"
      841,Robo-FTP User Script/Trace Logs,Apps,Program Files/Robo-FTP 3.12/UserData/*/Logs/*,lazy_ntfs,Script and Trace logs generated for each user
      842,Robo-FTP User XML Config,Apps,Program Files/Robo-FTP 3.12/UserData/*/config.xml,lazy_ntfs,Config.xml unique to each user. Contains list of custom scripts and ftp sites
      843,Robo-FTP User SSH Keys,Apps,Program Files/Robo-FTP 3.12/UserData/*/SSH Keys/*,lazy_ntfs,Saved SSH keys for each user
      844,Robo-FTP User SSL Certificates,Apps,Program Files/Robo-FTP 3.12/UserData/*/SSL Certificates/*,lazy_ntfs,Saved SSL Certificates for each user
      845,Robo-FTP User PGP Keys,Apps,Program Files/Robo-FTP 3.12/UserData/*/PGP Keys/*,lazy_ntfs,Saved PGP Keys for each user
      846,Robo-FTP SSH Keys,Apps,Program Files/Robo-FTP 3.12/ProgramData/SSH Keys/*,lazy_ntfs,Shared SSH keys
      847,Robo-FTP SSL Certificates,Apps,Program Files/Robo-FTP 3.12/ProgramData/SSL Certificates/*,lazy_ntfs,Shared SSL Certificates
      848,Robo-FTP PGP Keys,Apps,Program Files/Robo-FTP 3.12/ProgramData/PGP Keys/*,lazy_ntfs,Shared PGP Keys
      849,Robo-FTP Debug Logs,Apps,Program Files/Robo-FTP 3.12/ProgramData/Debug/*,lazy_ntfs,Debug logs generated by Robo-FTP
      850,Robo-FTP Script/Trace Logs,Apps,Program Files/Robo-FTP 3.12/ProgramData/Logs/*,lazy_ntfs,Script and Trace logs generated by Robo-FTP
      851,Robo-FTP XML Config,Apps,Program Files/Robo-FTP 3.12/ProgramData/config.xml,lazy_ntfs,Config.xml. Contains list of custom scripts and ftp sites
      852,Robo-FTP Jobs,Apps,Program Files/Robo-FTP 3.12/ProgramData/SchedulerService.sqlite,lazy_ntfs,Contains details of scheduled jobs
      853,RogueKiller Reports,Antivirus,ProgramData/RogueKiller/logs/AdliceReport_*.json,lazy_ntfs,
      854,RustDesk logs,Communications,Users/*/AppData/Roaming/RustDesk/*,lazy_ntfs,Collects all log files related to RustDesk
      855,RustDesk logs,Communications,Windows/ServiceProfiles/LocalService/AppData/Roaming/RustDesk/log/server,lazy_ntfs,Collects all log files related to RustDesk
      856,Usenet Clients - SABnzbd Download Logs,FileDownload,Users/*/AppData/Local/sabnzbd/logs/sabnzbd.log,lazy_ntfs,Locates SABnzbd download log
      857,Usenet Clients - SABnzbd History.db,FileDownload,Users/*/AppData/Local/sabnzbd/admin/history1.db,lazy_ntfs,Locates SABnzbd history log
      858,SCCM Client Log Files,Logs,Windows/CCM/Logs,lazy_ntfs,
      859,SDB Files,Executables,Windows/apppatch/Custom/*.sdb,lazy_ntfs,
      860,SDB Files,Executables,Windows.old/Windows/apppatch/Custom/*.sdb,lazy_ntfs,
      861,SDB Files x64,Executables,Windows/apppatch/Custom/Custom64/*.sdb,lazy_ntfs,
      862,SDB Files x64,Executables,Windows.old/Windows/apppatch/Custom/Custom64/*.sdb,lazy_ntfs,
      863,4K Video Downloader,SQLDatabases,Users/*/AppData/Local/4kdownload.com/4K Video Downloader/4K Video Downloader/*.sqlite,lazy_ntfs,Grabs database(s) that stores user download history
      864,Microsoft OneNote - FullTextSearchIndex,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/*/FullTextSearchIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's text content
      865,Microsoft OneNote - RecentNotebooks_SeenURLs,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/Notifications/RecentNotebooks_SeenURLs,lazy_ntfs,Grabs a file that appears to record recently seen OneNote notebooks
      866,Microsoft OneNote - AccessibilityCheckerIndex,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/16.0/AccessibilityCheckerIndex,lazy_ntfs,Grabs database(s) comprising of each OneNote notebook's version sync error history
      867,Microsoft OneNote - User NoteTags,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/16.0/NoteTags/*LiveId.db,lazy_ntfs,Grabs a database that stores the user specified tags within OneNote to be used application-wide
      868,Microsoft OneNote - RecentSearches,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.Office.OneNote_8wekyb3d8bbwe/LocalState/AppData/Local/OneNote/16.0/RecentSearches/RecentSearches.db,lazy_ntfs,Grabs a database that stores the user's recent searches within OneNote
      869,Microsoft Sticky Notes - 1607 and later,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.MicrosoftStickyNotes*/LocalState/plum.sqlite*,lazy_ntfs,
      870,Microsoft To Do - SQLite Database of To Do tasks,SQLDatabases,Users/*/AppData/Local/Packages/Microsoft.Todos_8wekyb3d8bbwe/LocalState/AccountsRoot/*/todosqlite.db*,lazy_ntfs,
      871,Robo-FTP Jobs,Apps,Program Files/Robo-FTP */ProgramData/SchedulerService.sqlite,lazy_ntfs,
      872,TeraCopy - History Databases,SQLDatabases,Users/*/AppData/Roaming/TeraCopy/History/*.db,lazy_ntfs,
      873,TeraCopy - Main Database,SQLDatabases,Users/*/AppData/Roaming/TeraCopy/main.db,lazy_ntfs,
      874,Notion Local Storage,App,Users/*/AppData/Roaming/Notion/notion.db,lazy_ntfs,
      875,IDrive Backed Up Files,App,ProgramData/IDrive/IBCOMMON/*/LDBNEW/*/*.idbs,lazy_ntfs,
      876,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/filecache.db*,lazy_ntfs,Getting individual files because folder may contain very large extraneous files
      877,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/config.dbx,lazy_ntfs,Getting individual files because folder may contain very large extraneous files
      878,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/home.db,lazy_ntfs,SQlite database which appears to keep track of the user's recent Dropbox activity
      879,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/icon.db,lazy_ntfs,SQLite database which appears to keep track of icons in the user's Drobox sync history which can give an indication as to which files and folders are present
      880,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/sync_history.db,lazy_ntfs,SQLite database which appears to keep track of the user's Drobox sync history
      881,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/sync/nucleus.sqlite3*,lazy_ntfs,SQLite database which appears to contain a table for deleted files
      882,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/host.db,lazy_ntfs,"SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
      883,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/host.dbx,lazy_ntfs,"SQLite database which contains the local path of the user's Dropbox folder encoded in BASE64. Decode each line separately, not together."
      884,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/sync/aggregation.dbx,lazy_ntfs,SQLite database which appears to contain snapshot table of the user's Dropbox contents in JSON with timestamps in UNIX Epoch
      885,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/avatarcache.db,lazy_ntfs,SQLite database which appears to contain the ID's of account(s) on the user's system where Dropbox is installed
      886,Dropbox Metadata,SQLDatabases,Users/*/AppData/Local/Dropbox/*/avatarcache.db,lazy_ntfs,SQLite database which appears to contain the ID's of account(s) on the user's system where Dropbox is installed
      887,Google File Stream Metadata,SQLDatabases,Users/*/AppData/Local/Google/Drive/*/cloud_graph/cloud_graph.db,lazy_ntfs,Windows_GoogleDrive_CloudGraphDB.smap
      888,Google File Stream Metadata,SQLDatabases,Users/*/AppData/Local/Google/Drive/*/TempData/*/change_buffer/**10,lazy_ntfs,DB(s) with seemingly randomized filename(s) that track file system changes within Google Drive
      889,Google File Stream Metadata,SQLDatabases,Users/*/AppData/Local/Google/Drive/*/snapshot.db,lazy_ntfs,Windows_GoogleDrive_SnapshotDB.smap
      890,Google File Stream Metadata,SQLDatabases,Users/*/AppData/Local/Google/Drive/*/sync_config.db,lazy_ntfs,Windows_GoogleDrive_SyncConfigDB.smap
      891,FileZilla SQLite3 Log Files,SQLDatabases,Users/*/AppData/Roaming/FileZilla/*.sqlite3*,lazy_ntfs,
      892,Chrome bookmarks XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Bookmarks*,lazy_ntfs,
      893,Chrome Cookies XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Cookies*,lazy_ntfs,
      894,Chrome Current Session XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Current Session,lazy_ntfs,
      895,Chrome Current Tabs XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Current Tabs,lazy_ntfs,
      896,Chrome Favicons XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Favicons*,lazy_ntfs,
      897,Chrome History XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/History*,lazy_ntfs,
      898,Chrome Last Session XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Last Session,lazy_ntfs,
      899,Chrome Last Tabs XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Last Tabs,lazy_ntfs,
      900,Chrome Login Data XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Login Data,lazy_ntfs,
      901,Chrome Preferences XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Preferences,lazy_ntfs,
      902,Chrome Shortcuts XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Shortcuts*,lazy_ntfs,
      903,Chrome Top Sites XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Top Sites*,lazy_ntfs,
      904,Chrome Visited Links XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Visited Links,lazy_ntfs,
      905,Chrome Web Data XP,SQLDatabases,Documents and Settings/*/Local Settings/Application Data/Google/Chrome/User Data/*/Web Data*,lazy_ntfs,
      906,Chrome bookmarks,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Bookmarks*,lazy_ntfs,
      907,Chrome Cookies,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Cookies*,lazy_ntfs,
      908,Chrome Current Session,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Session,lazy_ntfs,
      909,Chrome Current Tabs,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Current Tabs,lazy_ntfs,
      910,Chrome Download Metadata,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Download Metadata,lazy_ntfs,
      911,Chrome Extension Cookies,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Extension Cookies,lazy_ntfs,
      912,Chrome Favicons,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Favicons*,lazy_ntfs,
      913,Chrome History,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/History*,lazy_ntfs,
      914,Chrome Last Session,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Session,lazy_ntfs,
      915,Chrome Last Tabs,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Last Tabs,lazy_ntfs,
      916,Chrome Login Data,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Login Data,lazy_ntfs,
      917,Chrome Media History,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Media History*,lazy_ntfs,
      918,Chrome Network Action Predictor,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Action Predictor,lazy_ntfs,
      919,Chrome Network Persistent State,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Network Persistent State,lazy_ntfs,
      920,Chrome Preferences,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Preferences,lazy_ntfs,
      921,Chrome Quota Manager,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/QuotaManager,lazy_ntfs,
      922,Chrome Reporting and NEL,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Reporting and NEL,lazy_ntfs,
      923,Chrome Shortcuts,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Shortcuts*,lazy_ntfs,
      924,Chrome Top Sites,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Top Sites*,lazy_ntfs,
      925,Chrome Trust Tokens,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Trust Tokens*,lazy_ntfs,
      926,Chrome SyncData Database,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Sync Data/SyncData.sqlite3,lazy_ntfs,
      927,Chrome Visited Links,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Visited Links,lazy_ntfs,
      928,Chrome Web Data,SQLDatabases,Users/*/AppData/Local/Google/Chrome/User Data/*/Web Data*,lazy_ntfs,
      929,Edge bookmarks,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Bookmarks*,lazy_ntfs,
      930,Edge Collections,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Collections/collectionsSQLite,lazy_ntfs,
      931,Edge Cookies,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Cookies*,lazy_ntfs,
      932,Edge Current Session,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Current Session,lazy_ntfs,
      933,Edge Current Tabs,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Current Tabs,lazy_ntfs,
      934,Edge Favicons,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Favicons*,lazy_ntfs,
      935,Edge History,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/History*,lazy_ntfs,
      936,Edge Last Session,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Last Session,lazy_ntfs,
      937,Edge Last Tabs,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Last Tabs,lazy_ntfs,
      938,Edge Login Data,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Login Data,lazy_ntfs,
      939,Edge Media History,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Media History*,lazy_ntfs,
      940,Edge Network Action Predictor,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Network Action Predictor,lazy_ntfs,
      941,Edge Preferences,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Preferences,lazy_ntfs,
      942,Edge Shortcuts,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Shortcuts*,lazy_ntfs,
      943,Edge Top Sites,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Top Sites*,lazy_ntfs,
      944,Edge SyncData Database,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Sync Data/SyncData.sqlite3,lazy_ntfs,
      945,Edge Bookmarks,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Bookmarks*,lazy_ntfs,
      946,Edge Visited Links,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Visited Links,lazy_ntfs,
      947,Edge Web Data,SQLDatabases,Users/*/AppData/Local/Microsoft/Edge/User Data/*/Web Data*,lazy_ntfs,
      948,Addons,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/addons.sqlite*,lazy_ntfs,
      949,Bookmarks,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/weave/bookmarks.sqlite*,lazy_ntfs,
      950,Cookies,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/cookies.sqlite*,lazy_ntfs,
      951,Cookies,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/firefox_cookies.sqlite*,lazy_ntfs,
      952,Downloads,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/downloads.sqlite*,lazy_ntfs,
      953,Favicons,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/favicons.sqlite*,lazy_ntfs,
      954,Form history,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/formhistory.sqlite*,lazy_ntfs,
      955,Permissions,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/permissions.sqlite*,lazy_ntfs,
      956,Places,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/places.sqlite*,lazy_ntfs,
      957,Protections,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/protections.sqlite*,lazy_ntfs,
      958,Search,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/search.sqlite*,lazy_ntfs,
      959,Signons,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/signons.sqlite*,lazy_ntfs,
      960,Storage Sync,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/storage-sync.sqlite*,lazy_ntfs,
      961,Webappstore,SQLDatabases,Users/*/AppData/Roaming/Mozilla/Firefox/Profiles/*/webappstore.sqlite*,lazy_ntfs,
      962,Windows 10 Notification DB,SQLDatabases,Users/*/AppData/Local/Microsoft/Windows/Notifications/wpndatabase.db,lazy_ntfs,
      963,Windows 10 Notification DB,SQLDatabases,Users/*/AppData/Local/Microsoft/Windows/Notifications/appdb.dat,lazy_ntfs,
      964,ActivitiesCache.db,SQLDatabases,Users/*/AppData/Local/ConnectedDevicesPlatform/*/ActivitiesCache.db*,lazy_ntfs,
      965,Update Store.db,OS Upgrade,ProgramData/USOPrivate/UpdateStore/store.db,lazy_ntfs,
      966,Bitdefender SQLite DB Files,Antivirus,Program Files*/Bitdefender*/**10/regex:*.+/.(db|db-wal|db-shm),ntfs,Bitdefender SQLite databases
      967,EventTranscript.db,SystemEvents,ProgramData/Microsoft/Diagnosis/EventTranscript/EventTranscript.db*,lazy_ntfs,
      968,EventTranscript.db,SystemEvents,Windows.old/ProgramData/Microsoft/Diagnosis/EventTranscript/EventTranscript.db*,lazy_ntfs,
      969,SRUM,Execution,Windows/System32/SRU/**10,lazy_ntfs,
      970,SRUM,Execution,Windows.old/Windows/System32/SRU/**10,lazy_ntfs,
      971,SOFTWARE registry hive,Registry,Windows/System32/config/SOFTWARE,lazy_ntfs,
      972,SOFTWARE registry hive,Registry,Windows.old/Windows/System32/config/SOFTWARE,lazy_ntfs,
      973,SOFTWARE registry transaction files,Registry,Windows/System32/config/SOFTWARE.LOG*,lazy_ntfs,
      974,SOFTWARE registry transaction files,Registry,Windows.old/Windows/System32/config/SOFTWARE.LOG*,lazy_ntfs,
      975,SUM Database (.mdb files),Logs,Windows/System32/LogFiles/SUM/*.mdb,lazy_ntfs,"Grabs Current.mdb, SystemIdentity.mdb, and [GUID].mdb"
      976,SUPERAntiSpyware Logs,Antivirus,Users/*/AppData/Roaming/SUPERAntiSpyware/Logs/**10,lazy_ntfs,
      977,SUSE Linux Enterprise Server WSL /etc/os-release,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/os-release,lazy_ntfs,
      978,SUSE Linux Enterprise Server WSL /etc/fstab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/fstab,lazy_ntfs,
      979,SUSE Linux Enterprise Server WSL /etc/passwd,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/passwd,lazy_ntfs,
      980,SUSE Linux Enterprise Server WSL /etc/group,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/group,lazy_ntfs,
      981,SUSE Linux Enterprise Server WSL /etc/shadow,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/shadow,lazy_ntfs,
      982,SUSE Linux Enterprise Server WSL /etc/timezone,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/timezone,lazy_ntfs,
      983,SUSE Linux Enterprise Server WSL /etc/hostname,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/hostname,lazy_ntfs,
      984,SUSE Linux Enterprise Server WSL /etc/hosts,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/hosts,lazy_ntfs,
      985,SUSE Linux Enterprise Server WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/bash.bashrc,lazy_ntfs,
      986,SUSE Linux Enterprise Server WSL /etc/profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/etc/profile,lazy_ntfs,
      987,SUSE Linux Enterprise Server WSL .bash_history,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/**10/.bash_history,lazy_ntfs,
      988,SUSE Linux Enterprise Server WSL .bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/**10/.bashrc,lazy_ntfs,
      989,SUSE Linux Enterprise Server WSL .profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/rootfs/**10/.profile,lazy_ntfs,
      990,SUSE Linux Enterprise Server WSL ext4.vhdx,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.SUSELinuxEnterpriseServer*/LocalState/ext4.vhdx,lazy_ntfs,
      991,at .job,Persistence,Windows/Tasks/*.job,lazy_ntfs,
      992,at .job,Persistence,Windows.old/Windows/Tasks/*.job,lazy_ntfs,
      993,at SchedLgU.txt,Persistence,Windows/SchedLgU.txt,lazy_ntfs,
      994,at SchedLgU.txt,Persistence,Windows.old/Windows/SchedLgU.txt,lazy_ntfs,
      995,XML,Persistence,Windows/System32/Tasks/**10,lazy_ntfs,
      996,XML,Persistence,Windows/syswow64/Tasks/**10,lazy_ntfs,
      997,XML,Persistence,Windows.old/Windows/System32/Tasks/**10,lazy_ntfs,
      998,ScreenConnect Session Database,ApplicationLogs,Program Files*/ScreenConnect/App_Data/Session.db,lazy_ntfs,SQLite database with session information
      999,ScreenConnect Session Database,ApplicationLogs,Program Files*/ScreenConnect/App_Data/User.xml,lazy_ntfs,Contains each user's last authenticated time
      1000,ScreenConnect User Config,ApplicationLogs,ProgramData/ScreenConnect Client*/user.config,lazy_ntfs,Contains server domain and IP info
      1001,SecureAge Antvirus Logs,Antivirus,ProgramData/SecureAge Technology/SecureAge/log/**10,lazy_ntfs,
      1002,SentinelOne EDR Log,Antivirus,programdata/sentinel/logs/**10,lazy_ntfs,Logs are in Binary Format (.binlog)
      1003,ShareX,Apps,Users/*/Documents/ShareX/**10,lazy_ntfs,Locates and captures all files within the default ShareX folder path
      1004,Shareaza Logs,FileDownload,Users/*/AppData/Roaming/Shareaza/**10,lazy_ntfs,Locates Shareaza logs and copies them.
      1005,Siemens TIA Settings,ICS,Users/*/AppData/Roaming/Siemens/Automation/Portal*/Settings/**10,lazy_ntfs,
      1006,Signal Attachments cache,Communications,Users/*/AppData/Roaming/Signal/attachments.noindex/**10,lazy_ntfs,Profile pictures (and possibly attachments) for users who this individual has as contacts or has communicated with
      1007,Signal Logs,Communications,Users/*/AppData/Roaming/Signal/logs/**10,lazy_ntfs,"Logs for Signal. Most recent has the extension .log while old ones will have extension .log.0, .log.1 etc."
      1008,Signal config.json,Communications,Users/*/AppData/Roaming/Signal/config.json,lazy_ntfs,config.json holds the db.sqlite SQLCipher raw key
      1009,Signal Database,Communications,Users/*/AppData/Roaming/Signal/sql/db.sqlite,lazy_ntfs,"Stores attachment details, conversations, messages, and more"
      1010,SignatureCatalog,FileMetadata,Windows/System32/CatRoot/**10,lazy_ntfs,
      1011,SignatureCatalog,FileMetadata,Windows.old/Windows/System32/CatRoot/**10,lazy_ntfs,
      1012,main.db (App &lt;v12),Communications,Users/*/AppData/Local/Packages/Microsoft.SkypeApp_*/LocalState/*/main.db,lazy_ntfs,
      1013,skype.db (App +v12),Communications,Users/*/AppData/Local/Packages/Microsoft.SkypeApp_*/LocalState/*/skype.db,lazy_ntfs,
      1014,main.db XP,Communications,Documents and Settings/*/Application Data/Skype/*/main.db,lazy_ntfs,
      1015,main.db Win7+,Communications,Users/*/AppData/Roaming/Skype/*/main.db,lazy_ntfs,
      1016,s4l-[username].db (App +v8),Communications,Users/*/AppData/Local/Packages/Microsoft.SkypeApp_*/LocalState/s4l-*.db,lazy_ntfs,
      1017,leveldb (Skype for Desktop +v8),Communications,Users/*/AppData/Roaming/Microsoft/Skype for Desktop/IndexedDB/*.leveldb/**10,lazy_ntfs,
      1018,Skype for Destkop v8+ Chromium Cache,Communications,Users/*/AppData/Roaming/Microsoft/Skype for Desktop/Cache/**10,lazy_ntfs,Can be viewed with Nirsoft's ChromeCacheView
      1019,Slack - Chat Logs,Apps,Users/*/AppData/Roaming/Slack/IndexedDB/**10,lazy_ntfs,Locates Slack logs and copies them
      1020,Slack LevelDB Files,Apps,Users/*/AppData/Roaming/Slack/Local Storage/leveldb/**10,lazy_ntfs,
      1021,Slack Electron Logs,Apps,Users/*/AppData/Roaming/Slack/logs/**10,lazy_ntfs,Current Slack application is based on Electron and additional logging can be found here.
      1022,Slack Cache,Apps,Users/*/AppData/Roaming/Slack/Cache/**10,lazy_ntfs,Collects Slack cache files. This folder can be parsed like a Chrome Browser cache using a tool like Nirsoft ChromeCacheView
      1023,Slack Storage,Apps,Users/*/AppData/Roaming/Slack/storage/**10,lazy_ntfs,User activity logs can be present including slack-downloads log
      1024,Snagit - Captures,Apps,Users/*/AppData/Local/TechSmith/Snagit/DataStore,lazy_ntfs,Locates all Snagit captures
      1025,Snip &amp; Sketch,FileKnowledge,Users/*/AppData/Local/Packages/Microsoft.ScreenSketch_8wekyb3d8bbwe/TempState/*.png,lazy_ntfs,Pulls all temporary .png images generated by the Snip &amp; Sketch screen capture tool built into Windows
      1026,Sophos Logs (XP),Antivirus,Documents and Settings/All Users/Application Data/Sophos/Sophos */Logs/**10,lazy_ntfs,"Includes Anti-Virus, Client Firewall, Data Control, Device Control, Endpoint Defense, Network Threat Detection, Management Communications System, Patch Control, Tamper Protection"
      1027,Sophos Logs,Antivirus,ProgramData/Sophos/Sophos */Logs/**10,lazy_ntfs,"Includes Anti-Virus, Client Firewall, Data Control, Device Control, Endpoint Defense, Network Threat Detection, Management Communications System, Patch Control, Tamper Protection"
      1028,Soulseek Chat Logs,FileDownload,Users/*/AppData/Local/SoulseekQt/Soulseek Chat Logs/**10,lazy_ntfs,Locates Soulseek chat logs and copies them. Chat logs are in plaintext. Current as of version 2019.7.22.
      1029,Soulseek Search History/Shared Folders/Settings,FileDownload,Users/*/AppData/Local/SoulseekQt/1/*.dat,lazy_ntfs,"Locates .dat file(s) containing: search history, active searches (search_record), current shared folders (shared_file_folder), and wish list items (wish_list_item)."
      1030,SpeedCommander - .ini File,Apps,Users/*/AppData/Roaming/SpeedProject/SpeedCommander 19/*,lazy_ntfs,Locates folder where all configuration files reside
      1031,Splashtop Log Files,Software,Program Files*/Splashtop/Splashtop Remote/Server/log/**10,lazy_ntfs,Collects logs for Splashtop
      1032,Splashtop Log Files in ProgramData,Software,ProgramData/Splashtop/Temp/log/**10,lazy_ntfs,Collects logs for Splashtop
      1033,User startup folders,Persistence,Users/*/AppData/Roaming/Microsoft/Windows/Start Menu/Programs/Startup,lazy_ntfs,
      1034,System-wide startup folder,Persistence,ProgramData/Microsoft/Windows/Start Menu/Programs/StartUp,lazy_ntfs,
      1035,StartupInfo XML Files,Persistence,Windows/System32/WDI/LogFiles/StartupInfo/*.xml,lazy_ntfs,
      1036,StartupInfo XML Files,Persistence,Windows.old/Windows/System32/WDI/LogFiles/StartupInfo/*.xml,lazy_ntfs,
      1037,Steam Game Image files,Apps,Program Files/Steam/appcache/librarycache/**10,lazy_ntfs,Locates the directory containing image resources of installed/uninstalled games.
      1038,Steam Login Metadata file,Apps,Program Files/Steam/config/**10/loginusers.vdf,lazy_ntfs,Locates file containing Steam username and persona name.
      1039,Steam Friend List and Username History file,Apps,Program Files/Steam/userdata/*/config/**10/localconfig.vdf,lazy_ntfs,Locates file containing Steam Friend List and Username History.
      1040,Steam User Avatar files,Apps,Program Files/Steam/config/avatarcache/**10,lazy_ntfs,Locates the directory containing avatar cache.
      1041,Steam Game Tray Icon files,Apps,Program Files/Steam/steam/games/**10,lazy_ntfs,Locates the directory containing game icons appearing from tray menu.
      1042,Steam Startup Times Log file,Apps,Program Files/Steam/logs/**10/bootstrap_log.txt,lazy_ntfs,Locates the directory containing log for Steam startup times.
      1043,Steam Game Image files,Apps,Program Files (x86)/Steam/appcache/librarycache/**10,lazy_ntfs,Locates the directory containing image resources of installed/uninstalled games.
      1044,Steam Login Metadata file,Apps,Program Files (x86)/Steam/config/**10/loginusers.vdf,lazy_ntfs,Locates file containing Steam username and persona name.
      1045,Steam Friend List and Username History file,Apps,Program Files (x86)/Steam/userdata/*/config/**10/localconfig.vdf,lazy_ntfs,Locates file containing Steam Friend List and Username History.
      1046,Steam User Avatar files,Apps,Program Files (x86)/Steam/config/avatarcache/**10,lazy_ntfs,Locates the directory containing avatar cache.
      1047,Steam Game Tray Icon files,Apps,Program Files (x86)/Steam/steam/games/**10,lazy_ntfs,Locates the directory containing game icons appearing from tray menu.
      1048,Steam Startup Times Log file,Apps,Program Files (x86)/Steam/logs/**10/bootstrap_log.txt,lazy_ntfs,Locates the directory containing log for Steam startup times.
      1049,SublimeText 2/3 Auto Save Session,Text Editor,Users/*/AppData/Roaming/Sublime Text*/Settings/Session.sublime_session,lazy_ntfs,Sublime Text 2/3 stores unsaved (temporary) files and its content in its Session.sublime_session file
      1050,SublimeText 4 Auto Save Session,Text Editor,Users/*/AppData/Roaming/Sublime Text*/Local/*.sublime_session,lazy_ntfs,Sublime Text 4 stores unsaved (temporary) files and its content in its .sublime_session files
      1051,SugarSync Log File,Apps,Users/*/AppData/Local/SugarSync/sc1.log,lazy_ntfs,Locates a log file the gives a play-by-play of what the user synced when.
      1052,SugarSync - Shared Folders (Default Location),Apps,Users/*/Documents/SugarSync Shared Folders/**10,lazy_ntfs,
      1053,SugarSync - My SugarSync (Default Location),Apps,Users/*/Documents/My SugarSync/**10,lazy_ntfs,
      1054,SumatraPDF Settings - SessionData,FileKnowledge,Users/*/AppData/Local/SumatraPDF/SumatraPDF-settings.txt,lazy_ntfs,Settings file which contains information about previous user session
      1055,SumatraPDF Cache,FileKnowledge,Users/*/AppData/Local/SumatraPDF/sumatrapdfcache,lazy_ntfs,Folder contains a PNG snapshot of each PDF file the user had open at the time of last application close
      1056,Supremo Connection Logs,Communications,ProgramData/SupremoRemoteDesktop/Log/*.log,lazy_ntfs,Includes Supremo.00.Client.log and Supremo.00.Incoming.log
      1057,Supremo File Transfer Inbox,Communications,ProgramData/SupremoRemoteDesktop/Inbox,lazy_ntfs,Includes all files transferred to the inbox folder during a remote session
      1058,Symantec Endpoint Protection Logs (XP),Antivirus,Documents and Settings/All Users/Application Data/Symantec/Symantec Endpoint Protection/Logs/AV/**10,lazy_ntfs,
      1059,Symantec Endpoint Protection Logs,Antivirus,ProgramData/Symantec/Symantec Endpoint Protection/*/Data/Logs/**10,lazy_ntfs,
      1060,Symantec Endpoint Protection User Logs,Antivirus,Users/*/AppData/Local/Symantec/Symantec Endpoint Protection/Logs/**10,lazy_ntfs,
      1061,Symantec Event Log Win7+,EventLogs,Windows/System32/winevt/logs/Symantec Endpoint Protection Client.evtx,lazy_ntfs,Symantec specific Windows event log
      1062,Symantec Event Log Win7+,EventLogs,Windows.old/Windows/System32/winevt/logs/Symantec Endpoint Protection Client.evtx,lazy_ntfs,Symantec specific Windows event log
      1063,Symantec Endpoint Protection Quarantine (XP),Antivirus,Documents and Settings/All Users/Application Data/Symantec/Symantec Endpoint Protection/Quarantine/**10,lazy_ntfs,
      1064,Symantec Endpoint Protection Quarantine,Antivirus,ProgramData/Symantec/Symantec Endpoint Protection/*/Data/Quarantine/**10,lazy_ntfs,
      1065,ccSubSDK Database,Antivirus,ProgramData/Symantec/Symantec Endpoint Protection/*/Data/CmnClnt/ccSubSDK/**10,lazy_ntfs,
      1066,registrationInfo.xml,Antivirus,ProgramData/Symantec/Symantec Endpoint Protection/*/Data/registrationInfo.xml,lazy_ntfs,
      1067,Syscache,Program Execution,System Volume Information/Syscache.hve,lazy_ntfs,
      1068,Syscache transaction files,Program Execution,System Volume Information/Syscache.hve.LOG*,lazy_ntfs,
      1069,Tablacus Explorer - remember.xml,Logs,Users/*/AppData/Local/Temp/*/config/**10/remember.xml,lazy_ntfs,
      1070,Tablacus Explorer - window.xml,Logs,Users/*/AppData/Local/Temp/*/config/**10/window.xml,lazy_ntfs,
      1071,Tablacus Explorer - window1.xml,Logs,Users/*/AppData/Local/Temp/*/config/**10/window1.xml,lazy_ntfs,
      1072,TeamViewer Connection Logs,Communications,Program Files*/TeamViewer/connections*.txt,lazy_ntfs,Includes connections_incoming.txt and connections.txt
      1073,TeamViewer Application Logs,ApplicationLogs,Program Files*/TeamViewer/TeamViewer*_Logfile*,lazy_ntfs,Includes TeamViewer&lt;version&gt;_Logfile.log and TeamViewer&lt;version&gt;_Logfile_OLD.log
      1074,TeamViewer Application User Logs,ApplicationLogs,Users/*/AppData/Roaming/TeamViewer/TeamViewer*_Logfile*,lazy_ntfs,Alternate location for TeamViewer&lt;version&gt;_Logfile.log
      1075,TeamViewer Configuration Files,ApplicationLogs,Users/*/AppData/Roaming/TeamViewer/MRU/RemoteSupport/**10,lazy_ntfs,Includes miscellaneous config files
      1076,Telegram app folder,Apps,Users/*/AppData/Roaming/Telegram Desktop/**10,lazy_ntfs,Telegram app folder structure
      1077,Telegram downloaded files,Apps,Users/*/Downloads/Telegram Desktop/**10,lazy_ntfs,Chat Attachments
      1078,TeraCopy,TeraCopy,Users/*/AppData/Roaming/TeraCopy/**10,lazy_ntfs,
      1079,Thumbcache DB,FileKnowledge,Users/*/AppData/Local/Microsoft/Windows/Explorer/thumbcache_*.db,lazy_ntfs,
      1080,Mozilla Thunderbird Install Date,Apps,Users/*/AppData/Roaming/Thunderbird/Crash Reports/InstallTime*,lazy_ntfs,Holds install time in Unix Seconds timestamp
      1081,Mozilla Thunderbird Profiles.ini,Apps,Users/*/AppData/Roaming/Thunderbird/profiles.ini,lazy_ntfs,Profiles list - can hold references to other profiles held elsewhere on the device
      1082,Mozilla Thunderbird prefs.js,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/prefs.js,lazy_ntfs,User Preferences for that profile
      1083,Mozilla Thunderbird Global Messages Database,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/global-messages-db.sqlite,lazy_ntfs,"Holds list of contacts, emails, and other potentially useful artifacts"
      1084,Mozilla Thunderbird logins.json,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/logins.json,lazy_ntfs,"Holds last time online login used, last time password changed, hostname, HTTP(s) URL and more"
      1085,Mozilla Thunderbird places.sqlite,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/places.sqlite,lazy_ntfs,"Holds history for Thunderbird - as it contains portions of Firefox embedded, it can be used to visit websites too"
      1086,Mozilla Thunderbird ImapMail INBOX,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/ImapMail/**10/INBOX,lazy_ntfs,"Holds all email files with headers, content etc"
      1087,Mozilla Thunderbird Mail INBOX,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/Mail/**10/INBOX,lazy_ntfs,"Holds all email files with headers, content etc"
      1088,Mozilla Thunderbird Calendar Data,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/calendar-data/local.sqlite,lazy_ntfs,Holds local calendar data
      1089,Mozilla Thunderbird Attachments,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/Attachments/*,lazy_ntfs,Holds attachments
      1090,Mozilla Thunderbird Address Book,Apps,Users/*/AppData/Roaming/Thunderbird/Profiles/*/abook.sqlite,lazy_ntfs,Holds local address book
      1091,Torrents,FileDownload,**10/*.torrent,lazy_ntfs,
      1092,TotalAV Logs,Antivirus,Program Files*/TotalAV/logs/**10,lazy_ntfs,
      1093,TotalAV Logs,Antivirus,ProgramData/TotalAV/logs/**10,lazy_ntfs,
      1094,Total Commander - .ini File,Apps,Users/*/AppData/Roaming/GHISLER/wincmd.ini,lazy_ntfs,Locates .ini file associated with Total Commander which stores useful user activity information.
      1095,Total Commander - Log File,Apps,**10/totalcmd.log,lazy_ntfs,Locates log file associated with Total Commander. NOTE: this log file is NOT enabled by default and the filename can be modified.
      1096,Total Commander - Temp Files Created During Folder Traversal,Apps,Users/*/AppData/Local/Temp/FTP*.tmp,lazy_ntfs,Locates .tmp files which are created during the user's folder traversal and provide insight into contents of each folder traversed.
      1097,Total Commander - FTP .ini File,Apps,Users/*/AppData/Roaming/GHISLER/wcx_ftp.ini,lazy_ntfs,Locates .ini file associated with Total Commander which stores useful FTP information.
      1098,Total Commander - File Tree,Apps,Users/*/AppData/Local/GHISLER/treeinfo*.wc,lazy_ntfs,Locates a file that contains an exhaustive file tree of a user's file system.
      1099,Total Commander - Frequent Directory Listing,Apps,Users/*/AppData/Local/GHISLER/tcDirFrq.txt,lazy_ntfs,Locates a file that contains a frequently accessed folder listing.
      1100,Total Commander - FTP Logs,Apps,Users/*/AppData/Local/Temp/tcftp.log,lazy_ntfs,Locates a file that contains the Total Commander FTP logs.
      1101,TreeSize - ScanHistory.XML,Apps,Users/*/AppData/Roaming/JAM Software/TreeSize/scanhistory.xml,lazy_ntfs,Locates XML file that provides a list of previously scanned directories by the user.
      1102,Trend Micro Logs,Antivirus,ProgramData/Trend Micro/**10,lazy_ntfs,
      1103,Trend Micro Security Agent Report Logs,Antivirus,Program Files*/Trend Micro/Security Agent/Report/*.log,lazy_ntfs,
      1104,Trend Micro Security Agent Connection Logs,Antivirus,Program Files*/Trend Micro/Security Agent/ConnLog/*.log,lazy_ntfs,
      1105,Setupapi.log XP,USBDevices,Windows/setupapi.log,lazy_ntfs,
      1106,Setupapi.log Win7+,USBDevices,Windows/inf/setupapi.*.log,lazy_ntfs,
      1107,Setupapi.log Win7+,USBDevices,Windows.old/Windows/inf/setupapi.*.log,lazy_ntfs,
      1108,Ubuntu WSL /etc/os-release,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/os-release,lazy_ntfs,
      1109,Ubuntu WSL /etc/fstab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/fstab,lazy_ntfs,
      1110,Ubuntu WSL /etc/passwd,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/passwd,lazy_ntfs,
      1111,Ubuntu WSL /etc/group,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/group,lazy_ntfs,
      1112,Ubuntu WSL /etc/shadow,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/shadow,lazy_ntfs,
      1113,Ubuntu WSL /etc/timezone,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/timezone,lazy_ntfs,
      1114,Ubuntu WSL /etc/hostname,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/hostname,lazy_ntfs,
      1115,Ubuntu WSL /etc/hosts,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/hosts,lazy_ntfs,
      1116,Ubuntu WSL /etc/crontab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/crontab,lazy_ntfs,
      1117,Ubuntu WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/bash.bashrc,lazy_ntfs,
      1118,Ubuntu WSL /etc/profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/etc/profile,lazy_ntfs,
      1119,Ubuntu WSL .bash_history,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/**10/.bash_history,lazy_ntfs,
      1120,Ubuntu WSL .bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/**10/.bashrc,lazy_ntfs,
      1121,Ubuntu WSL .profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/**10/.profile,lazy_ntfs,
      1122,Ubuntu WSL User Crontabs,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/var/spool/cron/crontabs/**10,lazy_ntfs,
      1123,Ubuntu WSL Apt Logs,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/rootfs/var/log/apt/**10/*.log,lazy_ntfs,
      1124,Ubuntu WSL ext4.vhdx,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/CanonicalGroupLimited.Ubuntu*/LocalState/ext4.vhdx,lazy_ntfs,
      1125,UltraViewer User Logs,Remote Access,Users/*/AppData/Roaming/UltraViewer/**10,lazy_ntfs,"Includes all files related to UltraViewer chat, connections, and recordings"
      1126,UltraViewer System Logs,Remote Access,Windows/SysWOW64/config/systemprofile/AppData/Roaming/UltraViewer/**10,lazy_ntfs,"Includes all files related to UltraViewer chat, connections, and recordings"
      1127,UltraViewer Service Log,Remote Access,Program Files*/UltraViewer/UltraViewerService_log.txt,lazy_ntfs,UltraViewer Service log file
      1128,UltraViewer Connection Log,Remote Access,Program Files*/UltraViewer/ConnectionLog.Log,lazy_ntfs,UltraViewer Service level connection log
      1129,Usenet (NZB) Files,FileDownload,**10/*.nzb,lazy_ntfs,
      1130,VIPRE Business Agent Logs,Antivirus,ProgramData/VIPRE Business Agent/Logs/**10,lazy_ntfs,
      1131,VIPRE Business User Logs (v7+),Antivirus,Users/*/AppData/Roaming/VIPRE Business/**10,lazy_ntfs,
      1132,VIPRE Business User Logs (v5-v6),Antivirus,Users/*/AppData/Roaming/GFI Software/AntiMalware/Logs/**10,lazy_ntfs,
      1133,VIPRE Business User Logs (up to v4),Antivirus,Users/*/AppData/Roaming/Sunbelt Software/AntiMalware/Logs/**10,lazy_ntfs,
      1134,VLC Recently Opened Files,Apps,Users/*/AppData/Roaming/vlc/vlc-qt-interface.ini,lazy_ntfs,Configuration file for VLC. Holds [RecentsMRL] key which lists recently opened files as well as sometimes retaining timestamps for file opening
      1135,VLC Recorded Files,Apps,Users/*/Videos/vlc-*.avi,lazy_ntfs,"Recorded files in VLC. Sometimes the Record button may be pressed instead of Play by suspects, which can record them watching content with VLC"
      1136,VMware - Virtual Machine Inventory,Apps,Users/*/AppData/Roaming/VMware,lazy_ntfs,Locates an inventory of all Virtual Machines on disk.
      1137,VMware (Fusion/Workstation/Server/Player),Memory,**10/*.vmem,lazy_ntfs,Captures all raw memory from VMware virtual machines.
      1138,VMware (Fusion/Workstation/Server/Player),Memory,**10/*.vmss,lazy_ntfs,Captures all memory images from VMware virtual machines.
      1139,VMware (Fusion/Workstation/Server/Player),Memory,**10/*.vmsn,lazy_ntfs,Captures all memory images from VMware virtual machines.
      1140,RealVNC Log,ApplicationLogs,Users/*/AppData/Local/RealVNC/vncserver.log,lazy_ntfs,https://www.realvnc.com/en/connect/docs/logging.html#logging
      1141,RealVNC Log,ApplicationLogs,ProgramData/RealVNC-Service/vncserver.log,lazy_ntfs,https://help.realvnc.com/hc/en-us/articles/360002254238-All-About-Logging-
      1142,TightVNC Application Logs,ApplicationLogs,ProgramData/TightVNC/Server/Logs,lazy_ntfs,https://ro.ecu.edu.au/cgi/viewcontent.cgi?article=1160&amp;context=adf
      1143,Viber Config Database,Apps,Users/*/AppData/Roaming/ViberPC/config.db,lazy_ntfs,Configuration file for Viber
      1144,Viber Users Data Database,Apps,Users/*/AppData/Roaming/ViberPC/*/viber.db,lazy_ntfs,"Viber data for that user, containing Calls, Chat Messages, Contacts and more"
      1145,Viber Users Avatars Cache,Apps,Users/*/AppData/Roaming/ViberPC/*/Avatars,lazy_ntfs,Cache of the Avatars for other Viber users
      1146,Viber Users Backgrounds Cache,Apps,Users/*/AppData/Roaming/ViberPC/*/Backgrounds,lazy_ntfs,Store of the backgrounds
      1147,Viber Users Thumbnails Cache,Apps,Users/*/AppData/Roaming/ViberPC/*/Thumbnails,lazy_ntfs,Cache of the thumbnails for uploaded/downloaded images
      1148,VirtualBox VM configs,Apps,**10/*.vbox,lazy_ntfs,Locates all .vbox VM configuration files on disk
      1149,VirtualBox VM backup configs,Apps,**10/*.vbox-prev,lazy_ntfs,Locates all backup .vbox VM configuration files on disk
      1150,VirtualBox Logs,Apps,**10/VBox.log,lazy_ntfs,Locates all VBox.log files on disk
      1151,VirtualBox Backup Logs,Apps,**10/VBox.log.*,lazy_ntfs,Locates all backup VBox.log files on disk - these can show historic VM usage
      1152,VirtualBox Hardening Logs,Apps,**10/VBoxHardening.log,lazy_ntfs,Locates all VBoxHardening.log files on disk
      1153,VirtualBox,Memory,**10/*.sav,lazy_ntfs,Captures all partial memory images from VirtualBox.
      1154,VHD,Disk Images,**10/*.VHD,lazy_ntfs,
      1155,VHDX,Disk Images,**10/*.VHDX,lazy_ntfs,
      1156,VDI,Disk Images,**10/*.VDI,lazy_ntfs,
      1157,VMDK,Disk Images,**10/*.VMDK,lazy_ntfs,
      1158,VSCode Opened Files,Apps,Users/*/AppData/Roaming/Code/User/History/*/**10,lazy_ntfs,Grabs the files in the VSCode history. These are files the user has opened with VSCode
      1159,VSCode Workspaces,Apps,Users/*/AppData/Roaming/Code/User/globalStorage/storage.json*,lazy_ntfs,Grabs the file containing information about the users workspaces
      1160,VSCode User extensions,Apps,Users/*/AppData/Roaming/Code/CachedExtensions/user*,lazy_ntfs,Grabs the files relating to the users installed extensions
      1161,VSCode User settings,Apps,Users/*/AppData/Roaming/Code/User/settings.json*,lazy_ntfs,Grabs the file containing the settings the user has set.
      1162,VSCode User Preferences,Apps,Users/*/AppData/Roaming/Code/preferences*,lazy_ntfs,Grabs the file containing the preferences the user has set.
      1163,VSCode Network Cookies,Apps,Users/*/AppData/Roaming/Code/Network/Cookies*,lazy_ntfs,Grabs the cookie files. Same format as Chromium Cookies
      1164,VSCode Network Persistent State,Apps,Users/*/AppData/Roaming/Code/Network/Network Persistent State*,lazy_ntfs,Grabs the Network Persistent State file. Same format as in  Chromium
      1165,VSCode Logs,Apps,Users/*/AppData/Roaming/Code/logs/**10,lazy_ntfs,"Grabs the VSCode logs. Further analysis is needed to determine which logs are junk, and which can be vital."
      1166,Vivaldi Cookies,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/**10/Cookies*,lazy_ntfs,
      1167,Vivaldi Network Persistent State,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/**10/Network Persistent State,lazy_ntfs,
      1168,Vivaldi Favicons,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Favicons*,lazy_ntfs,
      1169,Vivaldi History,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/History*,lazy_ntfs,
      1170,Vivaldi Sessions Folder,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Sessions/*,lazy_ntfs,
      1171,Vivaldi Login Data,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Login Data,lazy_ntfs,
      1172,Vivaldi Network Action Predictor,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Network Action Predictor,lazy_ntfs,
      1173,Vivaldi Preferences,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Preferences,lazy_ntfs,
      1174,Vivaldi Top Sites,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Top Sites*,lazy_ntfs,
      1175,Vivaldi Bookmarks,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Bookmarks*,lazy_ntfs,
      1176,Vivaldi Visited Links,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Visited Links,lazy_ntfs,
      1177,Vivaldi Web Data,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Web Data*,lazy_ntfs,
      1178,Vivaldi User Tracking,Communications,Users/*/.vivaldi_reporting_data*,lazy_ntfs,
      1179,Vivaldi Calendar,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Calendar*,lazy_ntfs,
      1180,Vivaldi Contacts,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Contacts*,lazy_ntfs,
      1181,Vivaldi Notes,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/Notes*,lazy_ntfs,
      1182,Vivaldi Download Metadata,Communications,Users/*/AppData/Local/Vivaldi/User Data/*/DownloadMetadata*,lazy_ntfs,
      1183,WBEM,WBEM,Windows/System32/wbem/Repository/**10,lazy_ntfs,
      1184,WBEM,WBEM,Windows.old/Windows/System32/wbem/Repository/**10,lazy_ntfs,
      1185,WER Files,Executables,ProgramData/Microsoft/Windows/WER/**10,lazy_ntfs,
      1186,WER Files,Executables,Users/*/AppData/Local/Microsoft/Windows/WER/**10,lazy_ntfs,
      1187,Crash Dumps,SQL Exploitation,Users/*/AppData/Local/CrashDumps/*.dmp,lazy_ntfs,
      1188,Crash Dumps,SQL Exploitation,Windows/*.dmp,lazy_ntfs,
      1189,Crash Dumps,SQL Exploitation,Windows.old/Windows/*.dmp,lazy_ntfs,
      1190,Webroot Program Data,Antivirus,ProgramData/WRData/WRLog.log,lazy_ntfs,
      1191,WhatsApp Cache,Apps,Users/*/AppData/Roaming/WhatsApp/Cache,lazy_ntfs,"Copies the cache of WhatsApp. Can be opened with Chrome Cache Viewer for viewing embedded thumbnails and other image artefacts, as well as extracting .enc message files or other files"
      1192,WhatsApp Local Storage,Apps,Users/*/AppData/Roaming/WhatsApp/Local Storage/leveldb,lazy_ntfs,"Copies the Local Storage leveldb of WhatsApp. Contains phone model and name of user, plus encrypted base64 strings which can be viewed with LevelDBDumper"
      1193,Microsoft Store WhatsApp Cache,Apps,Users/*/AppData/Local/Packages/*WhatsAppDesktop*/LocalCache/Roaming/WhatsApp/Cache,lazy_ntfs,"Copies the cache of WhatsApp. Can be opened with Chrome Cache Viewer for viewing embedded thumbnails and other image artefacts, as well as extracting .enc message files or other files"
      1194,Microsoft Store WhatsApp Local Storage,Apps,Users/*/AppData/Local/Packages/*WhatsAppDesktop*/LocalCache/Roaming/WhatsApp/Local Storage/leveldb,lazy_ntfs,"Copies the Local Storage leveldb of WhatsApp. Contains phone model and name of user, plus encrypted base64 strings which can be viewed with LevelDBDumper"
      1195,Microsoft Store WhatsApp Desktop Profile Pictures,Apps,Users/*/AppData/Local/Packages/*WhatsAppDesktop*/LocalState/profilePictures,lazy_ntfs,"Copies the local store of contacts profile pictures, simply open with a photos software"
      1196,Microsoft Store WhatsApp Shared Media,Apps,Users/*/AppData/Local/Packages/*WhatsAppDesktop*/LocalState/shared/transfers/**10/regex:.*/.(jpg|mp4|pdf|webp),ntfs,"Copies the shared media, can get very large."
      1197,DetectionHistory,Antivirus,ProgramData/Microsoft/Windows Defender/Scans/History/Service/DetectionHistory/*/**10,lazy_ntfs,
      1198,WinSCP (.ini file),Logs,**10/WinSCP.ini,lazy_ntfs,
      1199,Windows Defender Logs,Antivirus,ProgramData/Microsoft/Microsoft AntiMalware/Support/**10,lazy_ntfs,
      1200,Windows Defender Event Logs,EventLogs,Windows/System32/winevt/Logs/Microsoft-Windows-Windows Defender*.evtx,lazy_ntfs,
      1201,Windows Defender Event Logs,EventLogs,Windows.old/Windows/System32/winevt/Logs/Microsoft-Windows-Windows Defender*.evtx,lazy_ntfs,
      1202,Windows Defender Logs,Antivirus,ProgramData/Microsoft/Windows Defender/Support/**10,lazy_ntfs,
      1203,Windows Defender Logs,Antivirus,Windows/Temp/MpCmdRun.log,lazy_ntfs,
      1204,Windows Defender Logs,Antivirus,Windows.old/Windows/Temp/MpCmdRun.log,lazy_ntfs,
      1205,DetectionHistory,Antivirus,ProgramData/Microsoft/Windows Defender/Scans/History/Service/DetectionHistory/*/**10,lazy_ntfs,
      1206,Windows Defender Quarantine,Antivirus,ProgramData/Microsoft/Windows Defender/Quarantine/**10,lazy_ntfs,
      1207,Windows Firewall Logs,WindowsFirewallLogs,Windows/System32/LogFiles/Firewall/pfirewall.*,lazy_ntfs,
      1208,Windows Firewall Logs,WindowsFirewallLogs,Windows.old/Windows/System32/LogFiles/Firewall/pfirewall.*,lazy_ntfs,
      1209,Cryptokeys,Windows Hello,Windows/ServiceProfiles/LocalService/AppData/Roaming/Microsoft/Crypto/Keys/**10,lazy_ntfs,
      1210,Masterkey,Windows Hello,Windows/System32/Microsoft/Protect/S-1-5-18/User/**10,lazy_ntfs,
      1211,NGC,Windows Hello,Windows/ServiceProfiles/LocalService/AppData/Local/Microsoft/Ngc/**10,lazy_ntfs,
      1212,SECURITY registry transaction files,Registry,Windows/System32/config/SECURITY.LOG*,lazy_ntfs,
      1213,SECURITY registry transaction files,Registry,Windows.old/Windows/System32/config/SECURITY.LOG*,lazy_ntfs,
      1214,SOFTWARE registry transaction files,Registry,Windows/System32/config/SOFTWARE.LOG*,lazy_ntfs,
      1215,SOFTWARE registry transaction files,Registry,Windows.old/Windows/System32/config/SOFTWARE.LOG*,lazy_ntfs,
      1216,SYSTEM registry transaction files,Registry,Windows/System32/config/SYSTEM.LOG*,lazy_ntfs,
      1217,SYSTEM registry transaction files,Registry,Windows.old/Windows/System32/config/SYSTEM.LOG*,lazy_ntfs,
      1218,SECURITY registry hive,Registry,Windows/System32/config/SECURITY,lazy_ntfs,
      1219,SECURITY registry hive,Registry,Windows.old/Windows/System32/config/SECURITY,lazy_ntfs,
      1220,SOFTWARE registry hive,Registry,Windows/System32/config/SOFTWARE,lazy_ntfs,
      1221,SOFTWARE registry hive,Registry,Windows.old/Windows/System32/config/SOFTWARE,lazy_ntfs,
      1222,SYSTEM registry hive,Registry,Windows/System32/config/SYSTEM,lazy_ntfs,
      1223,SYSTEM registry hive,Registry,Windows.old/Windows/System32/config/SYSTEM,lazy_ntfs,
      1224,SECURITY registry hive (RegBack),Registry,Windows/System32/config/RegBack/SECURITY,lazy_ntfs,
      1225,SECURITY registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SECURITY,lazy_ntfs,
      1226,SOFTWARE registry hive (RegBack),Registry,Windows/System32/config/RegBack/SOFTWARE,lazy_ntfs,
      1227,SOFTWARE registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SOFTWARE,lazy_ntfs,
      1228,SYSTEM registry hive (RegBack),Registry,Windows/System32/config/RegBack/SYSTEM,lazy_ntfs,
      1229,SYSTEM registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SYSTEM,lazy_ntfs,
      1230,SYSTEM registry hive (RegBack),Registry,Windows/System32/config/RegBack/SYSTEM1,lazy_ntfs,
      1231,SYSTEM registry hive (RegBack),Registry,Windows.old/Windows/System32/config/RegBack/SYSTEM1,lazy_ntfs,
      1232,WindowsIndexSearch,FileKnowledge,programdata/microsoft/search/data/applications/windows/*,lazy_ntfs,
      1233,GatherLogs,FileKnowledge,programdata/microsoft/search/data/applications/windows/GatherLogs/**10,lazy_ntfs,
      1234,Network setting files,Misc,windows/system32/drivers/etc/**10,lazy_ntfs,
      1235,Windows 10 Notification DB,Notifications,Users/*/AppData/Local/Microsoft/Windows/Notifications/wpndatabase.db,lazy_ntfs,
      1236,Windows 10 Notification DB,Notifications,Users/*/AppData/Local/Microsoft/Windows/Notifications/appdb.dat,lazy_ntfs,
      1237,MigLog.xml,OS Upgrade,Windows/Panther/MigLog.xml,lazy_ntfs,
      1238,Setupact.log,OS Upgrade,Windows/Panther/Setupact.log,lazy_ntfs,
      1239,HumanReadable.xml,OS Upgrade,Windows/Panther/*HumanReadable.xml,lazy_ntfs,
      1240,FolderMoveLog.txt,OS Upgrade,Windows/Panther/Rollback/FolderMoveLog.txt,lazy_ntfs,
      1241,Update Store.db,OS Upgrade,ProgramData/USOPrivate/UpdateStore/store.db,lazy_ntfs,
      1242,Windows Power Diagnostics,Diagnostics,ProgramData/Microsoft/Windows/Power Efficiency Diagnostics/**10,lazy_ntfs,
      1243,DNS Netlogon files,DNS,Windows/System32/config/**10/netlogon.*,lazy_ntfs,
      1244,DNS files,DNS,Windows/System32/dns/**10,lazy_ntfs,
      1245,DHCP files,DHCP,Windows/System32/dhcp/**10,lazy_ntfs,
      1246,Diagnostic Logs for WSA,Windows Subsystem for Android,Users/*/AppData/Local/Packages/MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe/LocalState/diagnostics/logcat/*.log,lazy_ntfs,Filenames should be %timestamp%.log
      1247,App download artifacts (PNG),Windows Subsystem for Android,Users/*/AppData/Local/Packages/MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe/LocalCache/*.png,lazy_ntfs,Will provide examiners with indicators of which apps were downloaded
      1248,App download artifacts (ICO),Windows Subsystem for Android,Users/*/AppData/Local/Packages/MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe/LocalCache/*.ico,lazy_ntfs,Will provide examiners with indicators of which apps were downloaded WHEN since .ico files appear immediately when download of an application completes
      1249,Appcompatdb.json,Windows Subsystem for Android,Users/*/AppData/Local/Packages/MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe/LocalState/appcompatdb.json,lazy_ntfs,"Grabs the appcompatdb.json, unknown exactly what this is but further relevance could be uncovered after more research is conducted"
      1250,userdata.vhdx,Windows Subsystem for Android,Users/*/AppData/Local/Packages/MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe/LocalCache/userdata.vhdx,lazy_ntfs,Grabs the user's data which appears to be stored in a VHDX
      1251,Legacy .rbs files relating to Windows Telemetry and Diagnostics,SystemEvents,ProgramData/Microsoft/Diagnosis/events*.rbs,lazy_ntfs,
      1252,Legacy .rbs files relating to Windows Telemetry and Diagnostics,SystemEvents,Windows.old/ProgramData/Microsoft/Diagnosis/events*.rbs,lazy_ntfs,
      1253,ActivitiesCache.db,FileFolderAccess,Users/*/AppData/Local/ConnectedDevicesPlatform/*/ActivitiesCache.db*,lazy_ntfs,
      1254,Windows Update Session Orchestrator logs,EventLogs,ProgramData/USOShared/Logs/System/**10/*.etl,lazy_ntfs,
      1255,Windows Update logs,EventLogs,Windows/Logs/WindowsUpdate/**10/WindowsUpdate*.etl,lazy_ntfs,
      1256,Windows Component-Based Servicing logs,EventLogs,Windows/Logs/CBS/**10/CBS*.log,lazy_ntfs,
      1257,Windows Your Phone - All Databases,Apps,Users/*/AppData/Local/Packages/Microsoft.YourPhone_8wekyb3d8bbwe/LocalCache/Indexed/**10,lazy_ntfs,Locates all Your Phone database files
      1258,System Volume Information,Folder capture,System Volume Information/**10,lazy_ntfs,
      1259,XYplorer - .ini file,Apps,Users/*/AppData/Roaming/XYplorer/XYplorer.ini,lazy_ntfs,Locates .ini file associated with Total Commander which stores useful user activity information.
      1260,XYplorer - .ini file for each respective pane,Apps,Users/*/AppData/Roaming/XYplorer/Panes/*/**10/pane.ini,lazy_ntfs,Locates the .ini file for the left and right pane.
      1261,XYplorer - AutoBackup folder,Apps,Users/*/AppData/Roaming/XYplorer/AutoBackup/**10,lazy_ntfs,Locates the AutoBackup folder and copies its contents.
      1262,XYplorer - .dat files,Apps,Users/*/AppData/Roaming/XYplorer/**10/*.dat,lazy_ntfs,"Locates the .dat files in the XYplorer's AppData folder, all of which are updated upon program's exit."
      1263,Xeox RMM Client Application logs,ApplicationLogs,Program Files/Xeox/*.log,lazy_ntfs,Contains Application Log entries such as service start and incomming connections.
      1264,Yandex Cookies,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/**10/Cookies*,lazy_ntfs,
      1265,Yandex Network Persistent State,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/**10/Network Persistent State,lazy_ntfs,
      1266,Yandex Favicons,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Favicons*,lazy_ntfs,
      1267,Yandex History,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/History*,lazy_ntfs,
      1268,Yandex Sessions Folder,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Sessions/*,lazy_ntfs,
      1269,Yandex Login Data,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Ya Passman Data*,lazy_ntfs,
      1270,Yandex Network Action Predictor,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Network Action Predictor,lazy_ntfs,
      1271,Yandex Preferences,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Preferences,lazy_ntfs,
      1272,Yandex Top Sites,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Top Sites*,lazy_ntfs,
      1273,Yandex Bookmarks,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Bookmarks*,lazy_ntfs,
      1274,Yandex Visited Links,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Visited Links,lazy_ntfs,
      1275,Yandex Web Data,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Web Data*,lazy_ntfs,
      1276,Yandex Autofill data,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Ya Autofill Data*,lazy_ntfs,
      1277,Yandex Passman logs,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Passman Logs*,lazy_ntfs,
      1278,Yandex Shortcuts,Communications,Users/*/AppData/Local/Yandex/YandexBrowser/User Data/*/Shortcuts*,lazy_ntfs,
      1279,Zoho Assist log files in AppData\Local,Apps,Users/*/AppData/Local/ZohoMeeting/log/**10,lazy_ntfs,Zoho Assist log files in AppData
      ocal
      1280,Zoho Assist .conf files in AppData\Local,Apps,Users/*/AppData/Local/ZohoMeeting/*.conf,lazy_ntfs,Grabs all .conf files present in this folder (Connection/Settings)
      1281,Zoho Assist log files in ProgramData,Apps,ProgramData/ZohoMeeting/log/**10,lazy_ntfs,Zoho Assist log files in ProgramData
      1282,Zoho Assist .conf files,Apps,ProgramData/ZohoMeeting/**10/*.conf,lazy_ntfs,Grabs all .conf files present in this folder (Connection/Proxy/Settings)
      1283,Zoho Assist log files in Program Files*,Apps,Program Files*/ZohoMeeting/UnAttended/ZohoMeeting/logs/**10,lazy_ntfs,Zoho Assist log files in Program Files*
      1284,Zoho Assist .conf files in  Program Files*,Apps,Program Files*/ZohoMeeting/UnAttended/ZohoMeeting/*.conf,lazy_ntfs,Grabs all .conf files present in this folder (Service/Settings)
      1285,Zoho Assist .txt files in  Program Files*,Apps,Program Files*/ZohoMeeting/UnAttended/ZohoMeeting/*.txt,lazy_ntfs,Grabs all .txt files present in this folder (Service/Settings)
      1286,Zoom client logs,Apps,Users/*/AppData/Roaming/Zoom/logs/**10/*,lazy_ntfs,Zoom client artifacts
      1287,Zoom client logs (Windows XP),Apps,Documents and Settings/*/Application Data/Zoom/**10/*,lazy_ntfs,Zoom client artifacts (Windows XP)
      1288,Zoom client recordings,Apps,Users/*/Documents/Zoom/**10/*,lazy_ntfs,Zoom recording artifacts
      1289,Zoom plugin (Outlook),Apps,Users/*/AppData/Roaming/Zoom Plugin/*.json,lazy_ntfs,Zoom plugin artifacts
      1290,iTunes Backup Folder,Communications,Users/*/AppData/Roaming/Apple/Mobilesync/Backup/**10,lazy_ntfs,
      1291,iTunes Backup Folder,Communications,Users/*/AppData/Roaming/Apple Computer/Mobilesync/Backup/**10,lazy_ntfs,
      1292,iTunes Backup Folder - iOS13,Communications,Users/*/Apple/Mobilesync/Backup/**10,lazy_ntfs,
      1293,mIRC Chat Logs (Vista+),Communications,Users/*/AppData/Roaming/mIRC/logs/**10,lazy_ntfs,
      1294,mIRC Chat Logs (2000/XP),Communications,Documents and Settings/*/Application Data/mIRC/logs/**10,lazy_ntfs,
      1295,mRemoteNG Logs,Communications,Users/*/AppData/Roaming/mRemoteNG/mRemoteNG.log,lazy_ntfs,Contains log entries for remote connections
      1296,mRemoteNG Connection Configuration and Backups,Communications,Users/*/AppData/Roaming/mRemoteNG/confCons.xml*,lazy_ntfs,"Contains connection config, often with obfuscated credentials"
      1297,mRemoteNG Program Settings,Communications,Users/*/AppData/*/mRemoteNG/**10/user.config,lazy_ntfs,Contains user-specific program settings
      1298,openSUSE WSL /etc/os-release,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/os-release,lazy_ntfs,
      1299,openSUSE WSL /etc/fstab,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/fstab,lazy_ntfs,
      1300,openSUSE WSL /etc/passwd,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/passwd,lazy_ntfs,
      1301,openSUSE WSL /etc/group,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/group,lazy_ntfs,
      1302,openSUSE WSL /etc/shadow,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/shadow,lazy_ntfs,
      1303,openSUSE WSL /etc/timezone,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/timezone,lazy_ntfs,
      1304,openSUSE WSL /etc/hostname,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/hostname,lazy_ntfs,
      1305,openSUSE WSL /etc/hosts,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/hosts,lazy_ntfs,
      1306,openSUSE WSL /etc/bash.bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/bash.bashrc,lazy_ntfs,
      1307,openSUSE WSL /etc/profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/etc/profile,lazy_ntfs,
      1308,openSUSE WSL .bash_history,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/**10/.bash_history,lazy_ntfs,
      1309,openSUSE WSL .bashrc,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/**10/.bashrc,lazy_ntfs,
      1310,openSUSE WSL .profile,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/rootfs/**10/.profile,lazy_ntfs,
      1311,openSUSE WSL ext4.vhdx,Windows Subsystem for Linux,Users/*/AppData/Local/Packages/46932SUSE.openSUSE*Leap*/LocalState/ext4.vhdx,lazy_ntfs,
      1312,pCloud Database,Apps,Users/*/AppData/Local/pCloud/*.db,lazy_ntfs,Database contains all files sync'd with pCloud account.
      1313,pCloud Database WAL File,Apps,Users/*/AppData/Local/pCloud/*.db-wal,lazy_ntfs,Write-Ahead Log for pCloud database file.
      1314,pCloud Database Shared Memory File,Apps,Users/*/AppData/Local/pCloud/*.db-shm,lazy_ntfs,Shared Memory for the pCloud database file.
      1315,TorrentClients - qBittorrent,FileDownload,Users/*/AppData/Roaming/qBittorrent/*.ini,lazy_ntfs,
      1316,TorrentClients - qBittorrent,FileDownload,Users/*/AppData/Local/qBittorrent/logs/*,lazy_ntfs,
      1317,TorrentClients - qBittorrent,FileDownload,Users/*/AppData/Local/qBittorrent/GeoDB/*,lazy_ntfs,Locate .mmdb file for network peer connection analysis.
      1318,TorrentClients - qBittorrent,FileDownload,Users/*/AppData/Local/qBittorrent/BT_backup/*,lazy_ntfs,Locate active (in-progress) torrent files.
      1319,TorrentClients - uTorrent,FileDownload,Users/*/AppData/Roaming/uTorrent/*.dat,lazy_ntfs,
  - name: KapeTargets
    type: hidden
    description: Each parameter above represents a group of rules to be triggered. This table specifies which rule IDs will be included when the parameter is checked.
    default: |
      Group,RuleIds
      _BasicCollection,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 36, 37, 38, 39, 51, 279, 280, 281, 490, 491, 492, 493, 494, 495, 496, 497, 638, 643, 644, 676, 677, 681, 682, 683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763, 969, 970, 971, 972, 973, 974, 991, 992, 993, 994, 995, 996, 997, 1067, 1068, 1079, 1105, 1106, 1107, 1232, 1233]"
      _KapeTriage,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 18, 19, 20, 21, 22, 23, 24, 29, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 51, 58, 59, 60, 61, 69, 70, 71, 72, 73, 74, 75, 76, 77, 82, 83, 84, 85, 86, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 167, 170, 171, 172, 173, 174, 175, 177, 223, 224, 225, 226, 227, 228, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260, 262, 279, 280, 281, 308, 309, 310, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 374, 375, 391, 392, 393, 404, 405, 406, 407, 408, 409, 410, 411, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 476, 477, 478, 479, 480, 481, 482, 483, 484, 490, 491, 492, 493, 494, 495, 496, 497, 498, 510, 511, 518, 519, 520, 521, 525, 526, 527, 528, 529, 530, 567, 568, 569, 570, 571, 572, 601, 602, 625, 626, 638, 643, 644, 647, 648, 649, 650, 651, 652, 653, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 673, 674, 675, 676, 677, 681, 682, 683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763, 764, 765, 853, 854, 855, 969, 970, 971, 972, 973, 974, 975, 976, 991, 992, 993, 994, 995, 996, 997, 998, 999, 1000, 1001, 1002, 1026, 1027, 1031, 1032, 1056, 1057, 1058, 1059, 1060, 1061, 1062, 1063, 1064, 1065, 1066, 1067, 1068, 1072, 1073, 1074, 1075, 1092, 1093, 1102, 1103, 1104, 1125, 1126, 1127, 1128, 1130, 1131, 1132, 1133, 1140, 1141, 1142, 1166, 1167, 1168, 1169, 1170, 1171, 1172, 1173, 1174, 1175, 1176, 1177, 1178, 1179, 1180, 1181, 1182, 1183, 1184, 1185, 1186, 1187, 1188, 1189, 1190, 1199, 1200, 1201, 1202, 1203, 1204, 1205, 1206, 1253, 1263, 1264, 1265, 1266, 1267, 1268, 1269, 1270, 1271, 1272, 1273, 1274, 1275, 1276, 1277, 1278, 1279, 1280, 1281, 1282, 1283, 1284, 1285, 1295, 1296, 1297]"
      _SANS_Triage,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 18, 19, 20, 21, 22, 23, 24, 29, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 51, 58, 59, 60, 61, 69, 70, 71, 72, 73, 74, 75, 76, 77, 80, 82, 83, 84, 85, 86, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 163, 167, 170, 171, 172, 173, 174, 175, 177, 213, 214, 223, 224, 225, 226, 227, 228, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260, 262, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 308, 309, 310, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 374, 375, 380, 381, 382, 383, 384, 385, 386, 387, 390, 391, 392, 393, 404, 405, 406, 407, 408, 409, 410, 411, 412, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 476, 477, 478, 479, 480, 481, 482, 483, 484, 490, 491, 492, 493, 494, 495, 496, 497, 498, 510, 511, 518, 519, 520, 521, 524, 525, 526, 527, 528, 529, 530, 547, 548, 549, 550, 551, 560, 561, 567, 568, 569, 570, 571, 572, 601, 602, 625, 626, 638, 643, 644, 647, 648, 649, 650, 651, 652, 653, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 673, 674, 675, 676, 677, 681, 682, 683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763, 764, 765, 853, 854, 855, 969, 970, 971, 972, 973, 974, 975, 976, 991, 992, 993, 994, 995, 996, 997, 998, 999, 1000, 1001, 1002, 1006, 1007, 1008, 1009, 1012, 1013, 1014, 1015, 1016, 1017, 1018, 1019, 1020, 1021, 1022, 1023, 1026, 1027, 1031, 1032, 1056, 1057, 1058, 1059, 1060, 1061, 1062, 1063, 1064, 1065, 1066, 1067, 1068, 1072, 1073, 1074, 1075, 1076, 1077, 1079, 1092, 1093, 1102, 1103, 1104, 1105, 1106, 1107, 1125, 1126, 1127, 1128, 1130, 1131, 1132, 1133, 1140, 1141, 1142, 1143, 1144, 1145, 1146, 1147, 1166, 1167, 1168, 1169, 1170, 1171, 1172, 1173, 1174, 1175, 1176, 1177, 1178, 1179, 1180, 1181, 1182, 1183, 1184, 1185, 1186, 1187, 1188, 1189, 1190, 1191, 1192, 1193, 1194, 1199, 1200, 1201, 1202, 1203, 1204, 1205, 1206, 1207, 1208, 1232, 1233, 1253, 1263, 1264, 1265, 1266, 1267, 1268, 1269, 1270, 1271, 1272, 1273, 1274, 1275, 1276, 1277, 1278, 1279, 1280, 1281, 1282, 1283, 1284, 1285, 1293, 1294, 1295, 1296, 1297]"
      _Boot,[1]
      _J,"[2, 3, 4, 5]"
      _LogFile,[6]
      _MFT,[7]
      _MFTMirr,[8]
      _SDS,"[9, 10]"
      _T,"[11, 12]"
      1Password,"[13, 14, 15]"
      4KVideoDownloader,"[16, 17]"
      AVG,"[18, 19, 20, 21, 22, 23, 24]"
      AceText,[25]
      AcronisTrueImage,"[26, 27, 28]"
      Action1,[29]
      ActiveDirectoryNTDS,[30]
      ActiveDirectorySysvol,[31]
      AgentRansack,"[32, 33, 34, 35]"
      Amcache,"[36, 37, 38, 39]"
      Ammyy,[40]
      Antivirus,"[18, 19, 20, 21, 22, 23, 24, 58, 59, 60, 61, 69, 70, 71, 72, 73, 74, 75, 76, 77, 82, 83, 84, 167, 170, 171, 172, 173, 174, 175, 231, 232, 233, 234, 235, 236, 262, 308, 309, 310, 391, 392, 393, 518, 519, 520, 521, 525, 526, 527, 528, 529, 530, 853, 976, 1001, 1002, 1026, 1027, 1058, 1059, 1060, 1061, 1062, 1063, 1064, 1065, 1066, 1092, 1093, 1102, 1103, 1104, 1130, 1131, 1132, 1133, 1190, 1199, 1200, 1201, 1202, 1203, 1204, 1205, 1206]"
      AnyDesk,"[41, 42, 43, 44, 45, 46, 47, 48, 49]"
      ApacheAccessLog,[50]
      AppCompatPCA,[51]
      AppData,[52]
      AppXPackages,"[53, 54, 55, 56, 57]"
      ApplicationEvents,"[58, 59, 60, 61]"
      AsperaConnect,"[62, 63]"
      AteraAgent,"[64, 65, 66, 67, 68]"
      Avast,"[69, 70, 71, 72, 73, 74]"
      AviraAVLogs,"[75, 76, 77]"
      BCD,"[78, 79]"
      BITS,[80]
      BitTorrent,[81]
      Bitdefender,"[82, 83, 84]"
      BoxDrive_Metadata,"[85, 86]"
      BoxDrive_UserFiles,"[87, 88]"
      BraveBrowser,"[89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108]"
      BrowserCache,"[109, 110, 111, 112, 113, 114, 115, 116]"
      CertUtil,"[117, 118, 119]"
      Chrome,"[120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159]"
      ChromeExtensions,"[160, 161]"
      ChromeFileSystem,[162]
      CiscoJabber,[163]
      ClipboardMaster,"[164, 165, 166]"
      CloudStorage_All,"[85, 86, 87, 88, 223, 224, 225, 226, 227, 228, 229, 373, 374, 375, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 601, 602, 603, 675, 1051, 1052, 1053, 1312, 1313, 1314]"
      CloudStorage_Metadata,"[85, 86, 223, 224, 225, 226, 227, 228, 374, 375, 601, 602, 675]"
      CloudStorage_OneDriveExplorer,"[601, 602, 678, 679, 680, 681, 682, 755, 756, 757, 758, 759, 760, 761, 762, 763]"
      CombinedLogs,"[279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 560, 561, 638, 1105, 1106, 1107, 1207, 1208]"
      Combofix,[167]
      ConfluenceLogs,"[168, 169]"
      Cybereason,"[170, 171, 172]"
      Cylance,"[173, 174, 175]"
      DC__,[176]
      DWAgent,[177]
      Debian,"[178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195]"
      DirectoryOpus,"[196, 197, 198, 199, 200, 201, 202, 203, 204]"
      DirectoryTraversal_AudioFiles,[205]
      DirectoryTraversal_ExcelDocuments,[206]
      DirectoryTraversal_PDFDocuments,[207]
      DirectoryTraversal_PictureFiles,[208]
      DirectoryTraversal_SQLiteDatabases,[209]
      DirectoryTraversal_VideoFiles,[210]
      DirectoryTraversal_WildCardExample,[211]
      DirectoryTraversal_WordDocuments,[212]
      Discord,"[213, 214]"
      DoubleCommander,"[215, 216, 217, 218, 219, 220, 221]"
      Drivers,[222]
      Dropbox_Metadata,"[223, 224, 225, 226, 227, 228]"
      Dropbox_UserFiles,[229]
      EFCommander,[230]
      ESET,"[231, 232, 233, 234, 235, 236]"
      Edge,[237]
      EdgeChromium,"[238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260]"
      EdgeChromiumExtensions,[261]
      Emsisoft,[262]
      EncapsulationLogging,"[263, 264, 265, 266]"
      EventLogs_RDP,"[267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278]"
      EventLogs,"[279, 280, 281]"
      EventTraceLogs,"[282, 283, 284, 285, 286, 287, 288, 289, 290, 291]"
      EventTranscriptDB,"[292, 293, 294]"
      Evernote,"[295, 296, 297]"
      Everything__VoidTools_,"[298, 299, 300, 301]"
      EvidenceOfExecution,"[36, 37, 38, 39, 51, 643, 644, 676, 677, 1067, 1068]"
      Exchange,"[302, 307]"
      ExchangeClientAccess,[302]
      ExchangeCve_2021_26855,"[303, 304, 305, 306]"
      ExchangeTransport,[307]
      FSecure,"[308, 309, 310]"
      FTPClients,"[312, 313, 314, 315, 1198]"
      Fences,[311]
      FileExplorerReplacements,"[196, 197, 198, 199, 200, 201, 202, 203, 204, 215, 216, 217, 218, 219, 220, 221, 230, 351, 352, 353, 354, 355, 356, 357, 554, 555, 556, 557, 558, 559, 599, 600, 656, 657, 1030, 1069, 1070, 1071, 1094, 1095, 1096, 1097, 1098, 1099, 1100, 1259, 1260, 1261, 1262]"
      FileSystem,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12]"
      FileZillaClient,"[312, 313]"
      FileZillaServer,"[314, 315]"
      Firefox,"[316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350]"
      FreeCommander,"[351, 352, 353, 354, 355, 356, 357]"
      FreeDownloadManager,"[358, 359, 360]"
      FreeFileSync,[361]
      Freenet,"[362, 363, 364, 365, 366]"
      FrostWire,"[367, 368, 369]"
      Gigatribe,"[370, 371, 372]"
      GoogleDriveBackupSync_UserFiles,[373]
      GoogleDrive_Metadata,"[374, 375]"
      GoogleEarth,"[376, 377, 378, 379]"
      GroupPolicy,"[380, 381, 382, 383, 384, 385, 386, 387]"
      HeidiSQL,"[388, 389]"
      HexChat,[390]
      HitmanPro,"[391, 392, 393]"
      IISConfiguration,"[394, 395, 396, 397]"
      IISLogFiles,"[398, 399, 400, 401, 402, 403]"
      IRCClients,"[390, 412, 1293, 1294]"
      ISLOnline,"[404, 405, 406, 407, 408, 409, 410, 411]"
      IceChat,[412]
      Idrive,"[413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426]"
      ImgBurn,[427]
      InternetExplorer,"[428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440]"
      IrfanView,[441]
      JDownloader2,"[442, 443, 444, 445, 446]"
      JavaWebCache,"[447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457]"
      Kali,"[458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475]"
      KapeTriage,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 18, 19, 20, 21, 22, 23, 24, 29, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 51, 58, 59, 60, 61, 69, 70, 71, 72, 73, 74, 75, 76, 77, 82, 83, 84, 85, 86, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 167, 170, 171, 172, 173, 174, 175, 177, 223, 224, 225, 226, 227, 228, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260, 262, 279, 280, 281, 308, 309, 310, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 374, 375, 391, 392, 393, 404, 405, 406, 407, 408, 409, 410, 411, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 476, 477, 478, 479, 480, 481, 482, 483, 484, 490, 491, 492, 493, 494, 495, 496, 497, 498, 510, 511, 518, 519, 520, 521, 525, 526, 527, 528, 529, 530, 567, 568, 569, 570, 571, 572, 601, 602, 625, 626, 638, 643, 644, 647, 648, 649, 650, 651, 652, 653, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 673, 674, 675, 676, 677, 681, 682, 683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763, 764, 765, 853, 854, 855, 969, 970, 971, 972, 973, 974, 975, 976, 991, 992, 993, 994, 995, 996, 997, 998, 999, 1000, 1001, 1002, 1026, 1027, 1031, 1032, 1056, 1057, 1058, 1059, 1060, 1061, 1062, 1063, 1064, 1065, 1066, 1067, 1068, 1072, 1073, 1074, 1075, 1092, 1093, 1102, 1103, 1104, 1125, 1126, 1127, 1128, 1130, 1131, 1132, 1133, 1140, 1141, 1142, 1166, 1167, 1168, 1169, 1170, 1171, 1172, 1173, 1174, 1175, 1176, 1177, 1178, 1179, 1180, 1181, 1182, 1183, 1184, 1185, 1186, 1187, 1188, 1189, 1190, 1199, 1200, 1201, 1202, 1203, 1204, 1205, 1206, 1253, 1263, 1264, 1265, 1266, 1267, 1268, 1269, 1270, 1271, 1272, 1273, 1274, 1275, 1276, 1277, 1278, 1279, 1280, 1281, 1282, 1283, 1284, 1285, 1295, 1296, 1297]"
      Kaseya,"[476, 477, 478, 479, 480, 481, 482, 483, 484]"
      Keepass,"[485, 486, 487]"
      KeepassXC,"[488, 489]"
      LNKFilesAndJumpLists,"[490, 491, 492, 493, 494, 495, 496, 497]"
      Level,[498]
      LinuxOnWindowsProfileFiles,"[499, 500, 501, 502]"
      LiveUserFiles,"[503, 504, 505, 506]"
      LogFiles,"[507, 508, 509]"
      LogMeIn,"[58, 59, 60, 61, 510, 511]"
      MOF,[512]
      MSSQLErrorLog,"[513, 514]"
      MacriumReflect,"[515, 516, 517]"
      Malwarebytes,"[518, 519, 520, 521]"
      ManageEngineLogs,"[522, 523]"
      Mattermost,[524]
      McAfee,"[525, 526, 527, 528, 529]"
      McAfee_ePO,[530]
      MediaMonkey,"[531, 532]"
      Megasync,[533]
      MemoryFiles,"[534, 535, 536, 537, 538]"
      MessagingClients,"[163, 213, 214, 390, 412, 524, 547, 548, 549, 550, 551, 1006, 1007, 1008, 1009, 1012, 1013, 1014, 1015, 1016, 1017, 1018, 1019, 1020, 1021, 1022, 1023, 1076, 1077, 1143, 1144, 1145, 1146, 1147, 1191, 1192, 1193, 1194, 1293, 1294]"
      MicrosoftOfficeBackstage,[539]
      MicrosoftOneNote,"[540, 541, 542, 543, 544]"
      MicrosoftStickyNotes,"[545, 546]"
      MicrosoftTeams,"[547, 548, 549, 550, 551]"
      MicrosoftToDo,"[552, 553]"
      MidnightCommander,[554]
      MiniTimelineCollection,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 279, 280, 281, 683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763]"
      MultiCommander,"[555, 556, 557, 558, 559]"
      NETCLRUsageLogs,"[560, 561]"
      NGINXLogs,[562]
      NZBGet,"[563, 564]"
      Nessus,"[565, 566]"
      NetMonitorforEmployeesProfessional,"[567, 568, 569, 570, 571, 572]"
      NewsbinPro,[573]
      Newsleecher,[574]
      Nicotine__,"[575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585]"
      Notepad__,"[586, 587, 588]"
      Notepad,[589]
      Notion,"[590, 591]"
      OfficeAutosave,"[592, 593, 594, 595]"
      OfficeDiagnostics,"[596, 597]"
      OfficeDocumentCache,[598]
      OneCommander,"[599, 600]"
      OneDrive_Metadata,"[601, 602]"
      OneDrive_UserFiles,[603]
      OpenSSHClient,"[604, 605, 606, 607, 608, 609, 610, 611, 612]"
      OpenSSHServer,"[613, 614, 615, 616, 617, 618, 619, 620, 621]"
      OpenVPNClient,"[622, 623, 624]"
      Opera,"[625, 626]"
      OutlookPSTOST,"[627, 628, 629, 630, 631, 632, 633, 634]"
      P2PClients,"[176, 367, 368, 369, 370, 371, 372, 1004, 1028, 1029]"
      PeaZip,[635]
      PerfLogs,[636]
      PowerShell7Config,[637]
      PowerShellConsole,[638]
      PowerShellTranscripts,"[639, 640, 641, 642]"
      Prefetch,"[643, 644]"
      ProgramData,[645]
      ProtonVPN,[646]
      PuffinSecureBrowser,"[647, 648, 649, 650, 651, 652, 653]"
      PushNotification,"[654, 655]"
      Q_Dir,"[656, 657]"
      QFinderPro__QNAP_,[658]
      RDPCache,"[659, 660, 661]"
      RDPLogs,"[662, 663, 664, 665, 666, 667, 668, 669]"
      Radmin,"[670, 671, 672, 673, 674]"
      RcloneConf,[675]
      RecentFileCache,"[676, 677]"
      RecycleBin,"[678, 679, 680, 681, 682]"
      RecycleBin_DataFiles,"[678, 679, 680]"
      RecycleBin_InfoFiles,"[681, 682]"
      RegistryHives,"[683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763]"
      RegistryHivesMSIXApps,"[683, 684, 685]"
      RegistryHivesOther,"[686, 687, 688, 689, 690, 691, 692, 693, 694, 695, 696, 697, 698, 699, 700, 701, 702, 703, 704, 705, 706, 707, 708, 709, 710, 711, 712, 713]"
      RegistryHivesSystem,"[714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754]"
      RegistryHivesUser,"[755, 756, 757, 758, 759, 760, 761, 762, 763]"
      RemoteAdmin,"[29, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 58, 59, 60, 61, 177, 404, 405, 406, 407, 408, 409, 410, 411, 476, 477, 478, 479, 480, 481, 482, 483, 484, 498, 510, 511, 567, 568, 569, 570, 571, 572, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 673, 674, 764, 765, 854, 855, 998, 999, 1000, 1031, 1032, 1056, 1057, 1072, 1073, 1074, 1075, 1125, 1126, 1127, 1128, 1140, 1141, 1142, 1263, 1279, 1280, 1281, 1282, 1283, 1284, 1285, 1295, 1296, 1297]"
      RemoteUtilities_app,"[764, 765]"
      RoamingProfile,"[766, 767, 768, 769, 770, 771, 772, 773, 774, 775, 776, 777, 778, 779, 780, 781, 782, 783, 784, 785, 786, 787, 788, 789, 790, 791, 792, 793, 794, 795, 796, 797, 798, 799, 800, 801, 802, 803, 804, 805, 806, 807, 808, 809, 810, 811, 812, 813, 814, 815, 816, 817, 818, 819, 820, 821, 822, 823, 824, 825, 826, 827, 828, 829, 830, 831, 832, 833, 834, 835, 836, 837, 838]"
      Robo_FTP,"[839, 840, 841, 842, 843, 844, 845, 846, 847, 848, 849, 850, 851, 852]"
      RogueKiller,[853]
      RustDesk,"[854, 855]"
      SABnbzd,"[856, 857]"
      SCCMClientLogs,[858]
      SDB,"[859, 860, 861, 862]"
      SOFELK,"[1, 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 36, 37, 38, 39, 51, 279, 280, 281, 490, 491, 492, 493, 494, 495, 496, 497, 643, 644, 676, 677, 1067, 1068]"
      SQLiteDatabases,"[863, 864, 865, 866, 867, 868, 869, 870, 871, 872, 873, 874, 875, 876, 877, 878, 879, 880, 881, 882, 883, 884, 885, 886, 887, 888, 889, 890, 891, 892, 893, 894, 895, 896, 897, 898, 899, 900, 901, 902, 903, 904, 905, 906, 907, 908, 909, 910, 911, 912, 913, 914, 915, 916, 917, 918, 919, 920, 921, 922, 923, 924, 925, 926, 927, 928, 929, 930, 931, 932, 933, 934, 935, 936, 937, 938, 939, 940, 941, 942, 943, 944, 945, 946, 947, 948, 949, 950, 951, 952, 953, 954, 955, 956, 957, 958, 959, 960, 961, 962, 963, 964, 965, 966, 967, 968]"
      SRUM,"[969, 970, 971, 972, 973, 974]"
      SUM,[975]
      SUPERAntiSpyware,[976]
      SUSELinuxEnterpriseServer,"[977, 978, 979, 980, 981, 982, 983, 984, 985, 986, 987, 988, 989, 990]"
      ScheduledTasks,"[991, 992, 993, 994, 995, 996, 997]"
      ScreenConnect,"[58, 59, 60, 61, 998, 999, 1000]"
      SecureAge,[1001]
      SentinelOne,[1002]
      ServerTriage,"[50, 168, 169, 302, 307, 314, 315, 398, 399, 400, 401, 402, 403, 513, 514, 522, 523, 562, 613, 614, 615, 616, 617, 618, 619, 620, 621]"
      ShareX,[1003]
      Shareaza,[1004]
      SiemensTIA,[1005]
      Signal,"[1006, 1007, 1008, 1009]"
      SignatureCatalog,"[1010, 1011]"
      Skype,"[1012, 1013, 1014, 1015, 1016, 1017, 1018]"
      Slack,"[1019, 1020, 1021, 1022, 1023]"
      Snagit,[1024]
      SnipAndSketch,[1025]
      Sophos,"[58, 59, 60, 61, 1026, 1027]"
      Soulseek,"[1028, 1029]"
      SpeedCommander,[1030]
      Splashtop,"[1031, 1032]"
      StartupFolders,"[1033, 1034]"
      StartupInfo,"[1035, 1036]"
      Steam,"[1037, 1038, 1039, 1040, 1041, 1042, 1043, 1044, 1045, 1046, 1047, 1048]"
      SublimeText,"[1049, 1050]"
      SugarSync,"[1051, 1052, 1053]"
      SumatraPDF,"[1054, 1055]"
      SupremoRemoteDesktop,"[1056, 1057]"
      Symantec_AV_Logs,"[58, 59, 60, 61, 1058, 1059, 1060, 1061, 1062, 1063, 1064, 1065, 1066]"
      Syscache,"[1067, 1068]"
      TablacusExplorer,"[1069, 1070, 1071]"
      TeamViewerLogs,"[1072, 1073, 1074, 1075]"
      Telegram,"[1076, 1077]"
      TeraCopy,[1078]
      ThumbCache,[1079]
      Thunderbird,"[1080, 1081, 1082, 1083, 1084, 1085, 1086, 1087, 1088, 1089, 1090]"
      TorrentClients,"[81, 1315, 1316, 1317, 1318, 1319]"
      Torrents,[1091]
      TotalAV,"[1092, 1093]"
      TotalCommander,"[1094, 1095, 1096, 1097, 1098, 1099, 1100]"
      TreeSize,[1101]
      TrendMicro,"[1102, 1103, 1104]"
      USBDetective,"[36, 37, 38, 39, 279, 280, 281, 490, 491, 492, 493, 494, 495, 496, 497, 683, 684, 685, 714, 715, 716, 717, 718, 719, 720, 721, 722, 723, 724, 725, 726, 727, 728, 729, 730, 731, 732, 733, 734, 735, 736, 737, 738, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 749, 750, 751, 752, 753, 754, 755, 756, 757, 758, 759, 760, 761, 762, 763, 1105, 1106, 1107]"
      USBDevicesLogs,"[1105, 1106, 1107]"
      Ubuntu,"[1108, 1109, 1110, 1111, 1112, 1113, 1114, 1115, 1116, 1117, 1118, 1119, 1120, 1121, 1122, 1123, 1124]"
      Ultraviewer,"[1125, 1126, 1127, 1128]"
      Usenet,[1129]
      UsenetClients,"[563, 564, 573, 574, 856, 857]"
      VIPRE,"[1130, 1131, 1132, 1133]"
      VLC_Media_Player,"[1134, 1135]"
      VMware,"[1136, 1137, 1138, 1139, 1154, 1155, 1156, 1157]"
      VMwareInventory,[1136]
      VMwareMemory,"[1137, 1138, 1139]"
      VNCLogs,"[58, 59, 60, 61, 1140, 1141, 1142]"
      Viber,"[1143, 1144, 1145, 1146, 1147]"
      VirtualBox,"[1148, 1149, 1150, 1151, 1152, 1153, 1154, 1155, 1156, 1157]"
      VirtualBoxConfig,"[1148, 1149]"
      VirtualBoxLogs,"[1150, 1151, 1152]"
      VirtualBoxMemory,[1153]
      VirtualDisks,"[1154, 1155, 1156, 1157]"
      VisualStudioCode,"[1158, 1159, 1160, 1161, 1162, 1163, 1164, 1165]"
      Vivaldi,"[1166, 1167, 1168, 1169, 1170, 1171, 1172, 1173, 1174, 1175, 1176, 1177, 1178, 1179, 1180, 1181, 1182]"
      WBEM,"[1183, 1184]"
      WER,"[1185, 1186, 1187, 1188, 1189]"
      WSL,"[178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195, 458, 459, 460, 461, 462, 463, 464, 465, 466, 467, 468, 469, 470, 471, 472, 473, 474, 475, 977, 978, 979, 980, 981, 982, 983, 984, 985, 986, 987, 988, 989, 990, 1108, 1109, 1110, 1111, 1112, 1113, 1114, 1115, 1116, 1117, 1118, 1119, 1120, 1121, 1122, 1123, 1124, 1298, 1299, 1300, 1301, 1302, 1303, 1304, 1305, 1306, 1307, 1308, 1309, 1310, 1311]"
      WebBrowsers,"[89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148, 149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 625, 626, 647, 648, 649, 650, 651, 652, 653, 1166, 1167, 1168, 1169, 1170, 1171, 1172, 1173, 1174, 1175, 1176, 1177, 1178, 1179, 1180, 1181, 1182, 1264, 1265, 1266, 1267, 1268, 1269, 1270, 1271, 1272, 1273, 1274, 1275, 1276, 1277, 1278]"
      WebServers,"[50, 398, 399, 400, 401, 402, 403, 513, 514, 562]"
      Webroot,[1190]
      WhatsApp,"[1191, 1192, 1193, 1194]"
      WhatsApp_Media,"[1195, 1196]"
      WinDefendDetectionHist,[1197]
      WinSCP,[1198]
      WindowsDefender,"[1199, 1200, 1201, 1202, 1203, 1204, 1205, 1206]"
      WindowsFirewall,"[1207, 1208]"
      WindowsHello,"[1209, 1210, 1211, 1212, 1213, 1214, 1215, 1216, 1217, 1218, 1219, 1220, 1221, 1222, 1223, 1224, 1225, 1226, 1227, 1228, 1229, 1230, 1231]"
      WindowsIndexSearch,"[1232, 1233]"
      WindowsNetwork,[1234]
      WindowsNotificationsDB,"[1235, 1236]"
      WindowsOSUpgradeArtifacts,"[1237, 1238, 1239, 1240, 1241]"
      WindowsPowerDiagnostics,[1242]
      WindowsServerDNSAndDHCP,"[1243, 1244, 1245]"
      WindowsSubsystemforAndroid,"[1246, 1247, 1248, 1249, 1250]"
      WindowsTelemetryDiagnosticsLegacy,"[1251, 1252]"
      WindowsTimeline,[1253]
      WindowsUpdate,"[1254, 1255, 1256]"
      WindowsYourPhone,[1257]
      XPRestorePoints,[1258]
      XYplorer,"[1259, 1260, 1261, 1262]"
      Xeox,[1263]
      Yandex,"[1264, 1265, 1266, 1267, 1268, 1269, 1270, 1271, 1272, 1273, 1274, 1275, 1276, 1277, 1278]"
      ZohoAssist,"[1279, 1280, 1281, 1282, 1283, 1284, 1285]"
      Zoom,"[1286, 1287, 1288, 1289]"
      iTunesBackup,"[1290, 1291, 1292]"
      mIRC,"[1293, 1294]"
      mRemoteNG,"[1295, 1296, 1297]"
      openSUSE,"[1298, 1299, 1300, 1301, 1302, 1303, 1304, 1305, 1306, 1307, 1308, 1309, 1310, 1311]"
      pCloudDatabase,"[1312, 1313, 1314]"
      qBittorrent,"[1315, 1316, 1317, 1318]"
      uTorrent,[1319]

  - name: NTFS_CACHE_TIME
    type: int
    description: How often to flush the NTFS cache. (Default is never).
    default: "1000000"

sources:
  - name: All File Metadata
    query: |
      -- Select all the rule Ids to be included depending on the group
      -- selection.
      LET targets &lt;= SELECT * FROM parse_csv(
           filename=KapeTargets, accessor="data")
      WHERE get(member=Group) AND log(message="Selecting " + Group)

      -- Filter only the rules in the rule table that have an Id we
      -- want. Targets with $ in their name probably refer to ntfs
      -- special files and so they are designated as ntfs
      -- accessor. Other targets may need ntfs parsing but not
      -- necessary - they are designated with the lazy_ntfs accessor.
      LET rule_specs &lt;= SELECT Id, Glob
        FROM parse_csv(filename=KapeRules, accessor="data")
        WHERE Id in array(array=targets.RuleIds)
        AND log(message="file: Selecting glob " + Glob)

      -- Call the generic VSS file collector with the globs we want in
      -- a new CSV file.
      LET all_results &lt;= SELECT * FROM Artifact.Generic.Collectors.File(
        Root=Device, Separator="/", Accessor="file", collectionSpec=rule_specs)

      SELECT * FROM all_results WHERE _Source =~ "Metadata"

  - name: Uploads
    query: |
      SELECT * FROM all_results WHERE _Source =~ "Uploads"

reports:
  - type: CLIENT
    template: |
      {{ import "Reporting.Default" "Templates" }}

      &lt;!-- Default report in case the artifact does not have one --&gt;
      ## {{ .Name }}

      {{ $name := .Name }}

      {{ template "hidden_paragraph_start" dict "description" "View Artifact Description" }}

      {{ Markdown .Description }}

      ### References&lt;/h3&gt;

      {{ range .Reference }}
      * [{{ . }}]({{.}})
      {{- end }}

      {{ template "hidden_paragraph_end" }}

      {{ $query := print "SELECT SourceFile, Size, Modified, LastAccessed, Created \
          FROM source(source='All File Metadata')" }}

      &lt;!-- There could be a huge number of rows just to get the count, so we cap at 10000 --&gt;
      {{ $count := Get ( Query (print "LET X = " $query " LIMIT 10000 " \
         " SELECT 1 AS ALL, count() AS Count FROM X Group BY ALL") | Expand ) \
         "0.Count" 0 }}

      &lt;!-- If this is a flow show the parameters. --&gt;
      {{ $flow := Query "LET X = SELECT Request.Parameters.env AS \
         Env FROM flows(client_id=ClientId, flow_id=FlowId)" \
         "SELECT * FROM foreach(row=X[0].Env, query={ \
             SELECT Key, Value FROM scope()})" | Expand }}

      {{ if $flow }}

      ### Selected Targets

      {{- range $flow -}}{{- if eq (Get . "Value") "Y" }}
      * {{ Get . "Key" }}
      {{- end -}}{{- end }}
      {{ end }}

      ## Files collected

      {{ if gt $count 9999 }}
      Collected more than {{ $count }} files.
      {{ else }}
      Collected a total of {{ $count }} files.
      {{ end }}

      {{ Query $query | Table }}


</code></pre>

