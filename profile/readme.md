# 📺 AnimeTV Community

Welcome to the official organization profile for **AnimeTV-Fork / AnimeTV Community**. We are an open-source, community-driven collective dedicated to developing, refining, and maintaining the ultimate anime streaming experience for smart TVs, desktops, and mobile devices.

---

<p align="center">
  <img src="https://raw.githubusercontent.com/AnimeTV-Fork/AnimeTV/main/tools/logo-design/animetv-logo/animetv-logo-brand.png" alt="AnimeTV Brand Logo" width="600" />
</p>

<p align="center">
  <a href="https://github.com/AnimeTV-Fork/AnimeTV/releases"><img src="https://img.shields.io/github/v/release/AnimeTV-Fork/AnimeTV?logo=github&label=Stable%20Release&color=007acc" alt="Stable Release" /></a>
  <a href="https://github.com/AnimeTV-Fork/AnimeTV"><img src="https://img.shields.io/badge/Nightly%20Release-Active-orange?logo=amp&logoColor=fff" alt="Nightly Release" /></a>
  <a href="https://discord.gg/VGtGtRedGR"><img src="https://img.shields.io/discord/1199444562670792714?style=flat&labelColor=7289da&color=2c2f33&label=Discord&logo=discord&logoColor=ffffff" alt="Discord Support" /></a>
  <a href="https://github.com/AnimeTV-Fork/AnimeTV/blob/main/LICENSE"><img src="https://img.shields.io/github/license/AnimeTV-Fork/AnimeTV?color=green&label=License" alt="License" /></a>
</p>

---

## 🚀 Overview

AnimeTV is a hybrid application designed to bring seamless anime streaming to your living room. Optimized for **Android TV**, **Google TV**, and **Fire TV Remote** navigation, it also runs beautifully on desktop environments (Windows, Linux, macOS) and standard Android mobile devices.

### 🌟 Key Ecosystem Features
*   **Multi-Source Fallback:** Aggregates streams from 6+ independent providers with automated error-handling and fallback mechanics.
*   **Subtitles & Localization:** Soft-subtitle support with automatic real-time translation for **134 languages**.
*   **Media Synchronization:** Native integration with **MyAnimeList (MAL)** and **AniList** for real-time tracking.
*   **Smart Playback:** Auto-next episodes, skip intros/outros, filter out filler episodes, and variable playback speeds (0.5x - 3.0x).
*   **TV-Friendly UI:** Designed for standard remote controllers with a rich visual trailer integration, category reordering, and voice-assisted search.

---

## 🏗️ Technical Architecture

We build with performance, reliability, and modularity in mind. Our code utilizes a **Clean Architecture** paradigm using **TypeScript**, **Preact**, and **ESM**, separating system logic into strict, unidirectional dependency layers:

```
core/ (Shared Primitives) ──> domain/ (Business Rules) ──> data/ (Infrastructure) ──> presentation/ (UI/Store)
```

### ⚡ Key Architectural Decisions
*   **Strict Immutable Entities:** All core models use `readonly` structures to prevent runtime side-effect bugs.
*   **Functional Error Handling:** `Result<T, E>` types are returned instead of raising generic exceptions, forcing compile-time safety.
*   **Pure Dependency Injection:** A decorator-free, reflection-free pure-function DI container (`di/container.ts`) wires up adapters at bootstrap.
*   **Network Performance:** Built-in **CronetEngine** for HTTP/3 and QUIC transport protocol support alongside DNS-over-HTTPS (DoH).

---

## 🛡️ Privacy & Security First
*   **Zero Server Tracking:** We host no user-tracking or watch-history databases. All your watchlist, bookmarks, and histories are stored entirely **locally** via device `localStorage`.
*   **Built-in Ad & Tracker Blocker:** The custom webview and electron interceptors automatically blacklist analytics, metrics, and tracking script domains to protect your privacy and ensure lightweight network consumption.

---

## 👥 Governance & Community

We believe in a transparent, collaborative, trust-based model for community maintenance.

*   **Maintainers:** Manage code quality, architecture reviews, and automated release cycles.
*   **Contributors:** Community developers making features, translations, and scrapers.

### Contributions & Branch Rules
We maintain strict coding guidelines (using Prettier, ESLint, and Vitest) to ensure the codebase remains clean. All contributions are submitted via Feature Branches and Pull Requests requiring 1+ maintainer approvals.

---

## 📥 Get AnimeTV

Want to download the application for your device?

*   **Stable Release APK:** Download from the [Releases page](https://github.com/AnimeTV-Fork/AnimeTV/releases)
*   **Nightly Release APK:** Grab the latest test builds from the [Nightly builds](https://github.com/AnimeTV-Fork/AnimeTV)
*   **Desktop Versions:** Electron-based installers for Windows, Linux, and macOS are available under the releases tab of the respective repositories.

---

## ⚠️ Disclaimer

*   AnimeTV only scrapes public links from various websites to make stream navigation simpler.
*   We do not host or distribute any media files or databases. All media resources belong to their respective third-party providers.
*   If copyright issues are involved, please contact the host site directly.

---

<p align="center">
  Made with ❤️ by the AnimeTV Community. 
</p>
