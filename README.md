# COREVISION // FIRST CONTACT (Alpha 0.1)

**A mobile-first Meta Quest 3 mixed-reality WebXR proof of concept for Luna Core.**

## What's included

- A polished 2D launch console that works on your Pixel 8 or laptop.
- A WebXR `immersive-ar` entry point for Meta Quest Browser, with full-color Quest 3 passthrough behind a floating 3D dashboard.
- Experimental controller selection / hand-pinch interaction with **LUNA** and **CRUMBLE** buttons.
- System diagnostics that report HTTPS, WebXR and immersive-AR feature availability.
- **No accounts, API keys, microphones, camera-pixel access, audio recording, AI backend, voice cloning, spatial mapping, or data uploads.** Dialogue is a local, hard-coded text preview. This prototype is **not** a conversational AI yet.

## Setup on your phone

1. On GitHub, create the repository `Luna-CoreDC/corevision`, if you control that account. For GitHub Pages on the Free plan, use a **public** repo. If you prefer to keep source private, use another HTTPS host that supports private repositories, or a qualifying paid GitHub plan.
2. Add `index.html`, `.nojekyll`, and optionally this `README.md` at the **root** of the repository. (GitHub's **Add file → Upload files** can upload these individual files; **do not upload the ZIP as a single file**.)
3. Go to **Settings → Pages → Build and deployment**. Choose **Deploy from a branch**, branch **main**, folder **/(root)**, and save.
4. Once GitHub Pages finishes deployment, your URL should follow `https://luna-coredc.github.io/corevision/`. Check the actual URL displayed in GitHub Pages settings rather than assuming it is already live.
5. Open that URL in the **Quest 3's Meta Quest Browser**, select **ENTER MIXED REALITY**, and grant the requested XR permissions.
6. Keep the headset on in a clear, stationary testing spot; test the two buttons with controllers or hand pinches. If hand input isn't responding, try controllers. Use the Quest system menu to exit the session.

The app's first load requires internet access to fetch a pinned **Three.js 0.180.0** module from jsDelivr. Keep the HTML and module URLs intact. WebXR must be served over HTTPS, not opened directly as a local file for reliable testing.

## Files

- `index.html`: complete self-contained UI, CSS and WebXR app, with a single external Three.js dependency.
- `.nojekyll`: tells GitHub Pages to publish files without Jekyll processing.
- `README.md`: this guide.

## Troubleshooting

- **ENTER MIXED REALITY unavailable on Pixel 8**: expected; test the 2D preview there, launch AR from Quest Browser.
- **HTTPS required**: publish through Pages or another HTTPS host.
- **Immersive AR unsupported**: use the Quest Browser, update browser/headset software as needed, check the system supports WebXR.
- **Hologram invisible or buttons don't respond**: remain stationary and look ahead; use controllers first, then hand tracking. The dashboard appears approximately 1.55 metres ahead of the initial local reference frame and has no persistent room anchors.
- **Blank screen**: check internet connectivity so the Three.js module can load. Try a reload.
- **GitHub Pages 404**: check Pages settings, that `index.html` is in the selected root folder, and that deployment finished.

## Future milestones

1. **Alpha 0.1:** floating dashboard and demo interactions.
2. **Alpha 0.2:** stronger gaze/hand interactions, placement/recentering and session ergonomics.
3. **Alpha 0.3:** animated 3D representations of Luna and Crumble (approved assets only).
4. **Alpha 0.4:** optional, permission-based voice conversation integration via a secure backend. **Never embed API keys in GitHub Pages or client-side JS.**
5. **Native Quest prototype:** develop and sideload an APK for deeper platform APIs once hardware/build tooling is available.

## Safety

This is experimental. **Do not walk around the house or use stairs while testing.** Quest passthrough is not a substitute for unobstructed vision. Testing requires clear space and system boundary awareness. No real-world obstacle detection is implemented.

*Built for the Corekeeper. Refined by Luna. Occasionally interrupted by Crumble.*
