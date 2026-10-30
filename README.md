# Maths-v1

Maths-v1 is a playful maths-themed music and quote microsite titled “Teacher: Maths is not Toxic.” Its root `index.html` pairs a short message with play and replay controls for the local audio file `your.mp3`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. Use the page controls to try audio playback; browser autoplay rules may require a visitor to interact before audio starts.

## Customize the page

Edit the message and presentation in `index.html`. The page links to Google Fonts, so typography may differ if those external requests are unavailable. To replace the audio, keep the filename aligned with the page’s reference or update the reference to match the new filename and location. Keep the audio file alongside the page when using the existing relative path.

## Project files

- `index.html` — page content, presentation, and audio controls.
- `your.mp3` — local audio referenced by the page.

When checking a missing audio file, compare its reference in `index.html` with the actual filename, path, and capitalization. Google Fonts are external resources; their availability is separate from the local audio file. No build scripts or deployment configuration are documented.