# OnTheGrid: what's new

The newest version is first.

## 0.2.0 (2026-10-22)

- **Save your work:** File ▸ Save keeps a song, its stems and all your changes (bar lines, tempo, sections, chords) in one `.otg` file, whether or not you've rendered it. Open it again later from File ▸ Open, Open Recent, or by double-clicking it: it opens instantly, just as you left it.
- **A File menu:** New, Open, Open Recent, Close, Save and Save As. Start another song without restarting OnTheGrid; it asks whether to save your changes first, and again when you quit.
- **A much smaller app:** the download is 160 MB instead of 420 MB, and OnTheGrid takes 270 MB on your Mac instead of 850 MB. It finds the same stems, beats and chords as before.
- **The same answer every time:** preparing the same song twice now gives exactly the same stems and bar lines.
- Splitting into stems shows how far along it is.
- Opening a recording you've prepared before starts from what OnTheGrid found; to keep your changes, save the song.

[Download](https://github.com/musicdemo/StudioTools/releases/download/onthegrid-v0.2.0/OnTheGrid-0.2.0.dmg)

## 0.1.6 (2026-10-21)

- **Update alerts:** when a new version of OnTheGrid is out, an alert appears in the toolbar. Click it to see what's new and download it.
- **Tempo:** playback always follows the tempo box, and the tempo the song was played at is shown above it; click it to go back. The menu next to the tempo counts the beats as found (–), in half time (½×) or in double time (2×).
- **Easier editing:** the Section, Bar and Chord lanes light up under the mouse; click anywhere in a bar to change it. Pop-ups close with ×, when the mouse leaves them, or with Esc.
- **Chords:** OnTheGrid finds the chords in every bar and the song's key. Fix any chord with a click; the chords go into the REAPER project, `song.json` and a new chords MIDI file.
- **Sections:** mark the song's Intro, Verse, Chorus and so on; they show as colored boxes under the overview and as regions in the REAPER project.
- The review ends at the song's last sound instead of showing trailing silence.

[Download](https://github.com/musicdemo/StudioTools/releases/download/onthegrid-v0.1.6/OnTheGrid-0.1.6.dmg)
