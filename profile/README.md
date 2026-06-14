<!--
  PortableWeb — GitHub organization profile.
  Rendered at https://github.com/portableweb  (repo: portableweb/.github → profile/README.md)
  Hero is the animated profile/flow.svg; static brand banner is profile/banner.png.
-->

<div align="center">

<img src="https://raw.githubusercontent.com/portableweb/.github/main/profile/flow.svg" alt="The PortableWeb loop: you ask an AI to build interactive web content, it is generated, you pack it as a single .pweb file, and it runs everywhere — phone, Mac, PC, or shared with a friend." width="100%" />

<br /><br />

# PortableWeb

**The file format for a portable web bundle, built to run everywhere.** One `.pweb` file that runs on any device, fully offline — no server, no web origin, no app store.

*PortableWeb is not an AI platform. It’s the open format for what you — and any AI tool — build with web technology.*

[![Website](https://img.shields.io/badge/portableweb.org-0b0b15?style=flat-square&labelColor=0b0b15&color=7c3aed)](https://portableweb.github.io/)
[![Open the app](https://img.shields.io/badge/open%20the%20app-%E2%86%97-2563eb?style=flat-square)](https://portableweb.github.io/app/)
[![W3C Community Group](https://img.shields.io/badge/W3C-Community%20Group-005a9c?style=flat-square)](https://www.w3.org/community/portableweb/)
[![IETF Internet-Draft](https://img.shields.io/badge/IETF-Internet--Draft-20d6d2?style=flat-square&labelColor=333)](https://www.ietf.org/archive/id/draft-selvaraj-portableweb-format-01.html)
[![Spec](https://img.shields.io/badge/spec-v0.1%20draft-9f67f5?style=flat-square)](https://github.com/portableweb/spec)
[![License](https://img.shields.io/badge/code-MIT-444?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Interactive content is built in minutes now. Where does it live?

AI-assisted tools have changed the economics of building interactive web content: a simulation, a small game, a 3D experience, or a data-rich report that used to take days of skilled work now takes minutes — and it’s being made **by the million**, with whichever tools people already use. None of it has a natural place to live.

Every existing option forces an unacceptable tradeoff:

| Option | The catch |
|---|---|
| **Deploy to a server** | Needs hosting and a live connection. Wrong tool for ephemeral or personal content — and it vanishes when the host goes dark. |
| **Publish to an app store** | Developer accounts, review cycles, maintenance. Absurd for the volume of artifacts being made today. |
| **PDF** | Portable and archival, but it flattens everything. A game loop or live simulation can't survive the trip. |
| **EPUB** | Its scripting enhances a *reading* experience; it can't represent a game or a real-time simulation. |
| **Web Bundles** | A network transport optimization, never broadly implemented. No offline-first execution model. |
| **Web App Manifest** | Describes an already-deployed app. Tied to a web origin — it says nothing about content with no server at all. |

> **No existing format treats interactive web content as a portable, self-contained, immediately runnable unit.**

## PortableWeb is that unit.

A PortableWeb bundle (`.pweb`) packages the HTML, CSS, JavaScript, and media of an interactive experience into **one file**. A compatible viewer opens it in its own sandboxed window — on desktop, mobile, or anywhere — entirely offline, with no deployment, no web origin, and no browser required.

It behaves like a document: save it, copy it, email it, archive it, or AirDrop it across the room. It works the first time and the thousandth, and it doesn't expire when a CDN goes dark. The format is **content-model agnostic** — a bundle can hold a game, a presentation, a simulation, a 3D experience, a scientific model, a report, or a book.

**And the loop closes.** Today you ask a model to build something, then pack the result as a `.pweb`. As models mature, they'll emit the `.pweb` directly — the finished, portable file, instantly usable everywhere.

## What's inside a bundle

A `.pweb` is just a ZIP. Rename it to `.zip` and unpack it with anything — no proprietary container, no DRM, no hidden state.

```text
my-document.pweb
├── mimetype          # required · first entry, uncompressed (application/vnd.portableweb+zip)
├── manifest.json     # required · id, version, title, entry point, declared permissions
├── index.html        # required · the entry the viewer loads first
├── assets/  media/   # images, fonts, audio, video
└── scripts/ styles/  # JS modules and stylesheets
```

## Principles

| | |
|---|---|
| **Self-contained** | A bundle carries everything it needs. No CDN dependency, no broken script tags in five years. |
| **Sandboxed** | No filesystem access, network off by default, storage scoped per bundle. Permissions declared in the manifest, enforced by the viewer, deny-by-default. |
| **Archival** | Each spec version freezes a stable feature subset. A v1.0 bundle renders identically in any v1.0 viewer, indefinitely. |
| **Owned** | A bundle is a file. No host, no account, no platform. It belongs to whoever holds it. |

## Standards — built in the open

PortableWeb isn't a private format. It's being developed where the web is built:

- 🌐 **[W3C Community Group](https://www.w3.org/community/portableweb/)** — the *Portable Web Content Format* CG. Container, manifest, viewer conformance, per-bundle storage, and a genuinely new permission-gated **offline peer-to-peer channel** (Bluetooth / Wi-Fi Direct) for multiplayer and collaboration without any server. Anyone may join; W3C membership not required.
- 📜 **[IETF Internet-Draft](https://www.ietf.org/archive/id/draft-selvaraj-portableweb-format-01.html)** — `draft-selvaraj-portableweb-format` defines the container, manifest schema, security considerations, and the `application/vnd.portableweb+zip` media type.

## Try it now

The **[PortableWeb web app](https://portableweb.org/app/)** runs entirely in your browser — open and render any `.pweb`, pack a project folder into a bundle, validate one against the spec, or scaffold a new project. No install, no account, nothing leaves your device.

## Get involved

PortableWeb is a small project with large ambitions. The format is still in **draft**, which means early feedback shapes it most.

- 🌐 **Join the [W3C Community Group](https://www.w3.org/community/portableweb/join)** — help shape the spec where it's being standardized.
- 📖 **Read & comment on the spec** — open issues or PRs on [`portableweb/spec`](https://github.com/portableweb/spec).
- 🧪 **Build something** — make a `.pweb` and share it. Real-world usage drives the spec far more than theory.
- 🛠️ **Contribute code** — the CLI, viewer, and website all welcome PRs.
- 📣 **Spread the word** — tell anyone who works with documents, archival, AI-generated content, or interactive media.

<div align="center">
<br />
<sub>Spec licensed <a href="https://creativecommons.org/licenses/by/4.0/">CC-BY 4.0</a> · Code licensed <a href="https://opensource.org/licenses/MIT">MIT</a> · <a href="https://portableweb.org">portableweb.org</a></sub>
</div>
