# TODO (in order of priority)
- [x] implement keyboard splitting
  - [x] code separately
  - [x] integrate into main code body
- [x] implement level 2
  - [x] design
  - [x] code separately
  - [x] integrate into main code body
- [x] implement level 3
  - [x] design
  - [x] code separately
  - [x] integrate into main code body
- [x] implement UI changes
  - [x] design
  - [x] implement
- [x] work on documentation ---- current priority
- [x] fix bugs --- current priority
- [ ] add pretty pictures to documentation
- [ ] playing in key with level 2-4
- [ ] user testing
- [ ] add relative minor to the key list in the 1 key 1 finger 1 chord section
- [ ] fix the bugs that are related to midi keyboard input
  - [ ] sustain lengths seem to be limited to when the keys are held down
    - [ ] possibly the sustain length might only apply to computer keyboard because of noteoff messages that get sent
  - [ ] note input is still a bit finicky in terms of detection


# Assistive Chord Trainer for Keyboard Instruments
This is a BSMT Capstone Project for Spring 2020. The purpose of this project is to design a keyboard learning utility that bridges the gap between learning to play single notes and learning to play chords on a keyboard instrument.

## Table of Contents
- [Contributors](#Contributors)
- [Suggested Use Scenario](#Suggested-Use-Scenario)
- [The Level System](#The-Level-System)
  - [1 Key 1 Finger 1 Chord](#1-Key-1-Finger-1-Chord)
  - [2 Finger Basic Chord Input](#2-Finger-Basic-Chord-Input)
  - [3 Finger Assisted Chord Input](#3-Finger-Assisted-Chord-Input)
  - [3 to 4 Finger Extended Assisted Chord Input](#3-to-4-Finger-Extended-Assisted-Chord-Input)

### Contributors
#### Alex Crellin

- Email: acrellin1195@gmail.com
- Status: Current 5th Year B.S. Music Technology @ Georgia Institute of Technology
- Hobbies: hiking, drumming, playing video games

#### Lyn Phan

- Email: phan@gatech.edu
- Status: Current 4th Year B.S. Music Technology @ Georgia Institute of Technology
- Hobbies: fixing motorcycles, repairing computers, playing video games
- Background: information technology, web development, indie game sound

### Suggested Use Scenario

placeholder

### The Level System

Each level in this system allows for increasing amounts of user interaction. This allows for a user to play the same song throughout all for levels, adding more and more fingers until they are able to play the song without any assistance.

#### 1 Key 1 Finger 1 Chord

*Basic Explanation*

The user can select a scale to play in. After that, any one finger input will either play the relevant chord for that note or a single note, depending on whether that note is in key.

*Technical Explanation*

This mode allows for the user to set a major key or relative minor key and play a single note from that scale. That note will be taken as the root of the chord. Two key appropriate third intervals will be stacked on that root to form a chord, resulting in a major, minor, or diminished chord depending on the root. Any notes played that are outside the selected key will be passed through without any chord being produced.

#### 2 Finger Basic Chord Input

*Basic Explanation*

The user can play any major or minor chord using two fingers. They should know what roots are from the previous level, so to play the same music they will have to use one more finger to play the third of the chord to trigger it.

*Technical Explanation*

This mode allows for the user to play a chord using two fingers on the root and middle third of the chord. This mode also unrestricts the key limitation and allows the user to play any chord in any key, but the user is limited in that they can only form major and minor chords. This allows for experimentation as the user can learn to finger the corresponding major and minor chords for each root note. The user can also build off of the previous level by playing the same chords as they did for songs, but this time actively choosing whether to play major or minor for that particular key. Any notes outside the accepted major or minor third over the selected root will not be played, resulting in only the root note being played.

#### 3 Finger Assisted Chord Input

*Basic Explanation*

Having learned how to play two notes in a chord, the user will now be required to find the note played by a third finger in the chord, the fifth.

*Technical Explanation*

This mode is identical to that of the previous level, but the fifth of the chord will no longer be filled in and must be played manually. This again forces a user to intuitively find where to place their third finger on the fifth of the chord. Any notes outside of the accepted inputs of major third, minor third, and major fifth will be filtered out.

#### 3 to 4 Finger Extended Assisted Chord Input

*Basic Explanation*

The user is now no longer limited to simple major and minor chords. They can now also add different tone qualities by adding or moving the fingers they currently use on the chords that they know. This is useful for exploring and trying out different sounds.

*Technical Explanation*

This mode builds on the previous level. In addition to forming major and minor chords, the user is allowed even more freedom in forming chords. This mode is mostly intended for exploration, as it additionally allows for sus2, sus4, min7, Maj7, and octave intervals to be formed over the root in addition to the major third, minor third, and major fifth. Any note outside of these possibilities will again be filtered out.
