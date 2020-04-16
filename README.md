# Assistive Chord Trainer for Keyboard Instruments
This is a BSMT Capstone Project for Spring 2020. The purpose of this project is to design a keyboard learning utility that bridges the gap between learning to play single notes and learning to play chords on a keyboard instrument.

## Table of Contents
- [Introduction](#Introduction)
- [Contributors](#Contributors)
- [Suggested Use Scenario](#Suggested-Use-Scenario)
- [Diagram Notes](#Diagram-Notes)
- [The Level System](#The-Level-System)
  - [1 Key 1 Finger 1 Chord](#1-Key-1-Finger-1-Chord)
  - [2 Finger Basic Chord Input](#2-Finger-Basic-Chord-Input)
  - [3 Finger Assisted Chord Input](#3-Finger-Assisted-Chord-Input)
  - [3 to 4 Finger Extended Assisted Chord Input](#3-to-4-Finger-Extended-Assisted-Chord-Input)

### Introduction
This is the thing that I wanted when I was a high schooler learning piano. Sure I could play single notes and I could tell you what they were, but chords? Nope. I didn't know enough music theory to just "make" them. I could tell what major and minor were, but every single major and minor chord looked different to me. Why were there so many keys? Why weren't all the major chords the same shape?

This program is designed to help ease someone learning piano through that process. Learning chords is a pain. Learning to play three notes in time and changing your hand shapes to the beat is also a pain. Someone using this program would be able learn the chords to a song easily by starting with simplified chords and moving gradually up to full chords. My goal was for them to be able to play whatever song they wanted to learn the entire time. They can work on chord changes one finger at a time, instead of trying to do several at once.

-LP

### Contributors
#### Lyn Phan

- Email: phan@gatech.edu
- Status: Current 4th Year B.S. Music Technology @ Georgia Institute of Technology (as of Spring 2020)
- Hobbies: fixing motorcycles, repairing computers, playing video games
- Background: information technology, web development, indie game sound

#### Alex Crellin

- Email: acrellin1195@gmail.com
- Status: Current 5th Year B.S. Music Technology @ Georgia Institute of Technology
- Hobbies: hiking, drumming, playing video games


### Suggested Use Scenario

A suggested use scenario of this program is to use it as an assistive tool for learning to finger the chords of a song. This use case expects a user to already be able to play single notes and identify notes on a piano keyboard. The user is also expected to know the basics about major and minor chords, though not necessarily be able to form them.

A typical web search for the chords of a song will provide lyrics and associated chords. The user can use the chord progression to play along as they sing or with the original song.

The levels allow the user to play the chords of the song at an increasing complexity each time. This allows the user to first focusing on playing the root of each chord, then the root and third, and finally all three notes. After that they can play on the fourth level which allows for even more variations on chord qualities.

### Diagram Notes

The diagrams for each level will be shown using keyboard diagrams like this. Notes performed by the user in these examples are represented by the blue dots. Green dots represent anything output automatically by the chord trainer. Red dots represent an incorrect input from the user. Written information will be added next to each diagram to provide context to supplement the diagram. Yellow represents a note that belongs to the chord but was not provided by the user or filled in automatically by the chord trainer.

Here is a blank keyboard diagram.

![Blank Piano Keyboard Diagram](/Assets/Pictures/blank_piano_keyboard.png?raw=true "Blank Piano Keyboard Diagram")

Here is an example of a keyboard diagram. This example represents a user who has played a C. We can also see that they played the note D above that C, but it was not available to be played in the selected mode and was red. The two green notes added by this program were the E and G above the C. From this information we can gather that the chord trainer was set to Level 1, where only one input is required and the chord trainer fills in the rest.

![Example 1](/Assets/Pictures/example_diagram.png?raw=true "Blank Piano Keyboard Diagram")

In the example below the user does the exact same thing as the previous example, except the mode is set to Level 4, since the notes of the chord are yellow, indicating that they were not filled in by the chord trainer.

![Example 2](/Assets/Pictures/example_diagram_2.png?raw=true "Blank Piano Keyboard Diagram")

### Using Without a MIDI Keyboard

Press the key with the tilda on it to activate computer keyboard mode. A symbol labeled as such on the interface will light up indicating if this mode is active. See the diagram below for computer to piano keyboard mappings. It is not indicated on the diagram, but the range available is C4 to G5.

![Computer Keyboard Diagram](/Assets/Pictures/keyboard_diagram.png?raw=true "Computer Keyboard Diagram")

### The Level System

Each level in this system allows for increasing amounts of user interaction. This allows for a user to play the same song throughout all for levels, adding more and more fingers until they are able to play the song without any assistance.

#### 1 Key 1 Finger 1 Chord

*Basic Explanation*

The user can select a scale to play in. After that, any one finger input will either play the relevant chord for that note or a single note, depending on whether that note is in key.

*Technical Explanation*

This mode allows for the user to set a major key or relative minor key and play a single note from that scale. That note will be taken as the root of the chord. Two key appropriate third intervals will be stacked on that root to form a chord, resulting in a major, minor, or diminished chord depending on the root. Any notes played that are outside the selected key will be passed through without any chord being produced.

*Visual Examples*

In the below example, the key has been set to A Major. Playing an F# in the key of A Major results in an F# minor chord.

![A Major Chord in Level 1](/Assets/Pictures/level_1_1.png?raw=true "Blank Piano Keyboard Diagram")

If the user plays multiple notes, then the leftmost note will be taken as the root of the chord. Notes not in the associated chord will be ignored and notes part of the associated chord that are not the root will continue to play.

In the example below, the key is set to G Major, and the user places their palm over multiple keys. The leftmost not that is played is a D, so the chord trainer uses D as the root of the chord. Every note they play between D and G is pressed by their palm but only the F# plays because it is part of the D Major chord that is formed.

![Hand Press Example in Level 1](/Assets/Pictures/level_1_2.png?raw=true "Blank Piano Keyboard Diagram")

#### 2 Finger Basic Chord Input

*Basic Explanation*

The user can play any major or minor chord using two fingers. They should know what roots are from the previous level, so to play the same music they will have to use one more finger to play the third of the chord to trigger it.

*Technical Explanation*

This mode allows for the user to play a chord using two fingers on the root and middle third of the chord. This mode also unrestricts the key limitation and allows the user to play any chord in any key, but the user is limited in that they can only form major and minor chords. This allows for experimentation as the user can learn to finger the corresponding major and minor chords for each root note. The user can also build off of the previous level by playing the same chords as they did for songs, but this time actively choosing whether to play major or minor for that particular key. Any notes outside the accepted major or minor third over the selected root will not be played, resulting in only the root note being played.

*Visual Examples*

In this first example the user plays a B Major chord. The fifth of the chord, F#, is filled in by the chord trainer.

![B Major](/Assets/Pictures/level_2_1.png?raw=true "Blank Piano Keyboard Diagram")

The user is also able to play a minor B chord, by playing D natural, which is a minor third above the root B, shown below.

![B minor](/Assets/Pictures/level_2_2.png?raw=true "Blank Piano Keyboard Diagram")

If the user plays a not that is not the major or minor third, then that note simply won't play. The fifth will still be filled in by the chord trainer since that is based off of the root, shown below.

![B "power chord"](/Assets/Pictures/level_2_3.png?raw=true "Blank Piano Keyboard Diagram")

#### 3 Finger Assisted Chord Input

*Basic Explanation*

Having learned how to play two notes in a chord, the user will now be required to find the note played by a third finger in the chord, the fifth.

*Technical Explanation*

This mode is identical to that of the previous level, but the fifth of the chord will no longer be filled in and must be played manually. This again forces a user to intuitively find where to place their third finger on the fifth of the chord. Any notes outside of the accepted inputs of major third, minor third, and major fifth will be filtered out.

*Visual Examples*

The A minor chord seen below requires all three fingers to be played.

![A minor](/Assets/Pictures/level_3_1.png?raw=true "Blank Piano Keyboard Diagram")

If the fifth is not input by the user, then it will not be played.

![A minor without fifth](/Assets/Pictures/level_3_2.png?raw=true "Blank Piano Keyboard Diagram")

In this example the user plays the root and the fourth above the root, resulting in only the root of the A minor to play.

![A minor attempt with fourth](/Assets/Pictures/level_3_3.png?raw=true "Blank Piano Keyboard Diagram")


#### 3 to 4 Finger Extended Assisted Chord Input

*Basic Explanation*

The user is now no longer limited to simple major and minor chords. They can now also add different tone qualities by adding or moving the fingers they currently use on the chords that they know. This is useful for exploring and trying out different sounds.

*Technical Explanation*

This mode builds on the previous level. In addition to forming major and minor chords, the user is allowed even more freedom in forming chords. This mode is mostly intended for exploration, as it additionally allows for sus2, sus4, min7, Maj7, and octave intervals to be formed over the root in addition to the major third, minor third, and major fifth. Any note outside of these possibilities will again be filtered out.

*Visual Examples*

More advanced chords can be built, such as a Csus2-7 (read as C suspended 2nd minor 7th).

![Csus2-7](/Assets/Pictures/level_4_1.png?raw=true "Blank Piano Keyboard Diagram")

Some notes are still restricted, such as the tritone and sixth, since those are not as musically useful for root position chords.

![F# and A are not valid for a a C root, but E is](/Assets/Pictures/level_4_2.png?raw=true "Blank Piano Keyboard Diagram")

The diagram below shows which notes are valid with a C root note. The C an octave above the chord is also an allowed input.

![Valid notes for a C root note](/Assets/Pictures/level_4_3.png?raw=true "Blank Piano Keyboard Diagram")
