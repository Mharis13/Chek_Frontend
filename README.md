# Chek

## Project Requirements

- [pnpm v12+](https://pnpm.io/installation)

## Run project

- run `pnpm install` to install dependencies.
- run `pnpm run start` to start the app.
- run `pnpm test` to run tests.

## Expo Go

### Requirements

- Expo account (this requirement was added in latest versions of the SDK. More info [here](https://expo.dev/changelog/expo-go-57-login)
- Logged into Expo account (PC) and Expo Go (App). It must use the same account.
- Latest Expo SDK installed in your device.

---

### Run in iOS device

1. Run command `pnpm run start`
2. Ensure that Expo is using the Expo Go, if it's using development build press `s` to switch mode.
3. Scan QR with the camera and open in Expo Go.

### Run in Android device

TBD

## PNPM

### How to solve ERR_PNPM_IGNORED_BUILDS

If pnpm stops with ERR_PNPM_IGNORED_BUILDS, the dependency install reached a package whose lifecycle build script is not approved.
This avoids installing scripts that can harm the project or even you or your computer.

1. Inspect the ignored builds with `pnpm ignored-builds`
2. Verify that the packages tree is not suspicious with `pnpm why <package_name>`
3. Check the packages scripts with `pnpm view <package_name> scripts`
4. If everything looks fine you can approve the builds with `pnpm approve-builds` or explicitly with `pnpm approve-builds <package_name>`

If the package looks suspicious **DO NOT** use it, is better to find an alternative than risking being hacked.
