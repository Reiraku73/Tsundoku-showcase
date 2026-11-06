# 📚 Tsundoku

<p align="center">
  A reader for manga, manhwa, manhua and comics — focused on the titles big platforms ignore,<br/>
  with a <b>Studio</b> where indie artists publish their own work.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/app-Android-3ddc84" />
  <img src="https://img.shields.io/badge/web-in%20development-lightgrey" />
  <img src="https://img.shields.io/badge/status-Demo-orange" />
  <img src="https://img.shields.io/badge/version-v0.4.3-blue" />
  <img src="https://img.shields.io/badge/built%20with-Expo%20%C2%B7%20React-61dafb" />
  <img src="https://img.shields.io/badge/backend-Supabase-3ecf8e" />
</p>

<p align="center">
  👉 <a href="../../releases/latest"><b>Download the latest demo APK</b></a> &nbsp;·&nbsp;
  <a href="https://mateoorodaz.vercel.app"><b>Screenshots & demo video</b></a>
</p>

---

## 🧩 One product, two clients

Tsundoku is a mobile app **and** a website, both on the same backend. The app is the main product; the web complements it.

| | 📱 **App** (Android) | 🌐 **Web** |
|---|---|---|
| **For** | Readers | Creators and visitors |
| **What it does** | Read, discover, build your library, upload from the phone | Public landing page and the **Studio**, where creators upload and manage their series |
| **Status** | Demo APK available (v0.4.3) | In development, not deployed yet |

---

## 📱 The app

* 📖 **Own streaming reader** — opens a CBZ and shows the first page as soon as it's extracted, without waiting for the whole file
* ↕️ **Two reading modes** — continuous vertical scroll or page by page, LTR or RTL, with configurable tap zones
* ⏭️ **Seamless chapters** — the next one preloads 8 pages before the end
* 📶 **Online or offline** — streams by default; download a chapter (or the whole series) to read it without a connection
* 🗣️ **Chapters in several languages** — the reader picks your reading language and offers the others when a chapter isn't in it
* 📚 **Library** with custom folders, your own drag-to-sort order and a "Continue reading" row
* 📤 **Upload from the phone** — a CBZ or just the chapter's loose images, packed for you
* ⭐ **Netflix-style home** — rotating featured banner, rows by category, tag filters
* 🌐 **Four languages** (EN, ES, JA, KO) — interface, reading language and a per-series override

<p align="center">
  <img src="assets/Home.png" width="250"/>
  <img src="assets/Reader.png" width="250"/>
  <img src="assets/Profile.png" width="250"/>
</p>

---

## 🌐 The web

* 🏠 **Public landing page** — the project, its vision and the development status
* 🎨 **Studio** (sign-in required) — upload series and chapters with the same flow as the app
* 🔀 **Drag-and-drop chapter ordering** — labels like `10`, `10.5` or `Extra`, with the real order stored separately
* 🔎 **Official title detection** — checks AniList, Open Library and the own database: licensed titles can only be uploaded by admins; everything else is indie

<p align="center"><i>Screenshots coming when the web is deployed.</i></p>

---

## 🛠️ Tech stack

| | |
|---|---|
| **App** | Expo SDK 58 · React Native 0.88 (New Architecture) · TypeScript · Zustand · expo-router |
| **Web** | React 19 · Vite · TypeScript · react-router · dnd-kit |
| **Backend** | Supabase: PostgreSQL with Row Level Security on every table, Auth and Storage |
| **Builds** | EAS Build |

---

## 🧠 Engineering highlights

* 🔐 **Database security audit** — closed a privilege escalation and premium content reachable through the Storage API, with RLS migrations tested in rolled-back transactions first
* 🧱 **Staged database refactor** without breaking either client: chapters with files per language and an editable order
* ⬆️ **Seven Expo SDK upgrades in two days** (51 → 58), plus React Native's New Architecture
* 🧮 **Base64 decoder of its own**, because `atob()` doesn't exist in Hermes
* 💳 **Monetization designed around store rules** — donations happen outside the app, so they don't fall under in-app purchase fees

---

## 🚧 Status

Active development (phase 5 of 6). The demo APK works; public sign-up stays closed until launch.
Demo builds before **v1.0.0** are published as APKs in this repo's [releases](../../releases).
Since **v0.4.3** older APKs no longer work (the backend changed how chapters are stored), so always grab the latest one.

---

## ⚠️ About this repository

<p align="center">
  This is a <b>public showcase</b>: the README, the screenshots and the APK releases.<br/>
  The source code is private; it's available on request for interviews.
</p>

---

## 📬 Contact

<p align="center">
  Feedback, collaboration or opportunities: <a href="mailto:mateo.orodaz4@gmail.com">mateo.orodaz4@gmail.com</a>
</p>
