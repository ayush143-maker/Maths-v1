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

## Manual review checklist

This is a checklist of actions to perform, not a record of verified results.

- Open the root `index.html` in a browser, or use the local preview steps above, and review the page content.
- Check that the audio reference in `index.html` points to `your.mp3` in the project folder and that the file is available at that path.
- Use the play and replay controls. Check whether the audio starts after interaction and whether replay behaves as intended; browser autoplay rules may require a tap.
- Inspect the page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the message and controls are visible and usable.
- If you changed the Google Fonts links, review the page typography with those changes in place.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check whether the play and replay controls and any other interactive elements can be reached and operated without a pointer. Check that focus order is sensible.
- Check that each focused control has a clearly visible focus indicator, including while using the audio controls.
- Review the play and replay controls for meaningful accessible names that communicate their actions. Check whether the message is available as text, rather than conveyed only through an image or other visual treatment.
- Check the message and control-label contrast against their backgrounds, including at narrow viewports and with the linked fonts unavailable.
- If the page includes moving or animated visual effects, check their behavior with the operating system's reduced-motion preference enabled. Review the audio controls separately so visitors can choose whether to start or replay audio.