# Release Workflow

In this file, you will find documented process about, how we release, new version of a app.

> [!IMPORTANT]
> This is not a practice that, we follow from top to bottom. 
> But it is rather, what our pre-release process look like.. (most of time)

1. We follow, so called `Main as Production Environment`. So, during the time of release we test the main branch code.

2. Updated the code where ever need. (code that refer to previous version names in application codebase).

3. Make Documentation up-to-date. (document the main change in app, from user point of view, mostly this is done along with development.. it a kind of docs review).

4. Update `changelog.md` & `release-notes.md` in Docs Repository.

5. Draft a new release with all apk files uploaded (signed apks).

6. Discuss on community and check & test release app on various parameters and

    - We run unit tests.
    - We run android tests.
    - And of-course, we internally as developers, also test it (manually).

7. Then, publish a tag in the documentaion version. (Add a tag to docs)

8. Then finally, click the publish release to launch a new version of app.

9. Tell in telegram community & social media.

10. Celebrate the Release.

