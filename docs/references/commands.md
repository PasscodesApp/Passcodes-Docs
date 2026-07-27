---
title: "Important Commands"
description: "A reference commands for passcodes."
tags:
    - References
    - Developers
---

# Important Commands

## Git & Github

- To a signed commit

```bash
gti commit -s -m "[feat/fix/docs/chore]: ..."
```

- To Push Your Current Branch To Repo To Merge Into Main

```bash
CURRENT_BRANCH=$(git branch --show-current) && \
git pull && \
git switch main && \
git pull && \
git switch "$CURRENT_BRANCH" && \
git rebase main && \
git push
```

## Android & Gradle Commands

- For `.AAB` To Universal `.APK`

```bash
java -jar bundletool.jar build-apks \
  --bundle=app.aab \
  --output=universal.apks \
  --mode=universal \
  --ks=keystore.jks \
  --ks-pass=pass:YOUR_KEYSTORE_PASSWORD \
  --ks-key-alias=YOUR_KEY_ALIAS \
  --key-pass=pass:YOUR_KEY_PASSWORD
```

- For `.AAB` To `.APK`

```bash
java -jar bundletool.jar build-apks \
  --bundle=app.aab \
  --output=universal.apks \
  --ks=keystore.jks \
  --ks-pass=pass:YOUR_KEYSTORE_PASSWORD \
  --ks-key-alias=YOUR_KEY_ALIAS \
  --key-pass=pass:YOUR_KEY_PASSWORD
```

- For Building A Clean ALL Variant

```bash
./gradlew clean build
```

- For Clearing Build Files

```bash
./gradlew clean
```

- For sync depeendency

```bash
./gradlew --refresh-dependencies
```

## Docs Repository Commands

- For run development server

```bash
uv run zensical serve -o
```

- For updating uv packages.

```bash
uv sync --upgrade
```
