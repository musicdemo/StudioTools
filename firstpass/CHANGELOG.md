# FirstPass: what's new

The newest version is first.

## 1.3.1 (2026-10-23)

- **Safer input levels:** tom tracks that are only hit in a few fills are now measured by their hits, not by the bleed between them. Before, such toms could be turned up by nearly 20 dB and clip. No track's input trim now takes its peaks above -6 dBFS; where that holds a track back, its fader makes up the difference, so the balance stays the same.
- **Drum panning:** the hi-hat, toms and cymbal mics are panned to where they sit in the overheads, so each hit comes from one place, with the hi-hat and toms a little wider. The toms keep their order from one side to the other.
- **Guitar panning:** two electric or two acoustic guitars are panned hard left and right; with more electric parts, the outer pair goes hard and the rest spread between.
- **Changing a track's role:** playback stops while FirstPass prepares the track again, then a window lists what it did (the bus it moved to, EQ, trim, compression and so on).

[Download](https://github.com/musicdemo/StudioTools/releases/download/firstpass-v1.3.1/FirstPass-1.3.1.dmg)

## 1.3.0 (2026-10-21)

The first public release of FirstPass: a reference mix from a folder of stems, in minutes.

- **Prepare a mix automatically:** FirstPass works out what each track is (kick, snare, bass, lead vocal…) and sets it up the way you'd start it yourself: polarity between related mics, input trim, high-pass, gate, EQ, compression, level and pan, with the reason for every decision shown on its strip.
- **Reverb:** a plate or room reverb return, with pre-delay and decay that follow the song's tempo and built-in ducking under the vocal.
- **Bounce:** trim the start and end, fade the tail or add a long fade-out, and save a 24-bit or 16-bit WAV or a 320 kbps MP3.
- **Export to REAPER:** the whole mix as a REAPER project, with the FirstPass plugins carrying the console's settings.
- **Export to Pro Tools** (2025.10 or later): FirstPass builds the session in Pro Tools, with a folder per bus, tracks in console order and coloured by bus, each track's trim, polarity and time alignment written into its audio, and the FirstPass mix and the reference on muted tracks to compare against.
- **Update alerts:** when a new version of FirstPass is out, an alert appears at the right of the toolbar. Click it to see what's new and download it. **FirstPass › Check for Updates…** checks right away.

[Download](https://github.com/musicdemo/StudioTools/releases/download/firstpass-v1.3.0/FirstPass-1.3.0.dmg)
