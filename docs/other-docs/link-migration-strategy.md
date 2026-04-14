# Link Migration Strategy

In this file you will find the solution to the problem of [link compatablity break](https://github.com/orgs/PasscodesApp/discussions/3) issue.

Now, here is what we think of this issue. `Url Consistency` is not fundementally an issue with passcodes. It's an general issue that occurs everywhere.
With passcodes it occur most often; cuz, my vision for passcodes as a project tend to change a lot.

Now, we will not consider the "link consistency" as a major issue, that we need are responsible to fix. cuz,

- first of all, passcodes is at the end of day an open source project, and we as developers can't solve everything, (in otherwords, we have limited time and sight to detect every broken link)
- the project by [its definition](project-overview.md), expects smart (nerd) users, who can find the require infomation any how. (mostly using docs or by asking on community)
- and third, the most important reason, passcodes is heavly an user's security app. which inheritly means users are expected to update it regurally. (even the security patches)

---

With that being said, here is guide for developers on how to attach link in passcodes app or anywhere in social media.. to make it minimally venurable to a change.
Mostly, passcodes app get problem with github link compatablity. because file system in git repository changes overtime.

Basically we use, what we call a `smart decision` system for linking (url embedding).

 1.  Choose a more reliable link to a resource.

    Most of time when we are adding link to github file. likly speaking, In most cases. we have a choice. instead of add file link from main branch add the link with a version tag.

    ```bash
    https://github.com/PasscodesApp/Passcodes/blob/main/README.md ❌❌❌

    https://github.com/PasscodesApp/Passcodes/blob/v0.1.0/README.md ✔️ ✔️ ✔️ 
    ```


 2. Choose a more general link if possible.

    This, is specfically applicable for resources, where you want dynamic changes intead of static files.

    This only apply to files that you believe are more important and thier links are likely not gonna change.
    and if thier url changes there will be some sort of backward compatablity or a workaround.

    ```bash
    https://github.com/PasscodesApp/Passcodes-Docs/blob/v0.1.0/changelog.md ❌❌❌
    https://github.com/PasscodesApp/Passcodes-Docs/blob/main/user-docs/changelog.md ✔️ ✔️ ✔️ 

    https://github.com/PasscodesApp/Passcodes/blob/main/LICENSE.txt ❌❌❌
    https://github.com/PasscodesApp/Passcodes-Docs/blob/main/LICENSE.txt ✔️ ✔️ ✔️ 

    https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md ❌❌❌
    https://github.com/PasscodesApp/Passcodes-Docs/blob/v1.0.0/database-design-docs/master.db/v1.md ✔️ ✔️ ✔️ 
    ```

 3.  Make link general with relative path.

    This mean always leverage the relative path, when possible it make it.. less venurable to big changes.. and work in varity of enviroments. like if repository name changes it stay compatible.

    But, this must be use smartly to ensure that it works.. otherwise sometimes it fails also.

    ```
    https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md ❌❌❌
    /database-design-docs/master.db/v1.md ✔️ ✔️ ✔️ 
    ```

 4.  **IMPORTANT**: Give context when possible. mostly we use link in context so user can find if link has changed. but try give/optimize more context by link text.
 
    Try to provide context such that it adhere to a more broad & generalized enviroment.

    This is very complicated (debetable) rule only for markdown. if you like and if it necessary follow this rule, like you are attaching a link to some important resource **otherwise just for markdown file, poritrized readablity.**

    ```markdown
    [v1 db schema](https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md) ❌❌❌
    [database-design-docs/master.db/v1.md @ Passcodes-Docs](https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md) ✔️ ✔️ ✔️ 
    ```
