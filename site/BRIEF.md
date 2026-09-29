# Recordly download page — brief

## Goal
One landing page for **recordly.neatoventures.com**. It explains what Recordly does and lets people download it. Its main job: a visitor understands Recordly in under a minute and downloads the right installer.

## Output
- `site/index.html`: one complete, self-contained HTML document (`<!doctype html>` included). All CSS and JS are inline. The only external resource allowed is Google Fonts (Space Mono + Outfit). No other CDNs, no external images, no analytics.
- Images come only from `site/media/` (relative paths): `media/icon-256.png` and `media/icon-64.png` (Recordly's app icon, a blue rounded square with a white flower-like mark). Draw any other visuals as inline SVG or CSS. **Do not use the upstream demo GIFs.** They show a real person's face and a public figure's social profile.
- It must work at 360px phone width with no horizontal scroll, and on desktop.

## Brand
Follow the **Neato Ventures brand guidelines** exactly:
- Full text: `/tmp/claude-0/-home-user-Recordly/5adbde06-b507-5350-bb37-c5351f92ed99/scratchpad/brand/text.txt`
- Page renders: `.../scratchpad/brand/p01.png` … `p11.png`. Look at p03–p07 and p10 at least.

Key rules, in short:
- Cream ground `#F6F5EE` with visible paper grain. Deep brown `#291A14` is the only ink. Teal `#45C4C2` is for structure and status. Burnt orange `#F75A33` is for the action, with at most one orange fill per viewport. Mustard `#F2C84A` means "Coming soon". Retro brown `#804C37` is for chrome bands, the footer and offset shadows.
- Small text uses the darker inks: orange ink `#A53012`, teal ink `#1E6B6B`. Other colors: plate `#F0EEE6`, border `#CFC2BE`, CRT bezel `#2A1B14`, CRT phosphor `#A8F7C9`.
- Space Mono (uppercase, tracked) for every heading, nav item, button, label, chip and number. Outfit for body text, in sentence case, at 400 weight with 1.55 line height. No third typeface. Nothing below 12px. Body measure is 65–75 characters.
- Surfaces are Paper, then Plate (2px top and bottom borders), then Chrome (retro brown with cream text). No two adjacent sections share a ground.
- Googie card: 2px taupe border, 12px radius, and a hard `5px 5px 0` offset shadow in retro brown at 15–20%. On hover it moves 2px up and left and the shadow turns teal.
- No blurred shadows, no gradient headlines, no glass on content cards. The only glass is the sticky nav, in cream at 72% over a 12px blur. No pure white or cool grey. No emoji icons.
- Motifs: scanlines, a soft mustard starburst, atom rings, and Googie buttons (orange filled primary with a hard shadow, brown-outlined ghost). Eyebrows use the `★ LABEL · STATUS ★` format.
- Status vocabulary, one colour each: LIVE, BETA, COMING SOON. A held-back action is dimmed, unclickable and tagged COMING SOON.
- Voice: short, declarative, plain. Never invent statistics, customers, quotes, testimonials or download counts. Never use "bespoke". Headings, nav, buttons and labels are uppercase. The company is always written "Neato Ventures". The wordmark is `NEATO_VENTURES` with the underscore always in burnt orange.
- Respect `prefers-reduced-motion`. Slow motion only. The atom may rotate slowly.

## Product naming
The product is **Recordly**. Keep that name; don't rename it to Neato_Recordly. Neato Ventures is the publisher/distributor, shown with the NEATO_VENTURES wordmark (atom mark plus wordmark) in the nav and footer.

## Honest attribution (required, AGPL-3.0)
Recordly is open-source software created by webadderall and contributors (https://github.com/webadderallorg/Recordly), licensed under AGPL-3.0. This build is distributed by Neato Ventures. Its source code is at https://github.com/markhiltonapps/Recordly. The page must say this plainly, link both repos, and name the licence. Don't imply that Neato Ventures created Recordly.

## Facts: what Recordly does (use only these)
Recordly is a desktop screen recorder and editor for walkthroughs, demos and product videos. It adds zooms, cursor polish and styled backgrounds without a motion designer. It's free and open source.

**Recording**
- Record a whole display or a single app window.
- Capture microphone and system audio.
- Go straight from recording into the editor.
- On Windows: a native Windows Graphics Capture helper, plus native WASAPI audio.

**Timeline editing**
- Drag-and-drop timeline.
- Trim unwanted sections.
- Manual zoom regions, plus automatic zoom suggestions based on cursor activity.
- Speed-up and slow-down regions.
- Text, image and figure annotations.
- Extra audio regions.
- Crop the frame.
- Save and reopen `.recordly` project files with the editor state kept.

**Cursor**
- Show or hide the rendered cursor.
- Size, smoothing, motion blur, click bounce and sway.
- Loop mode for cleaner looping exports.
- macOS-style cursor assets.

**Webcam overlay**
- Webcam bubble, which can be mirrored.
- Size, preset positions or custom X/Y placement, margin, roundness and shadow.
- Optional scaling that reacts to zoom.

**Frame styling**
- Built-in wallpapers, custom uploaded backgrounds, solid colours and gradients.
- Padding, rounded corners, background blur and drop shadows.
- Aspect ratio presets.

**Export**
- MP4 and GIF.
- Quality selection.
- GIF frame rate, loop toggle and size presets.
- Output dimension controls.
- Reveal the exported file in the system file manager.

**Workflow**
- Customisable keyboard shortcuts with an in-app shortcut reference.

## Do NOT mention or promise
- Cloud share links, sign-in or accounts, in-app feedback submission. These don't work in this build.
- An extensions marketplace.
- Auto-update claims.
- Any user or download numbers.

## Downloads (current release 1.4.0)
Use these stable "latest" links:
- **Windows 10 (build 19041+) / 11, x64** — LIVE. https://github.com/markhiltonapps/Recordly/releases/latest/download/Recordly-windows-x64.exe (about 199 MB)
- **Linux x64, AppImage, modern distros** — LIVE. https://github.com/markhiltonapps/Recordly/releases/latest/download/Recordly-linux-x64.AppImage (about 224 MB)
- **macOS** — COMING SOON. Show it as a held-back action: dimmed, not a link, tagged COMING SOON in mustard.
- All releases and checksums: https://github.com/markhiltonapps/Recordly/releases

Install notes to show:
- **Windows:** the installer isn't code-signed yet, so SmartScreen may show "Windows protected your PC". Choose **More info → Run anyway**.
- **Linux:** make the file executable (`chmod +x Recordly-linux-x64.AppImage`), then run it. Hiding the cursor while recording isn't supported on Linux.

Nice to have: a tiny inline script that highlights the download matching the visitor's OS (Windows or Linux) and puts that OS's button first in the hero. The page must work fully without JS.

## Page structure (suggested; the designer may improve it)
1. Sticky glass nav: NEATO_VENTURES mark on the left; anchors for Features and Download.
2. Hero on Paper: eyebrow, short uppercase headline, lede, one orange primary download button (for the detected OS, defaulting to Windows) and a ghost button to see features. Then an inline-SVG/CSS illustration of the Recordly editor: a framed recording on a wallpaper, a cursor, and a timeline strip with labelled regions like `ZOOM 2.0×`, `TRIM`, `SPEED 1.5×` and monospace timecodes. Build it from subject details, not generic shapes.
3. Features on Plate: grouped data plates (Record, Edit, Cursor, Webcam, Frame, Export).
4. How it works: three real steps (Record → Edit → Export), numbered because it is a real sequence.
5. Download on Paper with the starburst: platform cards with status chips, file size, requirements and install notes.
6. Chrome footer: attribution, licence, source links, the NEATO_VENTURES wordmark, and `★ THE FUTURE IS NEATO ★`.

## Quality bar
- It passes the brand's test: "If a stranger saw one screen with the logo removed, would they still know it was us?"
- WCAG 2.2 AA contrast. Visible keyboard focus. Semantic landmarks and headings. Alt text for images. SVG illustrations have a title or `aria-hidden`. Links make sense out of context.
- No lorem ipsum. Every claim is traceable to the facts above.
