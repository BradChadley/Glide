# Glide

A personal Windows remote desktop companion for RustDesk over Tailscale.

[Download Glide for Windows](https://github.com/BradChadley/Glide/releases/latest/download/Glide-Setup.msi)

Install once on each PC and use the new Glide shortcut. **Devices → Updates** then checks Glide, RustDesk and Tailscale together. Existing installed Glide 0.13 can update in-app.

Prepare downloads while connected; finish the session and close the RustDesk viewer before installing. Windows may ask for approval. Update Glide on **both PCs before RustDesk** so both recognize the reviewed 1.5.3 runtime. Tailscale 1.104.6 is current at publication.

Glide verifies its signed release feed, pinned RustDesk packages and official signed Tailscale installers. Host updates keep an encrypted configuration recovery copy and verify the running version, service and security settings afterward. Unconfirmed results offer verification and a redacted report. No automatic reboot, password reset, network-policy replacement or silent downgrade is requested.

Installers restart their services, so this is not a zero-downtime updater. Connection checks reduce interruption risk; do not start new sessions during installation, and finish other private-network activity first. Vendor and Windows automatic updates operate independently. Future RustDesk versions require a reviewed Glide release.

Windows 11 x64 with .NET Framework 4.8 or later is the intended platform. Initial RustDesk and Tailscale installation uses their own installers. No router port forwarding is needed.

## Verification and source

[Release verification](https://github.com/BradChadley/Glide/releases/latest/download/Release-verification.txt) · [Source archive](https://github.com/BradChadley/Glide/releases/download/v0.14.0/Glide-source-0.14.0.zip) · [Release history](https://github.com/BradChadley/Glide/releases)

The 0.14.0 app passed 226 isolated regression checks. Production vendor download/signature checks and isolated signed Glide staging passed. Its MSI passed consistency validation and contains no custom installation actions or embedded setup executable. Defender reported no threats on the exact final MSI, app, runtime ZIP and source ZIP. Actual vendor installation, settings preservation through a live upgrade and the two-PC experience still need user testing; the release report records these limits.

The MSI and launcher do not have a Windows Authenticode publisher certificate. Glide's signed update metadata is a separate protection; it does not establish Windows publisher reputation.

## Retired 0.12.0 installer

The old custom `Glide-Setup.exe` was withdrawn after a Microsoft Defender detection. It remains unavailable. The exact cause is unconfirmed and no vendor false-positive determination was requested. The MSI replaces the custom installer architecture; it does not clear the old file. Do not restore the old installer or disable protection. Negative scans are point-in-time evidence, not a guarantee.

This is a personal project, not an independently audited remote desktop product. No personal settings, credentials, diagnostic reports or private release key are published.
