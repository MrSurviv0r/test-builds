# VR HUB Update Tests

Temporary updater tests for MRSURVIV0R'S VR HUB. **Not production releases.**

Test copies check this repository only. Normal HUB builds will not automatically receive these updates. Public repositories remain publicly downloadable.

## Test 0.9.96 to 0.9.97

1. Put both test scripts and build commands in your normal HUB build folder, alongside Assets, Payload and the other build resources.
2. Run `Build-TEST-0.9.96.cmd` and `Build-TEST-0.9.97.cmd`. Outputs go to separate `dist-test-0.9.96` and `dist-test-0.9.97` folders.
3. ZIP the **0.9.97** EXE, retaining its filename `MRSURVIV0RS-VR-HUB.exe`. Name the ZIP exactly **MRSURVIV0RS-VR-HUB-0.9.97.zip**.
4. Publish a regular release here with tag **0.9.97**, that ZIP attached, and the sample release notes below. Do not mark it prerelease or leave it as a draft. Allow GitHub to finish processing the upload.
5. Run the **0.9.96 test EXE** locally. Confirm the popup shows current 0.9.96, new 0.9.97 and the notes.
6. Choose **Update Later**. Confirm the button remains **HUB Update Available**.
7. Click that button, choose **Update Now**, and confirm the update downloads, installs and relaunches as **0.9.97**.
8. Reopen the updated test HUB. It should not offer the same update again.

Only upload the 0.9.97 ZIP. Do not add TEST or PF20 to the ZIP name.

## Sample GitHub release notes

```markdown
## What's New in 0.9.97 — UPDATER TEST ONLY

- Temporary build to test GitHub update detection.
- Verify current/new versions and release notes inside the HUB.
- Verify Update Later preserves the update button.
- Verify Update Now installs and launches the new build.
- No production game changes. Not a production release.
```

## Isolation

Both test copies display UPDATE TEST in their title and use a separate `%LOCALAPPDATA%\MRSURVIV0R'S VR HUB - UPDATE TEST` folder and test-named desktop/Start Menu shortcuts. Production preferences are not copied, so first-run settings may appear. Updated test shortcuts can point into the test Versions folder.

The updater otherwise uses production PF20 behavior. Game lanes remain present; use these builds to test updates rather than modify game installations.

Keep the production repository and website JSON unchanged. Production PF20 stays at 0.9.96 and is a separate file.
