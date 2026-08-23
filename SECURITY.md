# Security Policy

## Reporting a vulnerability

Please **do not** report security vulnerabilities through public GitHub issues.

Send a description of the issue (affected version, steps to reproduce, impact) by e-mail to
**[EFA_CAMverse@lse.cc](mailto:EFA_CAMverse@lse.cc)**. You will receive a confirmation, and we will keep you
informed about the fix. Reports in English or German are welcome.

Bitte melden Sie Sicherheitslücken **nicht** über öffentliche GitHub-Issues, sondern per E-Mail an
**EFA_CAMverse@lse.cc** (betroffene Version, Schritte zur Reproduktion, Auswirkung).

## Supported versions

Only the latest release published on the [Releases page](../../releases/latest) receives fixes. EFA CAMverse checks
for updates at startup and offers to download the current version.

## Verifying downloads

All binaries (installer, application, libraries) are signed with an Extended Validation code-signing certificate
issued to **LEBERT Software Engineering GmbH & Co. KG**. Every release ships a `SHA256SUMS.txt` with the checksums of
its assets. See the README for how to check signature and checksum.
