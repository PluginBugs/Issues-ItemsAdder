name: Bug Report
description: File a bug report
title: "[Bug]: "
labels: ["bug"]
assignees:
  - LoneDev6
body:
  - type: checkboxes
    id: searched
    attributes:
      label: Terms
      options:
        - label: "I'm using the very latest version of ItemsAdder and its dependencies."
          required: true
        - label: I already searched on this [Github page](https://github.com/PluginBugs/Issues-ItemsAdder/issues) to check if the same issue was already reported.
          required: true
        - label: I already searched on the [plugin wiki](https://itemsadder.devs.beer/) to know if a solution is already known.
          required: true
        - label: I already asked on the **#💬ia-community-help** channel on **Discord** to know if anyone already has a solution for the issue.
          required: true
  - type: input
    id: discord_tag
    attributes:
      label: Discord tag (optional)
      description: How can we get in touch with you if we need more info?
      placeholder: ex. DiscordTag#0001
    validations:
      required: false
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: A clear and concise description of what the bug is.
      placeholder: Tell us what you see!
      placeholder: "Example: I can't interact with custom furniture if I'm in my own claim"
    validations:
      required: true
  - type: textarea
    id: steps
    attributes:
      label: Steps to reproduce the issue
      description: Describe how to reproduce the issue step by step
      placeholder: |
        1. Go to '...'
        2. Click on '....'
        3. Scroll down to '....'
        4. See error
    validations:
      required: true
  - type: textarea
    id: server_version
    attributes:
      label: Server version
      description: "(run `/version` command and paste it here)"
      placeholder: |
        Run `/version` command and paste it here
        
        Example:
        This server is running Paper version git-Paper-788 (MC: 1.16.5) (Implementing API version 1.16.5-R0.1-SNAPSHOT)"
  - type: textarea
    id: plugin_version
    attributes:
      label: ItemsAdder Version
      placeholder: |
        DO NOT WRITE 'LATEST', run command `/version ItemsAdder` and paste it here.
        
        Example:
        ItemsAdder version 2.4.17
    validations:
      required: true
  - type: textarea
    id: protocollib_version
    attributes:
      label: ProtocolLib Version
      placeholder: |
        DO NOT WRITE 'LATEST', run command `/version ProtocolLib` and paste it here.
        
        Example:
        ProtocolLib version 2.4.17
    validations:
      required: true
  - type: textarea
    id: lonelibs_version
    attributes:
      label: LoneLibs Version
      placeholder: |
        DO NOT WRITE 'LATEST', run command `/version LoneLibs` and paste it here.
        
        Example:
        LoneLibs version 2.4.17
    validations:
      required: true
  - type: textarea
    id: lightapi_version
    attributes:
      label: LightAPI Version (optional)
      placeholder: |
        DO NOT WRITE 'LATEST', run command `/version LightAPI` and paste it here.
        
        Example:
        LightAPI version 2.4.17
  - type: textarea
    id: libsdisguises_version
    attributes:
      label: LibsDisguises Version (optional)
      placeholder: |
        DO NOT WRITE 'LATEST', run command `/version LibsDisguises` and paste it here.
        
        Example:
        LibsDisguises version 2.4.17
  - type: textarea
    id: full_server_log
    attributes:
      label: FULL server log
      placeholder: "You can drag and drop your full server log here"      
  - type: textarea
    id: logs
    attributes:
      label: Error (optional)
      description: Please copy and paste any error you got (this will be automatically formatted into code).
      render: shell
      placeholder: |
        [19:26:04] [Craft Scheduler Thread - 18 - ItemsAdder/WARN]: [ItemsAdder] Plugin ItemsAdder v2.4.16 generated an exception while executing task 22801
          java.lang.ExceptionInInitializerError: null
            at dev.lone.itemsadder.l.j.a(SourceFile:166) ~[ItemsAdder.jar:?]
            at dev.lone.itemsadder.l.j.av(SourceFile:104) ~[ItemsAdder.jar:?]
            at dev.lone.itemsadder.l.a.a(SourceFile:164) ~[ItemsAdder.jar:?]
            at org.bukkit.craftbukkit.v1_17_R1.scheduler.CraftTask.run(CraftTask.java:101) ~[patched_1.17.1.jar:git-Airplane-84]
            at org.bukkit.craftbukkit.v1_17_R1.scheduler.CraftAsyncTask.run(CraftAsyncTask.java:57) [patched_1.17.1.jar:git-Airplane-84]
            at com.destroystokyo.paper.ServerSchedulerReportingWrapper.run(ServerSchedulerReportingWrapper.java:22) [patched_1.17.1.jar:git-Airplane-84]
            at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1130) [?:?]
            at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:630) [?:?]
            at java.lang.Thread.run(Thread.java:831) [?:?]
          Caused by: java.lang.reflect.InaccessibleObjectException: Unable to make field long java.util.zip.ZipEntry.size accessible: module java.base does not "opens java.util.zip" to unnamed module @6f6969ca
            at java.lang.reflect.AccessibleObject.checkCanSetAccessible(AccessibleObject.java:357) ~[?:?]
            at java.lang.reflect.AccessibleObject.checkCanSetAccessible(AccessibleObject.java:297) ~[?:?]
            at java.lang.reflect.Field.checkCanSetAccessible(Field.java:177) ~[?:?]
            at java.lang.reflect.Field.setAccessible(Field.java:171) ~[?:?]
            at com.comphenix.protocol.reflect.FieldUtils.getField(FieldUtils.java:111) ~[PROTOCOLLIB.jar:?]
            at dev.lone.itemsadder.l.k.<clinit>(SourceFile:12) ~[ItemsAdder.jar:?]
            ... 9 more
  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots/Videos
      description: If applicable, add screenshots to help explain your problem.
      value: "(you can drag and drop files or paste links)"
  - type: markdown
    attributes:
      value: |
        ## Thanks for taking the time to fill out this bug report!
