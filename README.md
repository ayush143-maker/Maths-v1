# Maths-v1

Maths-v1 is a maths-themed canvas and music experience titled “Teacher : Maths is not Toxic.” Its `index.html` animates cyan and pink geometric paths with timed camera movement and sequential lyric lines. The sequence also includes the interstitial “meanwhile maths in my head :”. The PLAY button starts the timed sequence, and a REPLAY button appears after its 29-second timeline.

The page attempts to play audio from the `AUDIO_URL` constant, which is currently set to `your.mp3`; a source comment says to replace it with the desired song file. An attempt to play the file does not guarantee that audio will load or play in a particular browser.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. Use the page controls to try the sequence and audio; browser autoplay rules may require a visitor to interact before audio starts.

## Customize the page

Edit the message and presentation in `index.html`. To replace the audio, keep the filename aligned with the `AUDIO_URL` reference or update the reference to match the new filename and location. Keep the audio file alongside the page when using the existing relative path. The canvas resizes with the window.

The page loads Caveat, Dancing Script, and Poppins from Google Fonts, so typography may differ if those external requests are unavailable.

## Project files

- `index.html` — page content, canvas animation, sequence controls, and audio reference.
- `your.mp3` — local audio file referenced by the current `AUDIO_URL` value.

When checking a missing audio file, compare the reference in `index.html` with the actual filename, path, and capitalization. No build scripts or deployment configuration are documented.