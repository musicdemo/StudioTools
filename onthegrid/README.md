# OnTheGrid

<img src="../assets/onthegrid-icon.png" width="96" align="right" alt="">

**Put a song recorded without a click onto a steady tempo.**

Songwriters often play a new song the way they're comfortable: no metronome, a few
passes back to back. That's a great performance, and a slow start for a production:
before you can add drums, bass or keys, every bar has to be lined up with a click by hand.

OnTheGrid does that part. Drop in the rough recording and it:

- **splits it into stems** (vocals, guitar, piano, drums, bass, other: whatever has real
  content in it),
- **finds the beat and the bar lines** from the instruments, holding the bar length steady
  so a strumming pattern or a held chord doesn't throw it off,
- **finds the chords** in every bar, and the key,
- lets you **check it by ear** and fix anything it got wrong, with a few clicks,
- and **renders the song and every stem onto a whole-number tempo**, with two bars of
  lead-in before the first downbeat.

Drop the files into your DAW at zero and they're on the grid.

[Download the latest version](https://github.com/musicdemo/StudioTools/releases?q=onthegrid&expanded=true) ·
[What's new](CHANGELOG.md)

**Needs** a Mac with Apple silicon (M1 or later) and about 500 MB of disk space.

---

## Contents

- [Installing](#installing)
- [Quick start](#quick-start)
- [Saving and opening songs](#saving-and-opening-songs)
- [Checking and fixing the timing](#checking-and-fixing-the-timing)
- [Tempo](#tempo)
- [Song sections](#song-sections)
- [Chords and key](#chords-and-key)
- [Rendering](#rendering)
- [What you get](#what-you-get)
- [Comping takes played without a click](#comping-takes-played-without-a-click)
- [Tips and troubleshooting](#tips-and-troubleshooting)
- [Video tutorials](#video-tutorials)

---

## Installing

1. Download `OnTheGrid-<version>.dmg` from the
   [latest release](https://github.com/musicdemo/StudioTools/releases?q=onthegrid&expanded=true).
2. Open it and drag **OnTheGrid** onto **Applications** (choose **Replace** when updating).
3. Open OnTheGrid from Applications.

The first time you open a song from your Documents folder, macOS asks whether OnTheGrid
may access it; choose **Allow**.

When a new version is out, an alert appears in OnTheGrid's toolbar: click it to see
what's new and download it.

## Quick start

1. **Drop a song** onto the window, or click **Choose a Song…**. WAV or MP3; a rough phone
   recording works, so do rehearsals and live takes.
2. OnTheGrid splits it, finds the beat and finds the chords, in about half a minute.
3. **Listen** with the click on (the metronome button). The high click should land on the
   one of every bar. Anything worth a closer listen is listed under **Worth a listen**.
4. Mark the song's sections and fix any chord or bar line you want to (all optional).
5. Click **Render**. The files go to `Music/OnTheGrid/<Song> (<tempo> BPM, <meter>)`, and
   **Show in Finder** takes you there.
6. To come back to the song later, **File ▸ Save** it.

## Saving and opening songs

**File ▸ Save** keeps everything about a song in one `.otg` file: the recording, its stems,
and every change you made (bar lines, tempo, meter, sections, chords, key), rendered or
not. A five-minute song's file is about 50–80 MB. Open it again with **File ▸ Open**,
**File ▸ Open Recent**, by double-clicking it in Finder, or by dropping it on the window:
it opens instantly, just as you left it. The file holds everything it needs, so you can
move it, back it up or send it to another Mac with OnTheGrid.

**File ▸ New** (or **Close**) goes back to the drop screen for the next song. If the song
that's open has changes you haven't saved, OnTheGrid asks whether to save them first, and
it asks again when you quit. The window's title shows **Edited** while there are unsaved
changes.

Opening the recording itself again (rather than its `.otg` file) starts from what
OnTheGrid found, without your changes; it's quick, because the stems are kept.

## Checking and fixing the timing

The review screen shows the whole song across the top (click to move around) and a
zoomed view below with three lanes over the waveform: **Section**, **Bar** and **Chord**.
Whatever is under the mouse lights up; click it to change it. Space plays and stops;
the arrow keys move a bar at a time.

- **A bar line in the wrong place:** click the beat in the waveform where the one really
  is and choose **The one is here**. The bar lines after it follow, and your mark shows in
  amber.
- **Worth a listen** flags the places to check: a bar with an extra or missing beat (a
  singer adding a beat is common, and is kept: the tempo map gives that bar its own time
  signature), a stretch where the beat was hard to hear, and bar lines placed by tempo
  where nothing clear was played. Click one to jump there and hear it.

## Tempo

- Playback always follows the **tempo box**: you hear the song stretched to that tempo,
  on a steady click, exactly as it will render. After a change it takes about a second.
- The tempo it was **played** at is shown above the box, in parentheses; click it to go
  back.
- Any whole-number tempo works: the bar lines stay where they are and only the stretch
  changes. Past about 25% faster or slower, the display turns amber as a reminder to
  listen for stretching artifacts.
- The menu next to the tempo counts the beats **as found** (–), in **half time** (½×) or in
  **double time** (2×), for songs that feel twice as slow or fast as the beat it found.

## Song sections

Click a bar in the **Section** or **Bar** lane and pick where a section starts: Intro,
Verse, Pre-Chorus, Chorus, Bridge, Instrumental and more (Verse 2, Refrain, Tag, Vamp…
under **More**). A section runs until the next one. The strip under the overview shows the
whole arrangement, and clicking a section jumps to it.

Sections go into the tempo map as markers, into the REAPER project as colored regions, and
into `song.json`.

## Chords and key

The **Chord** lane shows each bar's chord with its Nashville number (G 1, C 4, D/F# 5/7).
If one is wrong, click the bar and type the right chords:

- `G` or `Em` or `F#m`: one chord for the bar
- `C D`: a change halfway through the bar
- `C/E`: a slash chord
- `-`: no chord

Your corrections show in amber; **Back to what was found** undoes one. The **KEY** menu sets
the key the numbers count from: **Auto** uses the key found from the chords.

OnTheGrid finds major and minor chords, with a slash bass where the bass clearly plays the
third. Sevenths, suspended chords and pushes are yours to type in.

## Rendering

Click **Render** and choose:

- **Also make a REAPER project**: the stems on their own tracks at zero, the tempo and
  time signatures set, the sections as colored regions and the chords as markers.
- **Chord names in DAW markers**: letters (G, C/E) or numbers (1, 4/6).

## What you get

In `Music/OnTheGrid/<Song> (<tempo> BPM, <meter>)/`:

| File | What it is |
|---|---|
| `<Song> - full mix.wav` | the whole song on the grid |
| `<Song> - vocals.wav`, `- guitar.wav`, … | each stem with real content, on the grid, sample-aligned with the full mix |
| `<Song> - tempo map.mid` | the tempo, any odd bars' time signatures, and section markers: import it to set your DAW's grid |
| `<Song> - chords.mid` | the chords as block chords on one MIDI track: a scratch keys part |
| `<Song> - song.json` | every bar, its section and chords, for importing into other tools |
| `<Song>.rpp` | the REAPER project, if you asked for one |
| `<Song> - notes.txt` | the tempo, key, arrangement and anything worth a listen |

Every song starts with **two bars of lead-in** before the first downbeat.

## Comping takes played without a click

When an artist plays several passes back to back without a click, put each one through
OnTheGrid **at the same tempo**: note the first take's tempo and type it into the tempo box
for each of the others. Every take comes out on the same grid with the same two-bar
lead-in, so they stack in your DAW and you can comp between them.

## Tips and troubleshooting

- **The bar lines are a beat off for a stretch:** click the beat where the one really is
  and choose **The one is here**; the bars after it follow.
- **The song feels twice as fast or slow as the tempo shown:** pick ½× or 2× next to the
  tempo.
- **Very free endings** (a big ritardando, a long final chord) can't be put on a grid and
  may need a stretch marker or two by hand in your DAW.
- **Stretching artifacts** grow with the amount of stretch: a few percent is inaudible; a
  quarter or more is worth a careful listen.
- **The first song after installing** takes a little longer (about 15 seconds more) while
  macOS checks the app and OnTheGrid gets its models ready for your Mac.

## Video tutorials

*Coming soon.*
