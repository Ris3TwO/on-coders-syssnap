<div align="center">

# Resource Monitor & Screen Capture Overlay

A lightweight, high-performance desktop overlay widget for real-time system monitoring and fast screen captures.

[![Tauri](https://img.shields.io/badge/Tauri-v2-blue?style=flat-square&logo=tauri&logoColor=white)](https://tauri.app/)
[![Rust](https://img.shields.io/badge/Rust-1.75+-orange?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Vue.js](https://img.shields.io/badge/Vue.js-v3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)](https://vuejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v3-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

</div>

---

## Overview

**Resource Monitor Overlay** is an always-accessible desktop application inspired by performance monitoring tools like IObit Performance Monitor. Built on Tauri v2 and Vue 3, it offers an unobtrusive widget interface (always-on-top or desktop-pinned overlay) for tracking system resources with minimal CPU/RAM overhead, paired with a screen capture module.

### Core Features

* **System Telemetry:** Real-time metrics for CPU usage, Memory (RAM), Disk I/O, and Network throughput powered by the Rust `sysinfo` crate.
* **Window Management:** Toggle between Frameless, Always-on-Top, or Always-on-Bottom (desktop layer) modes via native Tauri APIs.
* **Screen Capture:** Fast screen grabbing using native Rust OS integrations (`xcap`).
* **Minimal Footprint:** Native performance with low memory usage.

---

## Screenshots

> *Screenshots will be placed here once UI components are implemented.*

| Overlay Mode | Expanded Metrics |
| :---: | :---: |
| `![Overlay Preview](docs/screenshots/overlay-preview.png)` | `![Metrics Preview](docs/screenshots/metrics-preview.png)` |

---

## Tech Stack

* **Desktop Core:** Tauri v2 (Rust)
* **Frontend Framework:** Vue 3 (Composition API, TypeScript)
* **Styling:** Tailwind CSS
* **System Telemetry:** `sysinfo` (Rust Crate)
* **Screen Capture:** `xcap` / Native OS Capture APIs

---

## Prerequisites

Ensure you have the following installed on your machine:

* **Node.js:** v18.0.0 or higher
* **Package Manager:** `pnpm` (recommended)
* **Rust toolchain:** `rustc` and `cargo` (latest stable)
* **Platform Dependencies:** Follow the official [Tauri v2 Prerequisites Guide](https://v2.tauri.app/start/prerequisites/) for your operating system (Windows C++ Build Tools, Linux `webview2` / `gtk` dependencies, or macOS Xcode Command Line Tools).

---

## Getting Started

### 1. Clone the repository

```bash
git clone [https://github.com/Ris3TwO/on-coders-syssnap.git](https://github.com/Ris3TwO/on-coders-syssnap.git)
cd on-coders-syssnap
```

### 2. Install frontend dependencies

```bash
pnpm install
```

### 3. Run in development mode

```bash
pnpm tauri dev
```

## Build Process

To compile the application and produce production bundles (installers and executables):

### Validate code quality and tests

```bash
pnpm check:all
```

### Build binaries

```bash
pnpm tauri build
```

The compiled bundles (MSI, NSIS executable, or Linux packages) will be available in: `src-tauri/target/release/bundle/`

## License

Distributed under the MIT License. See `LICENSE` for more information.

---