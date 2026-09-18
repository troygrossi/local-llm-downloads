# LOCAL_LLM — downloads

Installers for **LOCAL_LLM**, a local-first AI copilot. The source repository is
private; this one exists only so the download link works without a login.

**[Get the latest release →](https://github.com/troygrossi/local-llm-downloads/releases/latest)**

## What is here

| | |
|---|---|
| Releases | the installer, the zip, and `SHA256SUMS.txt` for each version |
| `latest.json` | the update feed, fetched by Settings → Check for updates |

Nothing else. No source, no issue tracker.

## Verify what you downloaded

The installer is **not code-signed**, so Windows SmartScreen will warn you. That
warning is correct: nothing vouches for the binary except the checksum published
beside it. Check it before you run it.

```powershell
Get-FileHash .\LOCAL_LLM_0.2.2_x64-setup.exe -Algorithm SHA256
```

Compare the result against `SHA256SUMS.txt` on the release page. If they differ,
do not run the file.

## Requirements

Windows 10 or 11, 64-bit. 8 GB memory, 10 GB disk, more for large models and
image generation. No graphics card is required — the card decides how large a
model you get, not whether it runs.

First run downloads a few GB: the engine, and one model chosen for your machine.
