## 🧪 Signature-Based Detection Lab
Objective:
To understand how signature-based malware detection works by generating file hashes and verifying them using VirusTotal.

## ⚙️ Steps Performed

1. Created Lab Directory
```bash
mkdir signature_lab
cd signature_lab
```
2. Downloaded Sample File
  Downloaded the malz.zip archive into the signature_lab directory.
- https://uploads.teachablecdn.com/attachments/h1DLyM50RiumcnnTBXCK_malz.zip
3. Listed Files
```bash 
ls
```
4.Unzipped the Archive
```bash
unzip malz.zip
```
- Password used: infected
- Extracted file: test.exe

5.Generated Checksums
```bash
sha256sum test.exe
md5sum test.exe
```
- SHA256: 2886677e1611d89f7c24c7a30dc4ef9c14109e8ba4318e5be721af81b4fcb6
- MD5: 9e7c18ed01675b77d14d6e26de9a3ddb
<img width="956" height="680" alt="Image" src="https://github.com/user-attachments/assets/6b9dfda7-1193-4a3f-87b4-29a7f7ab4738" />

6.Verified File on VirusTotal
- Opened Firefox and navigated to VirusTotal
- Pasted the SHA256 hash in the search bar.
- Reviewed the detection results (screenshot captured).
<img width="1918" height="881" alt="Image" src="https://github.com/user-attachments/assets/eeebe4ae-e0b0-408f-9205-405c1099039f" />

<img width="1918" height="881" alt="Image" src="https://github.com/user-attachments/assets/5ee791fb-fb9f-40e1-a371-df60262e4365" />

## ⚠️ Note
- Do not execute any suspicious files like test.exe. Always perform analysis inside a sandboxed or isolated VM for safety.
