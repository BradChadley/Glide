# Glide

A personal Windows remote desktop companion for RustDesk over Tailscale.

[Download Glide for Windows](https://github.com/BradChadley/Glide/releases/latest/download/Glide-Setup.msi)

Close the old Glide window, open the MSI, and click **Install**. Do this once on each PC. Open Glide using its new desktop or Start menu shortcut. Afterward, use **Devices → Updates → Download update → Restart Glide**.

Windows Installer handles the application files, shortcuts, repair and removal. Setup does not change existing pairing, passwords, virtual displays, RustDesk settings or Tailscale policies. Updates keep the existing pinned signing key and previous-version recovery.

Windows 11 x64 with .NET Framework 4.8 or later is the intended platform. RustDesk and Tailscale are installed separately. No router port forwarding is needed.

## Verification and source

[Release verification](https://github.com/BradChadley/Glide/releases/latest/download/Release-verification.txt) · [Source archive](https://github.com/BradChadley/Glide/releases/latest/download/Glide-source-0.13.0.zip) · [Release history](https://github.com/BradChadley/Glide/releases)

The 0.13.0 app passed 211 isolated regression checks. Its MSI passed Windows Installer consistency validation and contains no custom installation actions or embedded setup executable. Defender reported no threats on the exact final MSI, app, runtime ZIP and source ZIP. The release report contains hashes and testing limits. A first live installation still needs user testing.

The MSI and launcher do not have a Windows Authenticode publisher certificate. Glide's signed update metadata is a separate protection; it does not establish Windows publisher reputation.

## Retired 0.12.0 installer

The old custom `Glide-Setup.exe` was withdrawn after a Microsoft Defender detection. It remains unavailable. The exact cause is unconfirmed and no vendor false-positive determination was requested. The new MSI replaces the custom installer architecture; it does not clear the old file. Do not restore the old installer or disable protection. Negative scans are point-in-time evidence, not a guarantee.

This is a personal project, not an independently audited remote desktop product. No personal settings, credentials, diagnostic reports or private release key are published.