# Maths-v1

A playful maths-themed music and quote microsite titled “Teacher: Maths is not Toxic.” The root `index.html` pairs a short message with play and replay controls for the local audio file `your.mp3`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Personalize the page and audio

Edit the message and presentation in `index.html`. Its Google Fonts links are external; changing or removing them may change the typography. If replacing `your.mp3`, keep its filename aligned with the reference in `index.html`, or update that reference to match the new filename and location. Keep the audio file in the project folder when hosting the static page so the relative path continues to work.

Browser autoplay rules may require a visitor to tap a control before audio starts; use the controls when checking a replacement file.

## Troubleshooting

Use these as diagnostic checks; they do not indicate known problems.

1. Confirm you opened the root `index.html`, the page’s entry point.
2. If audio does not load, check its reference in `index.html` against the local `your.mp3` file. Preserve the relative path and check filename capitalization, especially when hosted.
3. Inspect the browser console for errors and the network panel for failed audio, page, or font requests. Try playback through the page controls, since browser autoplay restrictions may require a user gesture.
4. The audio file is local project content; Google Fonts are external network requests. A font request failure is different from a missing local audio file and may only affect typography.

## Configuration and data handling

The listed root files contain no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files.

The page and `your.mp3` are project content. Review them before publishing, and do not include private information or audio you do not have permission to distribute.

## Review checklist

These are review steps, not verified test results.

- Review the page at narrow and wide viewport sizes, including on mobile hardware where practical.
- Use play and replay and observe whether audio starts after interaction and replay behaves as intended.
- After changing the audio or layout, repeat the path and browser-console checks above.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access to play, replay, and other interactive elements. Check focus order and visible focus indicators.
- Review controls for accessible names that communicate their actions, and check that the message is available as text.
- Check message and control-label contrast, including with the linked fonts unavailable.
- If the page includes moving or animated effects, check them with the operating system’s reduced-motion preference enabled. Ensure visitors can choose whether to start or replay audio.