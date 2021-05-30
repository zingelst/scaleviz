# scaleviz
Shows chords and scales on a piano. I can't read music and don't much feel like learning, so being a bit more visual, seeing the keys of the notes in the scales/chords appealed to me, so I made this.

## How to use:
- Just load the `index.html` file up in a browser. Tested in Chrome, Firefox and MS Edge.

## Features:
- Select a root note and a scale and press "Scale!" - The keys in that scale will be emphasized. The root notes will be highlighted in yellow. Keys not in the scale will be grey
- Pressing "Play Scale!" will sound out the scale in a pretty pathetic set of tones.
- Selecting a root note and a Chord and pressing "Show Chord!" will show the keys of that chord highlit in red.
- Pressing "Play Chord!" will play the notes of the chord in a pretty pathetic set of tones.
- Pressing "Reset" will clear all highlighting.

## In the Future?:
- WebMIDI support - Maybe but I use Firefox and WebMIDI isn't supported. 
- Better tone engine - The basic sine wave WebAudio I use is _horrible_
- Highlight the notes of the scale as they're played
- Toggle to show the notes of the keys on the keys themselves.

### ALGORITHM:
- Start at the desired note on a 1-12 scale, mapping C=1, C#=2, D=3, D#=4 E=5 F=6 F#=7 G=8 G#=9 A=10 A#=11 B=12
- Add the steps of the scale mod 12 and wrap around till all steps are used
- Copy the resulting pattern of the 1-12 to as many octaves as desired

### Scales:
THE FORMULAS
Here’s a list of whole-half step scale formulas:
W = Whole step, H = Half step, WH = Whole and a half step (3 half steps or frets).

```
Major scale = W-W-H-W-W-W-H (2-2-1-2-2-2-1)
Natuaral Minor scale = W-H-W-W-H-W-W (2-1-2-2-1-2-2)
Minor pentatonic scale = WH-W-W-WH-W (3-2-2-3-2)
Blues scale = WH-W-H-H-WH-W (3-2-1-1-3-2)
Major pentatonic scale = W-W-WH-W-WH (2 2 3 2 3)
Harmonic Minor scale = W-H-W-W-H-WH-H (2-1-2-2-1-3-2)
Melodic Minor scale = W-H-W-W-W-W-H (2-1-2-2-2-2-1)

Ionian scale = W-W-H-W-W-W-H (2-2-1-2-2-2-1)
Dorian scale = W-H-W-W-W-H-W (2-1-2-2-2-1-2)
Phrygian scale = H-W-W-W-H-W-W (1,2,2,2,1,2,2)
Lydian scale = W-W-W-H-W-W-H (2,2,2,1,2,2,1)
Mixolydian scale = W-W-H-W-W-H-W (2,2,1,2,2,1,2)
Aeolian scale = W-H-W-W-H-W-W (2-1-2-2-1-2-2)
Locrian scale = H-W-W-H-W-W-W (1,2,2,1,2,2,2)
Whole tone scale = W-W-W-W-W-W (2-2-2-2-2-2)
Whole-Half Diminished = W-H-W-H-W-H-W-H (2-1-2-1-2-1-2-1)
Half-Whole Diminished = H-W-H-W-H-W-H-W (1-2-1-2-1-2-1-2)
```
