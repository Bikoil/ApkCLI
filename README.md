<h1 align="center">
APK CLI
</h1>
<div align="center">
<em> A Git based package manager made for Android using APKs </em>
</div>

***

> [!CAUTION]
> THIS PROJECT IS A WORK IN PROGRESS AND IS BEING MADE BY NON FULLY SKILLED PEOPLE, IT STILL HAS A LONG WAY TO GO, WE ARE ENTHUTHIASTIC ABOUT THIS PROJECT AND HOPE IN MAKING IT WORK SOON.
> We have still not added anything to this project. We are in the process of planning it and intend to start it soon.

- if you'd like to see how ApkCLI will install packages, please look at [this MindMeister diagram](https://mm.tt/app/map/3347354119?t=v5Vi6lyLvk) or the [RTF file](https://github.com/Bikoil/ApkCLI/blob/main/HowAPKCLIWillWork.rtf) of the diagram

# How it works
```


          User requests package by 'apk install <package>'
                                |
                                |
                                |
                                v
          Package is fetched from a Github repo --> • This will be done by either 'curl' or 'wget'
                                |
                                |
                                |
                                v
          Package is installed as a compressed xz file --> • The xz files of packages will be stored in '/sdcard/.apkclitmp/xztmp/'
       -------------------------|-------------------------
      |                         |                         |
      |                         |                         |
      v                         v                         v
APK is stored in        Package is decompressed   Original xz file is deleted
'/sdcard/.apkcli/APK/'          |
                                |
                                |
                                v
      APK is installed via 'pm install /sdcard/.apkcli/APK/<file>.apk'
                                
```

# Info
- The package manager will contain not only APK packages, but also other tools to be installed normally on other package managers, tools such as `git` or maybe `node`
