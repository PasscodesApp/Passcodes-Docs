# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
We don't strictly follow them. but the exceptions are very less, very intuitive, but..obvious
and well documented in our release workflow docs.

!!! tip

    Do checkout the [release notes](release-notes.md) for casual changelog. it is more user friendly to read..
    and documents important changes to project in a way's that make sense from a users view.

    This here is for technical users and more developer oriented changelog.

---

## Link

- **Telegram:** [Community (@passcodescommunity)](https://t.me/passcodescommunity)
- **Website:** [https://passcodesapp.github.io/Passcodes-Website/](https://passcodesapp.github.io/Passcodes-Website/)

---

## v1.2.1 - Alpha (Jan 31, 2026)

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 4
Version Name = "v1.2.1-Alpha"
Master Database Version = "v1"
```

</details>

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v1.2.1){:target="\_blank"}  
[Release Notes](release-notes/#v121-alpha-jan-31-2026)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/compare/v1.2.0...v1.2.1)

## v1.2.0 - Alpha (Jan 31, 2026) [YANKED RELEASE]

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 3
Version Name = "v1.1.2-Alpha"
Master Database Version = "v1"
```

</details>

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v1.2.0){:target="\_blank"}  
[Release Notes](release-notes/#v120-alpha-jan-31-2026-yanked-release)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/compare/v1.1.2...v1.2.0)

## v1.1.2 - Alpha (Dec 15, 2025)

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 3
Version Name = "v1.1.2-Alpha"
Master Database Version = "v1"
```

</details>

!!! danger "Breaking Changes"

    This is a kind of a breaking release, it will wipe off all your in-app settings..
    which mean after updating the app, all your previous setting will be reset to defualt.

    This **doesn't** mean that your password data will be lost.. I repeat **your password data will be there as it is, untouched in app**.

    ??? question "You may ask why this is not `v2.0.0`?  even if it has breaking changes???"
        Firstly, the user interaction with app is not change that much in this release that it make sense to make it a major release (`v2.0.0`).

        Secondly & more importantly, It is `v1.1.1` because, setting's data is not than important, core & criticual to app itself.

### Breaking Changes

- **Migrate to DataStore**: changed the way how setting and feature flag were been storage.
  previously, we were using shared preferences. but,
  now we use datastore which is much more modern way of storing such type of data... but this will also mean
  that all your previously store setting will be longer be available anymore. we have decide this breaking changes,
  because app settings can be restored again (in like few minutes). [[@JeelDobariya38]](https://github.com/JeelDobariya38)

### Added

#### Preview Features

- **Autofill System (Preview Feature)**: added an autofill service to autofill user's credentials on
  the fly. [[@hexCode63]](https://github.com/hexCode63)

- **Jetpack Compose (Preview Feature)**: added jetpack compose UI & even added a toggle to switch to
  this new UI. but it would be worthless to do so, because it just has a single screen.. _this feature is mainly
  for very earlier testing_. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

### Changed

- **MVI Flavored - Clean Architecture**: migrated the codebase to make it more scalable,
  extendable & readable. this will enable us to create better features faster & make a strong base for faster
  iteration & collaboration. and will help us delegate & modularized task in future. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

- **Java 21**: code now compile to java 21. previously it was compiling to java 11.
  this should improve performance & efficiency a bit. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

- **Improved Performance & Responsiveness**: Improve performance & better responsiveness of UI (less of density
  pixel, more of scalable pixel measurements). [[@JeelDobariya38]](https://github.com/JeelDobariya38)

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v1.1.2){:target="\_blank"}  
[Release Notes](release-notes/#v112-alpha-dec-15-2025)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/compare/v1.1.1...v1.1.2)

---

## v1.1.1 - Alpha (Sept 11, 2025)

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 2
Version Name = "v1.1.1-Alpha"
Master Database Version = "v1"
```

</details>

### Fixed

- **Fixed Import Passwords**: fixed the bug that was not allowing user to select csv files
  from file picker. due to incorrect mimetype in code.. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v1.1.1){:target="\_blank"}  
[Release Notes](release-notes/#v111-alpha-sept-11-2025)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/compare/v1.1.0...v1.1.1)

---

## v1.1.0 - Alpha (Sept 1, 2025)

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 2
Version Name = "v1.1.0-Alpha"
Master Database Version = "v1"
```

</details>

### Added

- **Improved UI/UX**: improved view password screen's visual feel, also adjust the button colors a
  bit. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

- **Added Feature Flagging**: given user a control on whether they wanna latest experience or stable
  experience. added a way for launching preview features without worry about their
  stability. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

- **Update Checking**: made a basic update checker that help users to stay up to date with latest
  release & also notify user about already reported security vulnerability using pre-release
  mechanism. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

#### Preview Features

- **Copy Button (preview feature)**: added a copy button for copying passwords for easy of use. but
  as it
  is potential threat to security, so made it as a preview feature. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

- **G-Passwords Import/Export (preview feature)**: added a import/export feature. which is also
  compatible with google passwords. I have test it with my google password setup. but, I am not sure
  weather this will run in every edge case or not. So, it is a preview feature for
  now. [[@JeelDobariya38]](https://github.com/JeelDobariya38)

### Notes

- **Official Github Organization (Aug 31, 2025)**: migrate project & repository from
  `JeelDobariya38 (personal account)`
  to `PasscodesApp (my organization)` for better development and governance of the project.

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v1.1.0){:target="\_blank"}  
[Release Notes](release-notes/#v110-alpha-sept-1-2025)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/compare/v1.0.0...v1.1.0)

---

## v1.0.0 - Stable (Aug 16, 2025)

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 1
Version Name = "v1.0.0-Stable"
Master Database Version = "v1"
```

</details>

### Added

- **Localized App**: added language translation for English, Chinese, Hindi, Indonesian, Japanese,
  Korean,
  German, Spanish, Vietnamese. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

- **Improved UI/UX**: added confirmation dialogs for destructive actions, improved support for
  light & dark
  theme with additional minor changes. [[@JeelDobariya38](https://github.com/JeelDobariya38) & [@kudanilll](https://github.com/kudanilll)].

- **New Icon**: rebanded the app as passcodes with a new visual app icon. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

### Changed

- **Migrated Package Name**: migrate package name from `com.passwordmanager` to
  `com.jeeldobariya.passcodes`. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

- **Improve Safety By Kotlin Implementation**: move away from `Java` to `Kotlin`
  Language. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

- **Improve Data Storing Process**: move away from `SqliteDatabase` to `Room` Library for better
  datastorage & security. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v1.0.0){:target="\_blank"}  
[Release Notes](release-notes/#v100-stable-aug-16-2025)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/compare/v0.1.0...v1.0.0)

---

## v0.1.0 - Alpha (Aug 26, 2024) [YANKED RELEASE]

<details>
  <summary>View Internal Details</summary>

```
Pacakage Name = "com.passwordmanager"
Min Android = 8.0 (API level 26)
Max Android = 13 (API level 33)
Version Code = 1
Version Name = "0.1.0-Alpha"
Master Database Version = "v1"
```

</details>

!!! danger

    This is an [yanked release](installing/#explicitly-yanked-release-pure-trash) and should not be used by any user.
    The soley purpose of this release is, just for documenation & serves as a part of project's story...

    The main cause we have yanked this release is.. not that the release itself is bad by any manner.. this release was very early & premature..
    As in, a prototype release. It is stable in it own pace.. and you can use it if, you wish to do so.. but treat this version more as premature. & just for learning..
    If you have any error or bug using this version.. you can report to github issues. we will try our best to assist. but this issue won't have prority.. but it will be fun to discuss how an prototype release stand in production enviroment..

    Also the project's name back then use to be "password manager". which is kind of dumb & lame name, and to be honest little to old also, but it is the name we have started our journey with. we have after a year (2024), maded a decision and envisioned project differently with a name "passcodes".. which is a also an old name, one of mine eariler project, which I have removed from github... but it was the reason I meet [Daniel](https://github.com/kudanilll) in the first place.. and we have started this new project as `password manager` and that eventally became `passcodes`... and now it's in production and in real user's hands... as you read this... 😂😂😂😂😂

    The was a eariler release from a parent project of `passcodes`. Read more over at github [#12](https://github.com/PasscodesApp/Passcodes/discussions/12) & [#14](https://github.com/PasscodesApp/Passcodes/issues/14)

### Added

- **App Icon Creation**: designed and implemented the initial app icon, providing the application
  with a recognizable visual identity. [[@HamadaNative]](https://github.com/HamadaNative).

- **Basic App Structure**: established the foundational architecture of the app, including the main
  entry point and the initial setup. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

- **Main Page Development**: developed the main page of the app, including basic UI components and
  initial layout. [[@JeelDobariya38]](https://github.com/JeelDobariya38).

- **Basic Password Store**: developed a database to store the passwords data. [[@kudanilll]](https://github.com/kudanilll).

- **Basic Design System**: developed a basic material 2 design system for consistency in app's
  feel & look. [[@HamadaNative]](https://github.com/HamadaNative).

### Notes

- This was the initial alpha (pre-release), focusing more on setting up the app for a basic structure and
  visual elements. It is an prototype release (`Proof Of Concept`).

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v0.1.0){:target="\_blank"}  
[Release Notes](release-notes/#v010-alpha-aug-26-2024-yanked-release)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/commits/v0.1.0)
