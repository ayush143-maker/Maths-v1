# Maths-v1

A playful maths-themed music and quote microsite titled “Teacher: Maths is not Toxic.” The root `index.html` pairs a short message with play and replay controls for the local audio file `your.mp3`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Personalize the page and audio

Edit the message and page presentation in `index.html`. Its Google Fonts links are external; changing or removing them may change the typography. If replacing `your.mp3`, keep its filename aligned with the reference in `index.html`, or update that reference to match the new filename and location. Keep the audio file in the project folder when hosting the static page so the relative path continues to work.

Browser autoplay rules may require a visitor to tap a control before audio starts; use the controls when checking a replacement file.