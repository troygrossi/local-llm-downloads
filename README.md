# LOCAL_LLM — downloads

Installers for **LOCAL_LLM**, a local-first AI copilot. The source repository is
private; this one exists only so the download link works without a login.

**[Get the latest release →](https://github.com/troygrossi/local-llm-downloads/releases/latest)**

## What is here

| | |
|---|---|
| `vX.Y.Z` releases | the app: Windows installer and zip, macOS and Linux builds, and a `SHA256SUMS*.txt` per platform |
| `<name>-vX.Y.Z` releases | add-ons (`see`, `edit`, `image`, `search`) and portable dependencies (`searxng`, `playwright`), fetched by the app when you install a tool and checked against the sha256 it pins |
| `latest.json` | the update feed, fetched by Settings → Check for updates |

Nothing else. No source, no issue tracker.

## Verify what you downloaded

The Windows installer is **code-signed** (Azure Artifact Signing). Right-click
the file → Properties → Digital Signatures shows who signed it. SmartScreen may
still warn while the certificate builds a reputation. The macOS and Linux builds
are **not signed**; for those, the checksum published beside them is the only
thing that vouches for the file.

Either way, check the checksum before you run it:

```powershell
Get-FileHash .\LOCAL_LLM-setup.exe -Algorithm SHA256
```

```sh
shasum -a 256 LOCAL_LLM.dmg        # macOS
sha256sum LOCAL_LLM.AppImage       # Linux
```

Compare the result against the matching `SHA256SUMS*.txt` on the release page.
If they differ, do not run the file.

## Requirements

Windows 10 or 11, 64-bit. macOS (Apple Silicon or Intel) and Linux (AppImage or
.deb) builds are early: expected to work, not yet tested on a clean machine.

8 GB memory, 10 GB disk, more for large models and image generation. No
graphics card is required — the card decides how large a model you get, not
whether it runs.

First run downloads a few GB: the engine, and one model chosen for your machine.
