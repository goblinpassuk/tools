# QR Pocket

Two small, privacy-friendly browser apps:

- **Notes to QR** turns text into a QR code, copies the original note, and downloads the code as a PNG.
- **QR Scanner** scans codes from a device camera or an uploaded image, then copies or opens the result.

## Run locally

Camera access requires a secure context (`https://` or `localhost`). Start any static server in this folder, for example:

```powershell
python -m http.server 8080
```

Then open `http://localhost:8080`.

The scanner library is included in the project. The QR generator and fonts load from public CDNs, but note text and scan results are processed only in the browser and are not uploaded by this app.

## Publish on GitHub Pages

1. Create a new GitHub repository, such as `qr-pocket`.
2. Add this folder to the repository and push it to the `main` branch.
3. On GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **GitHub Actions** as the source.
5. Open the **Actions** tab and wait for **Deploy QR Pocket to GitHub Pages** to finish.

The site will be available at `https://YOUR-USERNAME.github.io/qr-pocket/`. Every future push to `main` publishes the latest version automatically.

## Install as an app

After opening the published site in Chrome, Edge, or Safari, use the browser's **Install app** or **Add to Home Screen** option. QR Pocket includes a web app manifest and offline cache, so it launches like a standalone app.
