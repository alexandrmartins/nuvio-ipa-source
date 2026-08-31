<div align="center">

# Nuvio IPA Source

**Automatic Nuvio `.ipa` source for SideStore**

<a href="https://github.com/NuvioMedia/NuvioMobile">
  <img src="https://img.shields.io/badge/Nuvio-Official%20Repository-1E88E5?style=for-the-badge&logo=github&logoColor=white" alt="Nuvio Official Repository">
</a>
<a href="https://github.com/alexandrmartins/nuvio-ipa-source/actions/workflows/update.yml">
  <img src="https://img.shields.io/github/actions/workflow/status/alexandrmartins/nuvio-ipa-source/update.yml?style=for-the-badge&label=Auto%20Update" alt="Auto Update">
</a>
<a href="https://raw.githubusercontent.com/alexandrmartins/nuvio-ipa-source/main/source.json">
  <img src="https://img.shields.io/badge/SideStore-Add%20Source-8A2BE2?style=for-the-badge" alt="Add to SideStore">
</a>

A lightweight SideStore source that automatically tracks the **official Nuvio Mobile releases** and exposes the available iOS/iPadOS IPAs in a SideStore-friendly format.

</div>

## ✨ Features

- 🤖 **Automatic updates** — checks the official Nuvio repository every **30 minutes**.
- 📦 **Official IPAs** — downloads point directly to the IPA assets published by NuvioMedia.
- 📝 **Release notes** — each version includes the corresponding GitHub release notes.
- 🕘 **Version history** — previous IPA releases are preserved whenever an IPA is available.
- 📊 **Repository stats** — the source About section keeps Nuvio's GitHub stars, commits, issues and pull requests up to date.
- ✅ **IPA validation** — a release without an IPA does not get added to the source.

## 📲 Add to SideStore

Add the following URL as a source in SideStore:

```text
https://raw.githubusercontent.com/alexandrmartins/nuvio-ipa-source/main/source.json
```

<a href="https://raw.githubusercontent.com/alexandrmartins/nuvio-ipa-source/main/source.json">
  <strong>➕ Add Nuvio IPA Source to SideStore</strong>
</a>

## 🔄 How it works

Every 30 minutes, GitHub Actions checks the latest release from the official Nuvio Mobile repository.

If a new release contains an `.ipa`, the workflow automatically updates `source.json` with:

- version number;
- release date;
- corresponding IPA download URL;
- IPA file size;
- SHA-256 digest, when provided by GitHub;
- the release notes from that exact GitHub release.

Existing versions are kept, so the source maintains a history of installable releases.

## 📚 Sources

**Official Nuvio Mobile repository**  
https://github.com/NuvioMedia/NuvioMobile

**This SideStore source**  
https://github.com/alexandrmartins/nuvio-ipa-source

**Raw `source.json`**  
https://raw.githubusercontent.com/alexandrmartins/nuvio-ipa-source/main/source.json

## ⚙️ Automation

The updater lives in:

```text
.github/workflows/update.yml
```

It runs on a 30-minute schedule and can also be triggered manually from the repository's **Actions** tab.

The workflow uses `actions/checkout@v5` and GitHub's public API to retrieve release and repository information.

## ⚠️ Disclaimer

This is a **community-maintained SideStore source**. It does not modify the Nuvio application or its official releases.

The IPAs are hosted by the official **NuvioMedia/NuvioMobile** GitHub releases; this repository only provides the SideStore source metadata and automation around it.

Nuvio is an open-source project. Please refer to the official repository for the project's own license, documentation and development information.

## 📄 License

The files in this repository are provided as part of this community source. **Nuvio itself is not licensed by this repository**; for Nuvio's license, see the official project repository.

<div align="center">

Made for SideStore · Powered by GitHub Actions

</div>
