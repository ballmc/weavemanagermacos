# Weave Manager for MacOS

<div style="display: flex; justify-content: space-between;">
  <img width="400" alt="Screenshot 1" src="https://github.com/ballmc/weavemanagermacos/assets/140663688/0b2b1675-ed4a-4226-a762-fbc434a945c9">
  <img width="400" alt="Screenshot 2" src="https://github.com/ballmc/weavemanagermacos/assets/140663688/5deeb32a-2f1d-46e3-a14b-131cf7e5f46d">
</div>

## Overview

This is a prebuilt version of Weave Manager designed specifically for MacOS. It addresses issues related to `lunar_launcher_inject` not working on MacOS. Please note that this release is somewhat finicky, and certain configurations need to be manually set up.

## Prerequisites

### For Brand New Weave Users (replace `your_name` with your computer's user name)

1. If you don't have a `.weave` folder, create it in `/Users/your_name/.weave`.
2. If you don't have a `mods` folder, create it in `/Users/your_name/.weave/mods`.
3. Drag and drop your desired weave mods into `/Users/your_name/.weave/mods`.

## Running Weave Manager

### Setup Steps

1. Download `Weave-Loader-Agent-0.2.4.jar` (or whatever the latest version is called) from [Weave Loader Releases](https://github.com/Weave-MC/Weave-Loader/releases).
2. Rename the downloaded file to `loader.jar`.
3. Drag and drop the `loader.jar` file into `/Users/your_name/.weave`.

### Using Weave Manager

1. Download either `Weave.Manager.app.tar.gz` or `Weave.Manager_0.1.0_universal.dmg`.
2. Run the application.
3. Launch Lunar Client and then relaunch it using Weave Manager.

### Code Changes

### The issues I fixed with the original Weave Manager for documentation purposes

1. Built a universal binary on an M1 Mac by running

`rustup target add x86_64-apple-darwin`

`npm run tauri build -- --target universal-apple-darwin`

2. Commented out this in main.rs

<img width="867" alt="image" src="https://github.com/ballmc/weavemanagermacos/assets/140663688/410eca3c-ee65-4b0a-870a-37f82eac851f">

4. Added default placeholder icons to bypass build errors
   
<img width="344" alt="image" src="https://github.com/ballmc/weavemanagermacos/assets/140663688/d41f0f0f-21ab-4623-a7e4-87ebeda6d712">

6. Edited tauri.conf.json's scope to fix some permission/path issues for MacOS
   
<img width="684" alt="image" src="https://github.com/ballmc/weavemanagermacos/assets/140663688/7a5839ea-6141-47c7-ad45-cb84047ab895">

8. Edited tauri.conf.json's icons
   
<img width="260" alt="image" src="https://github.com/ballmc/weavemanagermacos/assets/140663688/35400911-6540-4b3e-a6ff-a4c278b43a49">

Original Weave Manager Link: https://github.com/Weave-MC/Weave-Manager
