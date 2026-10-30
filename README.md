# Maths-v1

A playful maths-themed music and quote microsite titled “Teacher: Maths is not Toxic.” The root `index.html` pairs a short message with play and replay controls for the local audio file `your.mp3`.

## Project files

The provided root-file inventory lists:

- `index.html` — the page entry point.
- `your.mp3` — the local audio file referenced by the page.
- `README.md` — this documentation.

The page also links to Google Fonts. Those font files are requested from external Google Fonts URLs, so they depend on network access.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deployment-readiness checklist

The following are recommendations for preparing and reviewing a published copy, not verified deployment results. No deployment provider or deployment configuration is identified here.

### Entry point and published directory

- [ ] Confirm the published directory contains `index.html` at the location expected to serve the page.
- [ ] Confirm the same published directory includes `your.mp3`, unless you have updated the audio reference to its new location.
- [ ] The provided project inventory lists these files at the repository root, and no separate build output is documented. If a publishing interface asks for a root or output directory, verify that its setting points to the directory containing the intended `index.html` and audio asset. Do not assume a generated output folder exists.
- [ ] Review any publishing settings before publishing; do not add a build command or output path unless the project’s actual configuration requires one.

### Relative assets and external requests

- [ ] Check the audio reference in `index.html` against the actual filename and location. If you rename or move `your.mp3`, update the reference accordingly.
- [ ] Preserve the relative location between the page and audio file, or adjust the path if their published locations differ.
- [ ] Check filename capitalization. A path that works on one system may not match a differently capitalized filename elsewhere.
- [ ] Remember that Google Fonts are external requests, while `your.mp3` is a local project asset. A font request failure may affect typography without indicating that the local audio file is missing.

### Safe configuration and content

- [ ] The provided root-file inventory does not list a separate configuration file or `.env.example`. The page is static HTML; anything included in the HTML or other browser-delivered files can be viewed by visitors.
- [ ] Do not put passwords, tokens, or other secrets in the page or tracked files.
- [ ] Review the page and audio before publishing. Do not include private information or audio you do not have permission to distribute.
- [ ] If changing fonts or other external links, confirm that the resulting page behaves as intended when those network requests are unavailable.

### Final preview after publishing

- [ ] Visit the published page after publishing and confirm the intended page loads from its expected address.
- [ ] Confirm the message, layout, and play and replay controls appear as intended.
- [ ] Use the controls to check audio playback. Browser autoplay rules may require a visitor to interact before audio starts.
- [ ] Check the browser console for errors and the network panel for failed page, audio, or font requests.
- [ ] Review the page at narrow and wide viewport sizes, including on mobile hardware where practical.
- [ ] If you make a change after this preview, review the published page again.

## Personalize the page and audio

Edit the message and presentation in `index.html`. Its Google Fonts links are external; changing or removing them may change the typography. If replacing `your.mp3`, keep its filename aligned with the reference in `index.html`, or update that reference to match the new filename and location. Keep the audio file in the published project when using the existing relative reference.

## Troubleshooting

These are diagnostic checks, not reports of known problems.

1. Confirm the published or local entry point is the intended `index.html`.
2. If audio does not load, compare its reference in `index.html` with the actual `your.mp3` filename and location. Check capitalization and the relative path.
3. Inspect the browser console for errors and the network panel for failed audio, page, or font requests. Try playback through the page controls, since browser autoplay restrictions may require a user gesture.
4. Distinguish external Google Fonts requests from the local audio file when investigating a failure; they have different sources.

## Review checklist

These are review steps, not verified test results.

- [ ] Use play and replay and observe whether audio starts after interaction and replay behaves as intended.
- [ ] After changing the audio or layout, repeat the path and browser-console checks above.
- [ ] Complete the final published-page preview described in the deployment checklist.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- [ ] Use Tab and Shift+Tab to check keyboard access to play, replay, and other interactive elements. Check focus order and visible focus indicators.
- [ ] Review controls for accessible names that communicate their actions, and check that the message is available as text.
- [ ] Check message and control-label contrast, including with the linked fonts unavailable.
- [ ] If the page includes moving or animated effects, check them with the operating system’s reduced-motion preference enabled. Ensure visitors can choose whether to start or replay audio.

## Final release review

- Open `index.html` from the published location and confirm the page loads as expected.
- Test with network access available and keep a sensible fallback for externally loaded resources.
- Review the published result once on a narrow screen and once on a wider screen; treat this as a release check, not an automated test report.
