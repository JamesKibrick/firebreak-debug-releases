# Firebreak Debug Releases

This is a **private repository** for distributing debug builds of the Firebreak File Transfer application.

## Purpose

Debug builds include:
- Console window for viewing logs and debugging output
- Same features and version numbers as standard releases
- Separate update channel to prevent accidental cross-updates

## Important Notes

- **DO NOT make this repository public** - Debug builds are for internal testing only
- Version numbers always match the standard releases in `firebreak-releases`
- Debug builds check this repository for updates, not the public one
- All releases are tagged with `-debug` suffix (e.g., `v1.9.0-debug`)

## Update Channel

Debug builds compiled with:
```python
BUILD_CHANNEL = "debug"
UPDATE_MANIFEST_URL = "https://raw.githubusercontent.com/JamesKibrick/firebreak-debug-releases/main/latest_version.json"
```

## For Testers

If you're testing debug builds:
1. You'll see a console window with debug output
2. Updates come from this private repository
3. You won't accidentally get standard (non-console) builds

## Releases

Releases are automatically created by the `release.py` script when using the `--with-debug` flag.