# Release Workflow

In this file, you will find documented process about, how we release, new version of the app.

!!! Note

    This is not a practice that, we follow from top to bottom.  But it is rather, what our pre-release process look like.. most of the times..

1.  We first draft a new release on github... with a tag, name & generate release notes in its description...

2.  We follow, so called `Main (branch) as Production Environment` practice. So, during the time of release, we test/review the code in main branch.

    > (TBH, this step of testing and review is often skip... cuz, I am really exicted for the release and just rush though the pre-release process... But I will try to improve it....)

3.  Once the review process ends, I updated the code where-ever need. (code that refer to previous version names in application codebase. mostly, in build.gradle.kts files).

4.  Make Documentation up-to-date. (document the main change in app, from user point of view, mostly this is done along with development.. it a kind of docs review).

5.  Update `changelog.md` & `release-notes.md` in Docs Repository.

    !!! Tip

         Now, Befre 6th step.. Rebuild the app again from main branch.. to take in account for outdated/stale assets.

6.  Upload all the apk files in github release (signed apks).

    !!! Info

         Always take backup of release assets.. and (essentail) outputs.. frezzed in time... Senior developers at Passcodes ([@JeelDobariya38](github.com/JeelDobariya38) & [@kudanilll](https://github.com/kudanilll)).. knows what we mean by the word "backup", what to back up and where to back up.....

7.  Now discuss on community, check & test release app on various parameters:-
    - We run unit tests.
    - We run android tests.
    - And of-course, we internally as developers, also test it (manually).

    > (TBH, i don't do this step anytime, always forget it.. this is just written in documentaion.. but this is not really a step for me in reality... cuz, I am to in hurry to release a new version)

8.  Then finally, click the publish button on github to release & launch a new version of app.

9.  Tell in telegram community & social media (linkedin mostly).

10. Celebrate the Release. Plan the future...
