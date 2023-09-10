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
| <a href="https://github.com/Jays2Kings/tachiyomiJ2K"><img src="fdroid/repo/icons/" alt="tachiyomiJ2K icon" width="36px" height="36px"></a> | [**tachiyomiJ2K**](https://github.com/Jays2Kings/tachiyomiJ2K) | Free and open source manga reader for Android | 1.6.6 (104) |
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
