# iPhone Simulator PWA

A small, static, interactive iPhone-style simulator. It is a browser-based demo, not iOS and not a real phone emulator.

## Deploy to Cloudflare Pages (Direct Upload)
1. Unzip `iphone-simulator-pwa.zip`.
2. Open https://dash.cloudflare.com/ and sign in / create an account.
3. In the dashboard, open **Workers & Pages** (the label may vary).
4. Choose **Create** / **Create application** → **Pages** → **Upload assets** / **Direct Upload**.
5. Name the project, for example `my-iphone-simulator`.
6. Upload the *contents* of this folder (make sure `index.html` is at the root, not inside another nested folder).
7. Deploy. Cloudflare will provide a public `https://PROJECT.pages.dev` URL you can share.

If the dashboard offers only Git integration, push these files to a GitHub repository and choose **Connect to Git** in Cloudflare Pages. For a plain static site, no build command is required and the output directory is the repository root (`/`).

## Test locally
Open `index.html` in a browser to try the basic simulator. PWA installation and service-worker offline caching require serving the files over HTTPS or localhost; they will not fully work from a `file://` URL.

## Included interactions
- Lock screen / home screen toggle
- Dynamic Island animation
- Wallpaper changes
- Demo Messages, Notes (saved in this browser), Settings, Photos, Camera, Weather, Music, Clock, Calendar, Maps, Mail, Health, Phone and Safari screens
- Responsive layout and PWA manifest/service worker

## Limitations
- These are simulated screens; no real iOS system, phone calls, camera capture, GPS, iMessage, Apple services or actual music playback.
- Notes are saved only in the current browser on the current device.
- External links from the Safari demo open in a new browser tab.
- A service worker caches core files; deploy updates may require a hard refresh if a browser retains an old cached version.
