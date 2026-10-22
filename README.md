# RevitXcelerate Updates

Public update metadata and verified installer downloads for RevitXcelerate.
Application source code is maintained separately in a private repository.

## Current availability

No installer has been published yet. An empty `updates.json` is intentional:
the add-in reports that no releases are published instead of offering an untested build.

## Installing updates

RevitXcelerate checks this feed in the background when internet access is available.
Use **RevitXcelerate > Settings > Check for Updates** to check manually.
When a release is available, review its notes and open its GitHub release page to download the installer.
Save your work and close Revit before running the installer. Keep the previous installer for recovery.
Only install releases that explicitly support your Revit year.

## Publisher contract

Upload a verified installer to a GitHub Release here before adding it to `updates.json`.
The feed uses schema version 1 and a `releases` array. Each entry must contain:

- `version`: semantic version, such as `0.1.0` or `0.1.0-beta.1`.
- `revitYears`: explicitly verified years from 2025, 2026 and 2027.
- `releasePage`: HTTPS GitHub release URL in this repository, with a matching version tag.
- `installerUrl`: HTTPS `.exe` asset URL under that release in this repository.
- `sha256`: SHA-256 digest of the exact installer file.
- `notes`: plain-text release notes.

Stable checks exclude semantic prerelease versions. Users may opt into preview releases.
Never place tokens, signing keys, model files, source archives, customer data or unverified installers here.
Update checks do not install software or replace DLLs while Revit is running.
