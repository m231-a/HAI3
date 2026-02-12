# Presentation Guide

## Using the HTML Presentation

### Opening the Presentation

1. **Double-click** `presentation.html` to open in your default browser
2. **OR** drag and drop `presentation.html` into any browser window
3. **OR** right-click → Open With → Chrome/Firefox/Safari/Edge

### Keyboard Controls

| Key | Action |
|-----|--------|
| `→` (Right Arrow) | Next slide |
| `←` (Left Arrow) | Previous slide |
| `Space` | Next slide |
| `N` | Toggle speaker notes |
| `F` | Toggle fullscreen |
| `Home` | Go to first slide |
| `End` | Go to last slide |

### During the Meeting

#### 1. **Before Screen Sharing**
- Open `presentation.html` in your browser
- Press `F` to enter fullscreen mode
- Test navigation with arrow keys
- Press `N` to check speaker notes are working

#### 2. **Start Screen Sharing**
- Share your browser window (not entire screen for cleaner look)
- Make sure presentation is visible
- You should see slide 1 (title slide)

#### 3. **During Presentation**
- Use `→` arrow key or `Space` to advance slides
- Press `N` to view speaker notes (notes appear at bottom)
  - **Notes are visible ONLY to you**, not to viewers
  - Press `N` again to hide notes
- Keep an eye on slide numbers (bottom right)

#### 4. **Timing Management**
- Slide 7-11 (Speaker slides): Stay 5 minutes each
- Use a separate timer or phone timer
- Give 1-minute warning to speakers

#### 5. **Navigation Tips**
- If you need to go back: `←` arrow key
- If you overshoot: `←` to go back
- To jump to specific slide: Click on slide number in corner

### Touch/Mobile Support

If presenting from a tablet:
- **Swipe left** → Next slide
- **Swipe right** → Previous slide

---

## Screen Sharing Tips

### For Zoom
1. Click "Share Screen"
2. Select your browser window
3. Enable "Share computer sound" (optional)
4. Click "Share"

### For Google Meet
1. Click "Present now"
2. Choose "A window"
3. Select your browser window

### For Microsoft Teams
1. Click "Share content"
2. Select "Window"
3. Choose your browser window

---

## Backup Options

### Option 1: Print to PDF
1. Open `presentation.html` in Chrome
2. Press `Ctrl+P` (Windows) or `Cmd+P` (Mac)
3. Select "Save as PDF"
4. Adjust settings:
   - Layout: Landscape
   - Pages: All
   - Scale: Fit to page
5. Save as `HAI3-Adopters-Presentation.pdf`

### Option 2: Export Screenshots
If you need static images:
1. Open presentation in browser
2. Press `F11` for fullscreen
3. Navigate to each slide
4. Press `PrtScn` (Windows) or `Cmd+Shift+4` (Mac)
5. Save each slide as image

### Option 3: PowerPoint Import
If someone needs PowerPoint format:
1. Create PDF (see Option 1)
2. Use online converter: pdf2pptx.com or similar
3. Or import PDF into PowerPoint:
   - Insert → Photo → Picture from File
   - Select all PDF pages

---

## Customization

### Changing Colors
Open `presentation.html` in a text editor and modify:

```css
/* Line 15: Background gradient */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Line 62: Heading color */
color: #667eea;
```

### Changing Fonts
Modify line 10:
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
```

### Adding/Removing Slides
1. Copy an existing slide block
2. Update `data-slide` number
3. Update slide number display
4. Add speaker notes to JavaScript `speakerNotes` object

---

## Troubleshooting

### Slides won't advance
- **Check:** Are you clicked inside the browser window?
- **Fix:** Click anywhere on the slide, then press arrow keys

### Fullscreen not working
- **Check:** Some browsers block fullscreen
- **Fix:** Click "Allow" if prompted, or use F11 for native fullscreen

### Speaker notes not showing
- **Check:** Did you press `N` key?
- **Fix:** Make sure cursor is in browser window, press `N`

### Presentation looks small
- **Check:** Browser zoom level
- **Fix:** Press `Ctrl+0` (Windows) or `Cmd+0` (Mac) to reset zoom

### Slides look different on another computer
- **Check:** Browser compatibility
- **Fix:** Use modern browsers (Chrome, Firefox, Safari, Edge)
  - Avoid Internet Explorer

---

## Presenter Checklist

### 1 Hour Before Meeting
- [ ] Open `presentation.html` in browser
- [ ] Test fullscreen mode (`F`)
- [ ] Test slide navigation (`→`, `←`)
- [ ] Test speaker notes (`N`)
- [ ] Have narrator script open in second window
- [ ] Test screen sharing setup
- [ ] Have timer ready for speakers

### 5 Minutes Before
- [ ] Browser open with presentation on slide 1
- [ ] Fullscreen mode enabled
- [ ] Speaker notes tested
- [ ] Narrator script visible on second monitor (or printed)
- [ ] Timer ready

### During Meeting
- [ ] Share browser window
- [ ] Advance slides with `→` or `Space`
- [ ] Press `N` to view speaker notes when needed
- [ ] Keep eye on slide numbers (bottom right)
- [ ] Give time warnings to speakers

---

## Quick Reference Card

Print this and keep it near your keyboard:

```
┌─────────────────────────────────────┐
│     HAI3 PRESENTATION CONTROLS      │
├─────────────────────────────────────┤
│  →  / Space    Next slide           │
│  ←             Previous slide        │
│  N             Toggle notes          │
│  F             Fullscreen            │
│  Home          First slide           │
│  End           Last slide            │
└─────────────────────────────────────┘

Slides: 16 total
Duration: 30 minutes
Speaker time: 5 min each (slides 7-11)
```

---

## Files Included

- `presentation.html` - Main presentation file (shareable)
- `NARRATOR_SCRIPT.md` - Detailed facilitation script
- `SLIDES.md` - Markdown version of slides
- `AGENDA.md` - Meeting agenda
- `PRE_MEETING_PREP.md` - Attendee prep guide

---

## Sharing the Presentation

### Via Email
Attach `presentation.html` - it's a single file, no dependencies needed.

### Via Cloud Storage
Upload to:
- Google Drive (share link)
- Dropbox (share link)
- OneDrive (share link)

### Via GitHub
Already in your repo at:
```
/docs/meetings/2026-02-12-hai3-adopters-feedback/presentation.html
```

---

## Tips for Success

✅ **DO:**
- Practice navigating before the meeting
- Keep narrator script open on second screen
- Use speaker notes for guidance
- Test screen sharing in advance
- Have backup PDF ready

❌ **DON'T:**
- Switch windows during presentation (stays in fullscreen)
- Navigate too fast (let attendees read slides)
- Forget to press `N` for speaker notes
- Present in a tiny window (use fullscreen)

---

## Need Help?

If something goes wrong during the meeting:
1. Press `Esc` to exit fullscreen
2. Refresh the page
3. Navigate back to your slide using arrow keys
4. Press `F` to re-enter fullscreen

The presentation is completely self-contained - no internet connection needed once the file is open.

---

**Good luck with your presentation! 🎉**
