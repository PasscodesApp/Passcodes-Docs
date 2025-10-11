# Passcodes-Docs

This repository contains Developers Docs, Support Docs & User Guide For Passcodes App.

> [!NOTE]
> The [docs (at repositiory)](https://github.com/PasscodesApp/Passcodes-Docs/) might have outdated (behind time) or forward (ahead of time) infomation (may be by a week or so).. 
> So, it always good habit to verify stuff.. By see the code... Because we as developer of passcodes focus more on code.. and documenation is our second priority..

## Structrue

We have a specfic structure that we follow, we divide the docs in directory based on concerns and whow the documentaion is ment to be read by.

| CONCERNS         | LINKS                                          | Description                                                |
| ---------------- | ---------------------------------------------- | ---------------------------------------------------------- |
| Users            | [user-docs/](user-docs/)                       | user manuals, how-to-use guides etc...                     |
| App Developers   | [dev-docs/](dev-docs/)                         | developer guides, coding docs, building guides etc...      |
| Database         | [database-design-docs/](database-design-docs/) | database schemas, migrations etc...                        |
| Third Party Devs | [custom-backend-docs/](custom-backend-docs/)   | custom backends guides                                     |
| Main Docs        | [other-docs/](other-docs/)                     | most **important** docs.. yet, they don;t relate to coding |
| Reference        | [references/](references/)                     | all docs that not project specfic. but can help developers |
| Essentials       | [essentials/](essentials/)                     | no docs here.. just github & management stuff..            |


## Documentaion Version System

<!-- Currently, docs is general to all app. and no version system is needed

We have version system for docs, every version of app will have a coressponding docs, that you will find from below table.
We use git(&hub) tags to seperate docs.. And this make up a version system for docs.

| App Version                   | Docs URL                                                       |
| ----------------------------- | -------------------------------------------------------------- |
| latest (development use only) | https://github.com/PasscodesApp/Passcodes-Docs                 |
| vX.X.X                        | https://github.com/PasscodesApp/Passcodes-Docs/blob/vX.X.X     |
| all prior version             | https://github.com/PasscodesApp/Passcodes-Docs/blob/prior-docs |

-->

All the version of the passcodes app, can use the documenation avaliable over here, The docs currenty are applicable all versions of app.. (atleast for now) [prior-docs](https://github.com/PasscodesApp/Passcodes-Docs/blob/prior-docs).
The docs avaliable here, in this repository are [under development](https://github.com/PasscodesApp/Passcodes-Docs/) and you should refer to tag [prior-docs](https://github.com/PasscodesApp/Passcodes-Docs/blob/prior-docs) in this repository.

## Tips & Recommendation

We recommend using / opening, this docs in [obsidian.md](https://obsidian.md) for better experience in navigating as It made in obsidian app..

if you think, you gonna use it a lot. otherwise, in GitHub is just fine as well.

## Best Practices We Follow

- Use lowercase character for docs file / directory name.
- Use hyphens for docs file / directory name.
- Also try to separate and organize docs as much as possible.. like a hierarchy. (don't fear nested structure).
- Avoid renameing a file once created, because there might be URL pointing to it... from app or from various source which once publish can;t change.. (but if you have a strong reason to rename break this rule) Also, refer to [link-migration-strategy.md](other-docs/link-migration-strategy.md).

## Contirbuting to Docs

This works same as contributing to repository.. Create your branch in this repo, make changes and submit a pr.. Always refer to [CONTRIBUTING.md](CONTRIBUTING.md)

## Notes

Here, You will find all the docs releated to the `Passcodes` and other project under `PasscodesApp` github organization..
This is single place that you need refer, for any docs or updates..

