# Detail Guide On Installation

This file give you a deep guide on installation & updation process. we hope that you have already read the step written in the readme. but, aren't satisfied with that and need more info and guide on installation and updation.

👏👏 We appreciate your efforts. As a developers, we try to abstract away complicated processes, But sometimes this abstraction makes things seems simpler that it really is.. Which lead to false image of the process. To avoid that, we have created this guide that help you navigate installation and updation process..

## Table of Contents

- [Installation Process](#installation-process)
- [Updation Process](#updation-process)
- [How To Find A Best Release](#how-to-find-a-best-release)
- [Explicitly Yanked Release (Pure Trash)](#explicitly-yanked-release-pure-trash)

## Installation Process

For initial installation of app, you can follow step given below, they works in most scenario.

1.  Checking whether the app can run on your device or not??

    - go to your setting app and check whether you are on android 8+ or not? (it usually avaiable near "system update" section)
    - if no, then sorry, app is not compatible with your device.
    - and if yes, then mostly you are good to go but, officially we only support device between android 8 to 14. for more or high version of android. app might still be run, but we don;t officially support it.

2.  After completing first step, Pick a version of app to install.

    - go to our [github repository's release page](https://github.com/PasscodesApp/Passcodes/releases). There you will find a list of releases available.
    - pick up any one of the release you like. (we recommend you to pick a good release. [how can you find a good release](#how-to-find-a-best-release)?)
    - after picking a release, you can read it's [release-notes](release-notes.md) to know what has changed. (optional step)

3.  Downloading an APK file

    - after picking a release, you can scroll to bottom of that release towards the assets section and download the apk that better fits your phone's CPU architecture.

    ???+ example

          * arm64 (v8) [Mostly every modern Android smartphone runs on arm64-v8a]
          * armeabi (v7a) [i.e. Samsung Galaxy A01, A02, A10 && Xiaomi Redmi 9A, 9C]
          * x86
          * x86 (64) [it is mostly relevant for Android emulators on desktop environments]

    - if you don;t know your phone's CPU architecture. just download the apk file that has word **`"universal"`** in its name.

4.  Installing an APK file

    - the apk file will most like be downloaded in your browser's download folder. (probably it would be Chrome, Firefox or Edge)
    - tap on the apk file in the browser or find the file in your device's file manager. it will be under downloads folder in your device...
    - now, open the app & enjoy.
    - also, take a moment to setup the app to your best interest. it will be really intuitive to do so.. just open the setting screen in passcodes app..

if any problem occurs while performing the above 4 step. report your problem using [github issues](https://github.com/PasscodesApp/Passcodes/issues/new) after checking the other [available support documentation](https://passcodesapp.github.io/Passcodes-Docs/) .

## Updation Process

As you are reading this part, we hope that you already have installed passcodes app in your phone and now, you want to update it.

you can follow step given below. they work in most scenario.

!!! failure

    updating from one version to another might result into a data lost. though, it occur extremely rarely.

    but, its a good idea/practice to take a backup of your data.

    this data lost are likely to occur, when you are updating from one major version to another major version meaning from ***`1.x.x`*** to ***`2.x.x`***.

1.  Checking whether the update is available or not??

    - find out the current verion of the app you are using.

    ???+ question "How to find the version of currently installed app??"

        you can find your currently installed passcodes app version....

        - ...on the main screen when you open the passcodes app itself.
        - ...under app info in your phone's settings app.

    - check whether a update exist or not? by comparing your current app version with latest app update on [github repository's release page](https://github.com/PasscodesApp/Passcodes/releases).
    - if no, then you can;t update but, you can surely ask about the next update using our [Telegram (@passcodescommunity)](https://t.me/passcodescommunity).

    ??? tip

        if you know a bit of android then just clone the repository and build from main. it will work fine, because we use main branch as production. take reference from existing [building documentation](./../dev-docs/building.md).

        ignore this if it doesn't make sense to you..

    - if yes, then check how big the update is and how it affect your experience as a user? to find out an updates impact. you can find the difference between your current version and the new version you are updating to...
    - i.e, if you are updating from **"1.x.x"** to **"2.x.x"** the the change will be very big. if you update from **"1.x.0"** to **"1.x.2"**. then, the change might not even be visible.

2.  Downloaded the updated apk files.

    - it is same as you did earlier while installing the app.
    - goto [release page](https://github.com/PasscodesApp/Passcodes/releases) and download the asset from select release. refer installation guide above if needed.
    - you can read it's [release-notes](release-notes.md) to know what has changed. (optional step)

3.  Update the app.

    - if, you updating to a new major release, meaning from 1.x.x to 2.x.x then, don;t forget to backup your data. you will thank your self later, if something goes wrong...
    - now install the new apk file by click on it in your downloads folder, it will ask you to upgrade instead of install.
    - now, open the app and enjoy your updated exprience.
    - there might be new stuff so, you might need to change your existing setup or need to setup the new ones. refer to our documentation.
    - you can read it's [release-notes](release-notes.md) to know what has changed. (optional step)

4.  Restore the backup if need.

    - if, needed restore the files/data back.
    - even revert to prevoius release if, problem presists.

    !!! info

        we admire the contribution even in form of your experience with app.

        meaning, you take a moment for reporting your "data loss / data corruption / any other" problem during the updation of app. will be  highly appreciate.
        this helps us make better experiences & fix bugs that might be missed by us.

---

## How To Find A Best Release?

To find a best release you should have knowledge of passcodes versioning system and type of releases we publishes/releases.

### Release Types

On our github release page you will find majorly **`(2 + 3 = 5) type of release`** . Where each type of release label tell you something about release.
Each release on github may have a label but, some even lacks them completely. These label tends to tell you more about release, so they are **IMPORTANT** to consider.

There are majorly two ways, In which we classify a release. mean one release will have two labels at ones.
so to speak:

- **`"Build Label"`**: this label that won't change once after we publish a release. (alpha/beta/stable)
- **`"Github Release Label"`**: this label can and tends to change with time. (pre-release/latest)

#### three type, are embedded in app itself, you can find them on github release title:

(this tags/labels can;t change after initial release of that version is done).

- _Alpha_: special design for development purposes (conatin a lots of latest feature as preview features), they **_`likely comes with a lots of bugs and security venerability`_**. We have likely publish this, without thoroughly test them.
- _Beta_: release that can be used by mass audience, and likely can contain minor bugs.
- _Stable_: are likely to be more stable than alpha & beta release types, contain **`near to zero bugs`** as they are very well tested. this release also will have **`extra developer attention & support`**.

#### two type are specific to github releases. these label's are on github release itself:

(this tags/label can change with time as they are dynamic and are not tied to app itself. meaning they are no hard coded anywhere!!)

- _Pre Release_: this release are not so good to install or to stick with. these are generally like **`marked as deperacted`** releases... As we update our app prominently, we mark previous release as deperacted using this pre release github label... but don't worry much about it, because if you are using a pre release.. the app itself will likely ask you to update or give you some sort of alert...
- _Latest_: this release label, make a release as the best up to date release to install. mean all every release will like be latest utill a ne latest release comes. just like every day is today utill tommorrow get a chance.... but **"`latest doesn't mean stable. it means latest feature.`"**

??? Note

    this label or flag changes with time. meaning, a app version after it release, can be marked as pre-release as there are lots of bug found in that release later or a release can later be marked as latest release as it all good after test in production enviroment.

#### So, here is a list in order where starting type are best and ending types are worse.

???+ Abstract

    Use **[bitwarden](https://bitwarden.com/download/)** really, if care this much about your digital security... because it provide you with the best safety standards,

    why use passcodes????? (for simplicity, i guess, okay no worry, passcodes is better than your forget password? 🤣🤣, but later migrate to bitwarden if possible)

    > Bitwarden

    > STABLE (the best)

    > LATEST

    > BETA

    > ALPHA

    > PRE-RELEASE

    > RELEASE-WITH-NO-FLAGS (the worst)

    > Explictly Yanked Release (Pure Trash)

    > And then comes your forget passwords (Seriously, just DON'T DO THIS!!!!!)

    !!! Example

        It more likely that a single release can have two flag at a same time. for example, a stable and pre-release. In such case, consider the github base label in this case `pre-release`. as they are more dynamic and provide the latest information from us (developer part).

        > this clear means a pre-release even if they are stable / alpha / beta / gamma (unlikely.... 😂)
        > it just doesn't matter it will be considered **`the worst`**...

---

## Explicitly Yanked Release (Pure Trash)

This release will have Yanked Release written in the release title and description on github release page.

Such release are just there for documentation purpose..

**`JUST DON'T USE THEM!!!!`**
