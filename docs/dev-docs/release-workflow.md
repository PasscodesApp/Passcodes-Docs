# Release Workflow

In this file, you will find documented process about, how we release, new version of the app.

!!! Note

    This is not a practice that, we follow from top to bottom.  But it is rather, what our pre-release process look like.. most of the times..

1.  We first draft a new release on github... with a tag, name & generated release notes in its description...

    !!! tip

        Name of the release must adher to `vX.X.X - [Alpha|Beta|Stable] [[YANKED RELEASE]]`

        refer:- [how to find a best release](./../user-docs/installing/#how-to-find-a-best-release)

2.  We follow, so called `Main (branch) as Production Environment` practice. So, during the time of release, we test/review the code in main branch.

    > (TBH, this step of testing and review is often skip... cuz, I am really exicted for the release and just rush though the pre-release process... But I will try to improve it....)

3.  Once the review process ends, I updated the code where-ever need. (code that refer to previous version names in application codebase. mostly, in app.json file).

4.  Update Documentation. (document the main change in app, from user point of view, mostly this is done along with development.. it a kind of docs review).

5.  Update `changelog.md` & `release-notes.md` in documentation repository.

    !!! Tip

        Now, Before the next step, rebuild the app again from main branch to take in-account for outdated/stale assets.

6.  Upload all the artifacts files in github release.

    !!! Info

        Always take backup of release artifacts and essential outputs... frezzed in time... senior developers at Passcodes ([@JeelDobariya38](github.com/JeelDobariya38) & [@kudanilll](https://github.com/kudanilll)) knows what we mean by the word "backup", what to backup and where to backup...

7.  Now discuss on community, check & test release app on various parameters:-
    - We run unit tests.
    - And of-course, we internally as developers, also test it (manually).

    > (TBH, I don't do this step anytime, always forget it.. this is just written in documentaion.. but this is not really a step for me in reality. cuz, I in super exicted to release a new version)

8.  Then finally, click the publish button on github to release & launch a new version of app.

9.  Tell in discord community & social media (linkedin mostly).

10. Celebrate the Release...
