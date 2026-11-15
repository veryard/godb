# godb releases

Downloads, release notes and the issue tracker for godb, a fast, light, native database client for MySQL 5.6+ /
MariaDB, PostgreSQL and SQLite. Drawn on the GPU, no webview, no CGO. Linux first, Windows second.

The source code is not published here; this repository holds the released files only.

## Download

Take the newest file for your system from the [latest release](../../releases/latest).

| File | For | Install |
|---|---|---|
| `godb-X.Y.Z-1.fc44.x86_64.rpm` | Fedora | `sudo dnf install ./godb-X.Y.Z-1.fc44.x86_64.rpm` |
| `godb-X.Y.Z-1-x86_64.pkg.tar.zst` | Arch Linux | `sudo pacman -U godb-X.Y.Z-1-x86_64.pkg.tar.zst` |
| `godb-X.Y.Z-linux-amd64.tar.gz` | any Linux | unpack, then `sh install.sh` (installs to `~/.local`, no root) |
| `godb-X.Y.Z-windows-amd64.zip` | Windows 10 or later | unzip and run `godb.exe` |
| `SHA256SUMS` | | `sha256sum -c SHA256SUMS --ignore-missing` |

Linux needs GTK 3 and Mesa (OpenGL); the packages depend on them. Only 64-bit x86 is built.

## Updates

On start godb reads the newest release number from this repository, at most once a day, and tells you when a newer
one exists. It sends no connection details and no data, and installs nothing itself. Turn it off in Settings, or
set `GODB_NO_UPDATE_CHECK=1`. To update, install the new files over the old ones.

## Versions

Version numbers are `MAJOR.MINOR.PATCH`, and follow the changes: a breaking change raises MAJOR, a new feature
raises MINOR, a fix raises PATCH. Each release's notes list the features and fixes in it.

## Problems and ideas

Open an issue and pick the matching form. Do not paste passwords, connection strings or data from your databases.

## Licence

See [LICENSE](LICENSE). Third-party software in godb is listed in `THIRD_PARTY_NOTICES.txt`, which is inside the
Linux tarball and attached to each release.
