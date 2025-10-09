# Overview

**Title:** Signature-based detection lab

**Purpose**
This lab demonstrates a minimal, safe workflow for extracting a password-protected malware archive, inspecting extracted artifacts, and creating cryptographic file signatures (SHA256 and MD5) that can be used for signature-based detection and tracking.

**Objectives**
- Safely extract files from `malz.zip` (password: `infected`) into a controlled directory.
- Inspect file types and metadata without executing any binaries.
- Produce SHA256 and MD5 checksums for suspicious files (e.g., `test.exe`) and for all extracted files.
- Save analysis outputs and screenshots so results can be reviewed or used to craft YARA signatures or IOC lists.

**Environment & Safety**
- **Always** run this lab inside an isolated environment (a disposable VM, sandbox, or container with no network access unless required and controlled).
- Do **not** execute any extracted binaries on the host.
- Take a snapshot/backup of the VM before any dynamic analysis.
- Never commit real malware samples to a public repository. Only commit logs, checksums, and sanitized outputs.

**Prerequisites**
- `unzip` (supports `-P` for password)
- `sha256sum`, `md5sum`
- `file`, `strings` (for safe static inspection)
- A working directory where `malz.zip` is stored

**Quick workflow (high-level)**
1. Create working directory `signature_lab/` and enter it.
2. Place `malz.zip` in the directory.
3. Create `extracted/` and unzip using the password `infected`.
4. List and inspect extracted files with `ls -la` and `file`.
5. Identify suspicious executables (e.g., `test.exe`) using filename patterns or file output.
6. Generate SHA256 and MD5 checksums for individual files and for the full extraction set.
7. Save `file` outputs, `strings` extracts, and checksum files into a `checksums/` folder.
8. Save screenshots of each major step into `screenshots/` and reference them in the README.
9. Keep all analysis results (hash lists, file metadata) but **do not** upload raw samples to public repositories.

**Expected outputs**
- `extracted/` — extracted sample files
- `checksums/all.sha256` — SHA256 sums for all extracted files
- `checksums/all.md5` — MD5 sums for all extracted files
- `checksums/<f
