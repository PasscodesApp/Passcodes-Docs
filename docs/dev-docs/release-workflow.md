# Release Workflow

In this file, you will find documented process about, how we release, new version of a app.

> [!IMPORTANT]
> This is not a practice that, we follow from top to bottom.
> But it is rather, what our pre-release process look like.. (most of times)

1. Draft a new release in github. (with a tag, name & generate release notes in description).

2. We follow, so called `Main (branch) as Production Environment` practice. So, during the time of release, we test/review the code in main branch.

   (TBH, this step of testing and review is often skip... cuz, i am really exicted for the release and just tush though pre-release process which i should not do... But I will try to calm myself-down during pre release..)

3. Once the review process ends, I updated the code where-ever need. (code that refer to previous version names in application codebase. mostly, in build.gradle.kts files).

4. Make Documentation up-to-date. (document the main change in app, from user point of view, mostly this is done along with development.. it a kind of docs review).

5. Update `changelog.md` & `release-notes.md` in Docs Repository.

6. Upload all the apk files in github release (signed apks). (rebuild the app again from main branch.. to take in account for outdated/stale assets).

> [!TIP]
> Always take backup of release assets.. and (essentail) outputs.. frezze in time... Senior developers at Passcodes (@JeelDobariya38 & @kudanill).. knows what we mean by word "backup" and what to back up and where to back up.....

7. Discuss on community, check & test release app on various parameters and
   - We run unit tests.
   - We run android tests.
   - And of-course, we internally as developers, also test it (manually).

   (TBH, i don't do this step anytime, always forget it.. this is just written in documentaion.. but not really a step for me in reality...)

8. Then finally, click the publish button to release & launch a new version of app.

9. Tell in telegram community & social media.

10. Celebrate the Release.
