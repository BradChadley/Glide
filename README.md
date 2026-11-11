# Glide

A personal Windows desktop companion for RustDesk and Tailscale, with guided setup, diagnostics, and signed in-app updates.

**Downloads paused:** version 0.12.0 was withdrawn after Microsoft Defender detected Glide-Setup.exe as Trojan:Win32/Wacatac.B!ml. The cause is under investigation; a false positive has not been confirmed. Do not restore the installer, allow the threat, or disable antivirus protection.

Run Setup once on each PC. Close an older Glide window first, click **Install Glide**, then use the new Glide shortcut. Existing settings are preserved.

For future releases, open **Devices → Updates**, choose **Download update**, then **Restart Glide** when ready. Update each PC independently. No ZIP extraction is needed.

## Requirements

- Windows 11, x64, with .NET Framework 4.8.
- Tailscale on both PCs, signed into the same private network.
- Glide's verified RustDesk engine and the guided host setup.

RustDesk and Tailscale are separate applications. Their binaries are not included in these release assets. No account data, device details, passwords, or release-signing private key are published here.

## Updates and recovery

Glide checks a pinned RSA-3072/SHA-256 release signature and package/file hashes before installing. Downloads are bounded and restricted to GitHub release hosts. Updates are staged beside the active app, and the previous version remains available under **Updates → Details & recovery**. If a new version cannot render its initial window, the updater restores the previous version.

The first setup executable is not Authenticode-signed. The release-signing key authenticates update payloads after that initial trust step; it is not a Windows publisher certificate. This personal preview has not had an independent security audit. A local startup check does not establish remote connection readiness.

Signed metadata expires and must be refreshed by the publisher. Expiration prevents installing stale updates; it does not prevent launching an installed version. Key rotation or changes to the original launcher require a new trusted setup.

## Source and notices

The release includes a separate source ZIP with the build script and tests. Runtime guides include the updater's boundaries and recovery instructions. RustDesk and Tailscale retain their own licenses and notices.

- [RustDesk](https://github.com/rustdesk/rustdesk)
- [Tailscale](https://tailscale.com/)

This repository currently distributes a personal app and its release assets. It is not an official RustDesk or Tailscale project.
