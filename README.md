# Maths-v1

A playful maths-themed music and quote microsite titled “Teacher: Maths is not Toxic.” The root `index.html` pairs a short message with play and replay controls for the local audio asset `your.mp3`, also in the project root.

## Preview locally

Open `index.html` in a browser. Alternatively, run a local server from the project folder:

    python -m http.server 8000

Then visit http://localhost:8000. Reload the page after editing to review the change.

## Audio and editing

Keep the audio filename aligned with the page reference if replacing `your.mp3`. Browser autoplay rules may require the visitor to tap a control before audio starts, so try the controls in the browser when reviewing audio changes.

## Hosting

This is a static page. A static host can serve the project files; keep `your.mp3` in the project root so the page can find it.