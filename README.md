## note
This repo is a clone of [xarantolus/fdroid](https://github.com/xarantolus/fdroid), filtered (via git-filter-repo's clean-ignore filter) to remove all app-specific commits. This makes it easier to clone and use yourself without extra history increasing the repo size.

### Wishlist

<details>
<summary>things I'd like to change about how this works</summary>

- Move fdroid commands out of metascoop if possible.
- maybe use official [gh client](https://github.com/cli/cli) instead of metascoop.
    - maybe output release list to a file, then compare incoming releases to decide whether or not to download more releases.
- caching?
- use a different image. medzik/fdroidserver docker image is rebuilt daily(?) with latest fdroid ppa preinstalled, this will cut down on setup time.
- move more commands to the workflow file insteax of using a script
- append credentials to fdroid config file instead of replacing file. this will allow changing non-sensitive details (description, url, etc) without updating secrets
- some way to remove history. unfortunately, we can't use the built-in fdroid settings for this, since it's more than just an fdroid repo (metascoop, etc are included). Maybe `git commit --amend` after removing old versions?

</details>

# fdroid
This repository hosts an [F-Droid](https://f-droid.org/) repo for my apps. This allows you to install and update apps very easily.

### Apps

<!-- This table is auto-generated. Do not edit -->
| Icon | Name | Description | Version |
| --- | --- | --- | --- |
| <a href="https://github.com/Xposed-Modules-Repo/org.hello.coolapk"><img src="fdroid/repo/icons/" alt="FuckCoolapkR icon" width="36px" height="36px"></a> | [**FuckCoolapkR**](https://github.com/Xposed-Modules-Repo/org.hello.coolapk) | FuckCoolapk R | Release-1.16.2 (1162) |
| <a href="https://github.com/tiann/KernelSU"><img src="fdroid/repo/icons/" alt="KernelSu icon" width="36px" height="36px"></a> | [**KernelSu**](https://github.com/tiann/KernelSU) | A Kernel based root solution for Android | v0.6.8 (11238) |
| <a href="https://github.com/gedoor/legado"><img src="fdroid/repo/icons/" alt="Legado 阅读 icon" width="36px" height="36px"></a> | [**Legado 阅读**](https://github.com/gedoor/legado) | Legado 3.0 Book Reader with powerful controls &amp; full functions❤️阅读3.0... | 3.23.073011 (14666) |
| <a href="https://github.com/NihilityT/MiPushFramework"><img src="fdroid/repo/icons/com.xiaomi.xmsf.1003003000.png" alt="MiPushFramework 小米系统级推送框架 icon" width="36px" height="36px"></a> | [**MiPushFramework 小米系统级推送框架**](https://github.com/NihilityT/MiPushFramework) | Let supported push service run system-ly on every Android devices | 0.3.10 (1003003000) |
| <a href="https://github.com/NihilityT/MiPush"><img src="fdroid/repo/icons/" alt="MiPushFramework的分应用模块 icon" width="36px" height="36px"></a> | [**MiPushFramework的分应用模块**](https://github.com/NihilityT/MiPush) | 让 MiPushFramework 支持分应用 | 0.0.26 (188) |
| <a href="https://github.com/MatsuriDayo/NekoBoxForAndroid"><img src="fdroid/repo/icons/" alt="NekoBoxForAndroid icon" width="36px" height="36px"></a> | [**NekoBoxForAndroid**](https://github.com/MatsuriDayo/NekoBoxForAndroid) | NekoBox for Android / sing-box / universal proxy toolchain for Android | 1.2.6 (150) |
| <a href="https://github.com/Notsfsssf/pixez-flutter"><img src="fdroid/repo/icons/" alt="Pixez Flutter icon" width="36px" height="36px"></a> | [**Pixez Flutter**](https://github.com/Notsfsssf/pixez-flutter) | 一个支持免代理直连及查看动图的第三方Pixiv flutter客户端 | 0.9.31 s (10009310) |
| <a href="https://github.com/Jays2Kings/tachiyomiJ2K"><img src="fdroid/repo/icons/" alt="tachiyomiJ2K icon" width="36px" height="36px"></a> | [**tachiyomiJ2K**](https://github.com/Jays2Kings/tachiyomiJ2K) | Free and open source manga reader for Android | 1.7.1 (106) |
| <a href="https://github.com/Tornaco/Thanox"><img src="fdroid/repo/icons/github.tornaco.android.thanos.3071983.png" alt="Thanox icon" width="36px" height="36px"></a> | [**Thanox**](https://github.com/Tornaco/Thanox) | I am thanos! 😈 👌 | 4.2.7.1-prc (3071983) |
| <a href="https://github.com/fankes/TSBattery"><img src="fdroid/repo/icons/" alt="TSBattery icon" width="36px" height="36px"></a> | [**TSBattery**](https://github.com/fankes/TSBattery) | A new way to save your battery avoid cancer apps hacker it. | 4.3 (29) |
| <a href="https://github.com/yujincheng08/BiliRoaming"><img src="fdroid/repo/icons/" alt="哔哩漫游 BiliRoaming icon" width="36px" height="36px"></a> | [**哔哩漫游 BiliRoaming**](https://github.com/yujincheng08/BiliRoaming) | b&#39;\xe5\x93\x94\xe5\x93\xa9\xe6\xbc\xab\xe6\xb8\xb8\xef\xbc\x8c\xe8\xa7\xa3\xe9\x99\xa4B\xe7\xab\x99\xe5\xae\xa2\xe6\x88\xb7\xe7\xab\xaf\xe7\x95\xaa\xe5\x89\xa7\xe5\x8c\xba\xe5\x9f\x9f\xe9\x99\x90\xe5\x88\xb6\xe7\x9a\x84Xposed\xe6\xa8\xa1\xe5\x9d\x97\xef\xbc\x8c\xe5\xb9\xb6\xe4\xb8\x94\xe6...&#39; | 1.6.12 (1208) |
| <a href="https://github.com/nining377/dolby_beta"><img src="fdroid/repo/icons/com.raincat.dolby_beta.354.png" alt="杜比大喇叭β版 DolbyBeta icon" width="36px" height="36px"></a> | [**杜比大喇叭β版 DolbyBeta**](https://github.com/nining377/dolby_beta) | b&#39;\xe6\x9d\x9c\xe6\xaf\x94\xe5\xa4\xa7\xe5\x96\x87\xe5\x8f\xad\xe7\x9a\x84\xce\xb2\xe7\x89\x88\xe8\xbf\x8e\xe6\x9d\xa5\xe4\xba\x86\xe9\x87\x8d\xe5\xa4\xa7\xe7\x9a\x84\xe9\x9d\xa9\xe6\x96\xb0\xef\xbc\x8c\xe5\x90\x88\xe5\xb9\xb6\xe4\xba\x86UnblockMusic Pro\xe7\x9a...&#39; | 3.5.4 (354) |
| <a href="https://github.com/Dr-TSNG/Hide-My-Applist"><img src="fdroid/repo/icons/" alt="隐藏应用列表 Hide-My-Applist icon" width="36px" height="36px"></a> | [**隐藏应用列表 Hide-My-Applist**](https://github.com/Dr-TSNG/Hide-My-Applist) | An Xposed module to intercept applist detections | 3.2 (410) |
<!-- end apps table -->

### How to use
1. At first, you should [install the F-Droid app](https://f-droid.org/), it's an alternative app store for Android.
2. Now you can copy the following [link](https://raw.githubusercontent.com/xrz-cloud/Download2MyFrdoid/main/fdroid/repo?fingerprint=D32D7A89ACC5CFCEE967B110ADB706AD1EA240BBD688E986A8FD726F0FBCDD42), then add this repository to your F-Droid client:

    ```
    https://raw.githubusercontent.com/xrz-cloud/Download2MyFrdoid/main/fdroid/repo?fingerprint=D32D7A89ACC5CFCEE967B110ADB706AD1EA240BBD688E986A8FD726F0FBCDD42
    ```

    Alternatively, you can also scan this QR code:

    <p align="center">
      <img src=".github/qrcode.png?raw=true" alt="F-Droid repo QR code"/>
    </p>

3. Open the link in F-Droid. It will ask you to add the repository. Everything should already be filled in correctly, so just press "OK".
4. You can now install my apps, e.g. start by searching for "Notality" in the F-Droid client.

### Apps

<!-- This table is auto-generated. Do not edit -->
<!-- end apps table -->
Please note that some apps published here might contain [Anti-Features](https://f-droid.org/en/docs/Anti-Features/). If you can't find an app by searching for it, you can go to settings and enable "Include anti-feature apps".

### For developers
If you are a developer and want to publish your own apps right from GitHub Actions as an F-Droid repo, you can fork/copy this repo and see  [the documentation](setup.md) for more information on how to set it up.

### [License](LICENSE)
The license is for the files in this repository, *except* those in the `fdroid` directory. These files *might* be licensed differently; you can use an F-Droid client to get the details for each app.
