# Release Notes

Here, You will find short, sweet and casual `tldrs` for release notes or change-log.
For more details and more professional tone, see [changelog.md](changelog.md).

!!! tip

    Do checkout the [changelog](changelog.md) for more formal release notes. it is more technical to read..

---

## Link

- **Telegram:** [Community (@passcodescommunity)](https://t.me/passcodescommunity)
- **Website:** [https://passcodesapp.github.io/Passcodes-Website/](https://passcodesapp.github.io/Passcodes-Website/)

---

## v1.1.2-Alpha (Dec 15, 2025)

```
Pacakage Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 3
Version Name = "v1.1.2-Alpha"
Master Database Version = "v1"
```

!!! danger
    
    This is a kind of a breaking release, it will wipe off all your in-app settings.. 
    which mean after updating the app, all your previous setting will be reset to defualt.
    
    This doesn't mean that your password data will be lost.. I repeat **your password data will be there as it is, untouched in app**.

    You may ask why this is not `v2.0.0` and `v1.1.1` if it has breaking changes???  
    Firstly, the user interaction with app is not change that much in this release that it make sense to name it `v2.0.0`.
    Secondly more importantly, It is `v1.1.1` because, setting's data is not than important & core to app itself.

**`TL;DR`: Improve the internal code quality.. | Clean architecture in codebase...**

- For user side of app.. things might look same.. or even some part of ui, like conformation dialog may seems to disapper completely.
- App has changed completely internally in codebase. The architecture of the app has shifted from something along the lines of MVC.. 
  to MVI Flavoured Clean architure. Which is more like google's/industry's way of making app in android world...
- This architecture change in app will give us as developers a better place (codebase) to work in. This also make a solid base for further features.
- This release is more like a **shift in direction of passcodes development tragitery, towards becaming a industry/production ready app** rather than just became an another password manager app..
- This release is also a part of biggest refactoring of codebase we are doing at passcodes....
- And thus, a part of it contains premature features like **Autofill & Jetpack Compose UI**. Which are served as a preview features in app, but you can also turn them on if you wish...
- This release also bring with it some performance boost. (theorically, Because I have not notice it yet). As the app now run on `JAVA 21`. it was previously `Java 11`.

---

## v1.1.1-Alpha (Sept 11, 2025)

```
Package Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 2
Version Name = "v1.1.1-Alpha"
Master Database Version = "v1"
```

**`TL;DR`: Sorry for delay, but we have fix import files feature...**

- We are very sorry for the delay.. we have officially fixed the import passwords csv file selection bug...
- In big project, such small mistakes/things happens.. so, ignore it please...

---

## v1.1.0-Alpha (Sept 1, 2025)

```
Package Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 2
Version Name = "v1.1.0-Alpha"
Master Database Version = "v1"
```


**`TL;DR`: Design Improvement.. | Will work with google passwords.... | We are officially an organization on GitHub from `Aug 31, 2025`....**

- This is our first **official release after migrating to the github organization...**
- This release has feature like importing & exporting passwords from google password's app...
- This is an alpha release. Also both the features (copying passwords & importing-exporting password) are disable by default. due to security threats... But, they can be turn on if you wish...
- From this point onwards, app has a mechanism to release feature progressively using feature flags. This means one could opt-into newer unstable features & get earlier access to latest features.
- Also as the passcodes have change from "just my personal hobby project" to an official github based organization.. This release mark as a step forward for us towards open source and towards [open to contribute](./../other-docs/open-contributing-timeline.md)... and potentailly leading us a community as a whole.....
- And more importantly it reflect, my long term vision with passcodes as a project... what it means?...
- Upcoming things will be more fascinating to watch and to be part of... So stick with us.. [Telegram](https://t.me/passcodescommunity)
- And also the app will have more long term support... (if you ignore, the fact that I am not a verified developer, as of "1/9/25 by google"... but will do it in a near time...)

!!! info
    Organization is named **PasscodesApp and not Passcodes. Because, it is not available on github.......**
    
    Stick to watch and observe passcodes upcoming progress... [Telegram](https://t.me/passcodescommunity)

---

## v1.0.0-Stable (Aug 16, 2025)

```
Package Name = "com.jeeldobariya.passcodes"
Min Android = 8.0 (API level 26)
Max Android = 14 (API level 34)
Version Code = 1
Version Name = "v1.0.0-Stable"
Master Database Version = "v1"
```


**`TL;DR`: Our first stable release.. | Not much has change in terms of look and features.. | Name of project has changed to `Passcodes`..**

- This is our first stable release, even though it looks and behaves same as prototype release.
- It's now more stable and more reliable as the data storage system is now tested, optimized and uses more modern approach (room library).
- Things have change internally also... like app was first builded using java language.. but, now it is in kotlin language. which is more align to google's way of building app.
- Now, you also have in-app ablity to switch languages & themes.. (Don;t rely on transalation as they are ai generated for now).
- App now has an improved UI/UX, It has hint's.. especially, as you all where asking like, "what is domain?" "what can i write in domain?" and so on.....

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v0.1.0)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/commits/v0.1.0)


---

## v0.1.0-Alpha (Aug 26, 2024) [YANKED RELEASE]

!!! danger
    
    This is an [yanked release](installing/#explicitly-yanked-release-pure-trash) and should not be used by any user.
    The soley purpose of this release is, just for documenation & serves as a part of project's story...

    The main cause we have yanked this release is.. not that the release itself is bad by any manner.. but the app name it uses is "password manager".
    which is an old name, the name we have started our journey with. we have after a year (2024), maded a decision and envisioned project differently, with a name "passcodes".. which is a also an old name. one of mine eariler project, which I have removed from github... but it was the reason I meet [Daniel](https://github.com/kudanilll) in the first place.. and we have started this new project as `password manager` and that eventally became `passcodes`... and now it's in production and in real user's hands... as you read this... 😂😂😂😂😂

    We have yanked this release to show this shift... you can even see in details below that package name has change..
    So theoretically and practically also, It is an another app/project... an deperacted one in software term's...

    Read more over at github [#12](https://github.com/PasscodesApp/Passcodes/discussions/12){:target="_blank"} & [#14](https://github.com/PasscodesApp/Passcodes/issues/14){:target="_blank"}

```
Package Name = "com.passwordmanager"
Min Android = 8.0 (API level 26)
Max Android = 13 (API level 33)
Version Code = 1
Version Name = "0.1.0-Alpha"
Master Database Version = "v1"
```

**`TL;DR`: Our first initial release.. | Prototype release..**

- It a prototype release which mean it can have bugs...
- It has all the core features, like creating, reading, updating and deleting passwords...
- It has a basic UI that allow you to do things, really intuitively and more structurely...
- But structure and intuitiveness doesn't necessary means a modern user interface—which is little to less cool, but UI reflect a structure in it...

[Checkout Release](https://github.com/PasscodesApp/Passcodes/releases/tag/v0.1.0){:target="_blank"}  
[Changelog](changelog/#v010-alpha-aug-26-2024-yanked-release)  
[Full Changelog](https://github.com/PasscodesApp/Passcodes/commits/v0.1.0)  
