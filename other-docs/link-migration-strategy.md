# Link Migration Strategy

In this file you will find the solution to the problem of [link compatablity break](https://github.com/orgs/PasscodesApp/discussions/3) issue.

Now, here what we thing on this issue. `Link Compatablity` is not fundementally an issue with passcodes. It general issue that occurs everywhere.
With passcodes it occur most because my vision for passcodes as project change a lot.

Now, we will not consider the link compatablity as major issue, that we need are responsible to fix. because,

- first of all, passcodes is at the end of day an open source project, and we as developers can't solve everything, 
- the project by [its definition](project-overview.md), expects smart (nerd) users how can find the require infomation any how. (mostly useing telegram community)
- and third and most important reason, passcodes is heavly an users security app. which inheritly means users are expected to update it regurally. (even the security patches)

With that said, here is guide for developers how to attach link in passcodes app or anywhere in social media.. to make it minimal venurable to change.
More passcodes app get problem with github link compatablity. because file system in git repository changes overtime.

Basically we use, what we call a `smart decision` system for linking (url embedding).

- Choose a more reliable link to a resource.

Most of time when we add github file like, In most case we have a choice. instead of add file link from main branch add the link with a version tag.

```bash
https://github.com/PasscodesApp/Passcodes/blob/main/README.md ❌❌❌

https://github.com/PasscodesApp/Passcodes/blob/v0.1.0/README.md ✔️ ✔️ ✔️ 
```


- Choose a more general link if possible.

This, is applicable for resources, where you want dynamic changes intead od static files.

This only apply to files that you believe are more important and thier links are likely not gonna change.
and if thier url changes there will be some sort backward compatablity workaround.

```bash
https://github.com/PasscodesApp/Passcodes-Docs/blob/v0.1.0/changelog.md ❌❌❌
https://github.com/PasscodesApp/Passcodes-Docs/blob/main/user-docs/changelog.md ✔️ ✔️ ✔️ 

https://github.com/PasscodesApp/Passcodes/blob/main/LICENSE.txt ❌❌❌
https://github.com/PasscodesApp/Passcodes-Docs/blob/main/LICENSE.txt ✔️ ✔️ ✔️ 

https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md ❌❌❌
https://github.com/PasscodesApp/Passcodes-Docs/blob/v1.0.0/database-design-docs/master.db/v1.md ✔️ ✔️ ✔️ 
```

- Make link general with relative path.

This mean always leverage the relative path, when possible it make less venurable to big changes.. and work in varity of enviroments. like if repository name changes it stay compatible.

But, this must use smartly to ensure that it works.. otherwise sometimes it fails also.

```
https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md ❌❌❌
/database-design-docs/master.db/v1.md ✔️ ✔️ ✔️ 
```

- Give context when possible.

Try to provide context such that it adhere to a more broad & generalized enviroment.

This is very complicated (debetable) rule only for markdown. if you like and if it necessary follow this rule, like you are attaching a link to some important resource
otherwise just for markdown file poritrized readablity.

```markdown
[v1 db schema](https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md) ❌❌❌
[https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md](https://github.com/PasscodesApp/Passcodes-Docs/blob/main/database-design-docs/master.db/v1.md) ✔️ ✔️ ✔️ 
```

