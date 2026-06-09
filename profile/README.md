<!--
  PortableWeb — GitHub organization profile.
  This file is rendered at https://github.com/portableweb
  It lives in the special repo:  portableweb/.github  →  profile/README.md
  The banner is profile/banner.png (regenerate from profile/banner.html).
-->

<div align="center">

<img src="https://raw.githubusercontent.com/portableweb/.github/main/profile/banner.png" alt="PortableWeb — an open format for self-contained, interactive documents" width="100%" />

<br /><br />

[![Website](https://img.shields.io/badge/portableweb-0b0b15?style=flat-square&labelColor=0b0b15&color=7c3aed)](https://portableweb.github.io)
[![Open the app](https://img.shields.io/badge/open%20the%20app-%E2%86%97-2563eb?style=flat-square)](https://portableweb.github.io/app/)
[![Spec](https://img.shields.io/badge/spec-v0.1%20draft-20d6d2?style=flat-square)](https://github.com/portableweb/spec)
[![License](https://img.shields.io/badge/code-MIT-444?style=flat-square)](https://opensource.org/licenses/MIT)
[![Spec license](https://img.shields.io/badge/spec-CC--BY%204.0-444?style=flat-square)](https://creativecommons.org/licenses/by/4.0/)

</div>

---

## Interactive documents, built to last

**PortableWeb** is an open file format for self-contained, sandboxed, interactive documents.
Think of a `.pweb` bundle as **a single file that opens like a document and behaves like a small, sandboxed web app** — like PDF, but interactive; like a webpage, but a file you own.

It works offline. It doesn't expire when a CDN goes dark. It doesn't need a server, an account, or a subscription. Each spec version freezes a stable subset of the web platform, so a bundle built today renders correctly in any compatible viewer — the archival promise PDF/A makes for static documents, applied to interactive ones.

## What's inside a bundle

A `.pweb` is just a ZIP. Rename it to `.zip` and unpack it with anything — no proprietary container, no DRM, no hidden state.

```text
my-document.pweb
├── mimetype          # required · first entry, uncompressed (application/vnd.portableweb+zip)
├── manifest.json     # required · id, version, title, entry point, declared permissions
├── index.html        # required · the entry the viewer loads first
├── assets/           # images, fonts, media
└── scripts/ styles/  # JS modules and stylesheets
```

## Principles

| | |
|---|---|
| **Self-contained** | A bundle carries everything it needs. No CDN dependency, no broken script tags in five years. |
| **Sandboxed** | No filesystem access, network off by default, storage scoped per bundle. Permissions declared in the manifest, enforced by the viewer. |
| **Archival** | Each spec version freezes a stable feature subset. A v1.0 bundle renders identically in any v1.0 viewer, indefinitely. |
| **Owned** | A bundle is a file. No host, no account, no platform. It belongs to whoever holds it. |

## Try it now

The **[PortableWeb web app](https://portableweb.github.io/app/)** runs entirely in your browser — open and render any `.pweb`, pack a project folder into a bundle, validate one against the spec, or scaffold a new project. No install, no account, nothing leaves your device.

```bash
# Prefer a terminal? The CLI packs and validates bundles too.
npm install -g portableweb
pweb pack ./my-document      # build a .pweb from a folder
pweb validate my-document.pweb
```

## Projects

| Repository | What it is |
|---|---|
| [**spec**](https://github.com/portableweb/spec) | The format specification, schema, and example bundles |
| [**IETF Internet-Draft**](https://github.com/portableweb/spec/blob/main/ietf/draft-selvaraj-portableweb-format-00.md) | Formal specification submission: `draft-selvaraj-portableweb-format-00` |
| [**.github**](https://github.com/portableweb/.github) | This profile, plus the [portableweb.github.io](https://portableweb.github.io) website |
| [**Discussions**](https://github.com/portableweb/portableweb/discussions) | Ideas, questions, and design conversations |

> The CLI and viewer repos welcome PRs too — check the [open issues across the org](https://github.com/portableweb) for good starting points.

## Get involved

PortableWeb is a small project with large ambitions. The format is still in **draft**, which means early feedback shapes it most.

- 📖 **Read & comment on the spec** — open issues or PRs on [`portableweb/spec`](https://github.com/portableweb/spec).
- 🧪 **Build something** — make a `.pweb` and share it. Real-world usage drives the spec far more than theory.
- 🛠️ **Contribute code** — the CLI, viewer, and website all welcome PRs.
- 📣 **Spread the word** — tell anyone who works with documents, archival, AI-generated content, or interactive media.

<div align="center">
<br />
<sub>Spec licensed <a href="https://creativecommons.org/licenses/by/4.0/">CC-BY 4.0</a> · Code licensed <a href="https://opensource.org/licenses/MIT">MIT</a> · <a href="https://portableweb.github.io">portableweb.github.io</a></sub>
</div>

---

<div align="center">
<sub>This project is open for community contribution. All materials are contributed under the Creative Commons Attribution 4.0 license (CC-BY-4.0). This work is being submitted as input to the W3C Portable Web Content Format (PortableWeb) Community Group.</sub>
</div>
