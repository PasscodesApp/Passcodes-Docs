# Important Commands

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
uv run zensical serve
```

- For updating zensical pacakge.

```bash
uv add --upgrade zensical
```
