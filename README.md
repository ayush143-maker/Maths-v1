# Maths-v1

A playful maths-themed music and quote microsite titled “Teacher: Maths is not Toxic.” The root `index.html` pairs a short message with play and replay controls for the local audio file `your.mp3`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Audio

If replacing `your.mp3`, keep its filename aligned with the reference in `index.html`. Browser autoplay rules may require a visitor to tap a control before audio starts. Keep the audio file in the project folder when hosting the static page so the page can find it.