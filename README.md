<p align="center"><br>
<a href="https://github.com/Lolo280374/tetrmp3"><img src="https://hackatime-badge.hackclub.com/U09CBF0DS4F/TETR.MP3"></a>
<a href="https://makeapullrequest.com"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
<a href="https://devrant.com/rants/4149950/i-fucking-hate-mobile-development-i-already-manage-the-data-devops-infra-and-mos"><img src="https://img.shields.io/badge/you_need-a_keyboard-white"></a>
<a href="https://devrant.com/rants/4149950/i-fucking-hate-mobile-development-i-already-manage-the-data-devops-infra-and-mos"><img src="https://img.shields.io/badge/not_optimized-for_mobile-red"></a>
<br><p>

<h3 align="center">
play tetris, but twist: an audio file of your choice controls the game's speed! (with it's bpm)
</h3>

<h1 align="center">
showcase (screenshots)
</h1>

<img width="1633" height="998" alt="gameplay" src="https://github.com/user-attachments/assets/1017d94e-5d7b-46a6-8771-f5a66f21dbbe" />

<img width="1716" height="1165" alt="fileimport" src="https://github.com/user-attachments/assets/1d3311ff-1cd9-43cf-be2c-cd7bb91846c3" />

> [!NOTE]
> you might encounter long waiting times at the "analyzing song to detect its bpm..." part. please note that this only should take a few seconds on short songs, and that this depends of your computer's capabilities. however, if you are trying to import a big file, like a playlist for example (+5 min), the wait could be long, but should nowhere exceed somewhere like 1 minute. so yeah! use short songs! i guess...

## table of contents

- [about](#about)
- [supported file formats](#supported-file-formats)
- [how is BPM calculated](#how-is-bpm-calculated)
- [keybinds](#keybinds)
- [demo files](#demo-files)
- [contributing](#contributing)
- [reporting issues](#reporting-issues)
- [credits](#credits)
- [license](#license)

## about
for this week of siege, the theme was grid! so i decided let's go and make tetris, with a small twist!
the idea came from me that exact day playing TETR.IO, and realizing that i could just use tetris as a good game for the grid usage, and i got to work! i wanted to add a small twist, so I also added the fact that the game's speed changes with the BPM of the song, to make it like a difficulty level! sadly, it's often not that hard actually, but it's a good demo really!

in the end, this week, i'm actually happy of what i did, yay. and the UI is quite good when I think about it! simple and nice. plain dark mode. enough yapping i'm out byeeeeeeeeeeee

## supported file formats
the following file formats are supported when it comes to importing audio files. note that technically, you can import any format, but compatibility isn't guaranteed!
* Vorbis (OGG)
* Waveform Audio (WAV)
* Free Lossless Audio Codec (FLAC)
* Advanced Audio Coding (AAC)
* MP3/MPEG-1 or 2 Audio Layers (MP3)
* Apple/MPEG-4 Audio (M4A)

## how is BPM calculated
BPM calculation is not magic. it's math. i suck at maths, but that's all right. (also this implementation is truely not perfect, but it does the job...)

to calculate the BPM, we use a library called MusicTempo. that library is avalaible on the [NPM package manager](https://www.npmjs.com/package/music-tempo), and it honestly simplifies our lives heavily. so we grab the music, put it thru musicTempo, which will give us the BPM of the song, and then yea!

then, to convert that BPM onto actual game speed, we just do the math of "60000 / <the bpm>", and that will give us a conversion from "beats per minutes" to "milliseconds per beat", exactly what our code expects, so then we just slam that value into the code and boom, speed changes with the BPM!

i'm no math expert. sorry if that explanation sucks. you can check the code yourself.

## keybinds
the game has rather simple keybinds. if you already played TETR.IO, you'll feel yourself (almost like at home), considering i'm also a TETR.IO player and I decided to reuse the same keybinds.

* left/right/down arrows - moves the active shape on the grid
* up arrow - rotates the active shape on the grid
* spacebar - make the active shape instantly reach the bottom, going to the next shape essentially

## demo files
this was a nightmare. i had to find audio files to put in the game for the Siege demo, issue is a lot of the songs nowadays are obviously not copyright-free or royalty-free. i decided to use the following songs...

* The Nymphaeum Part V by Angelwing;

why: this is the default MikoPBX hold music, and it gave me memories so i thought hey that'd be funny.

* デイドリーム (Daydream) by RINZO and MAHIRU;

why: i wanted a J-Pop song, but most of them are obviously going thru licensers like Sony, so that was a pain, so i just decided okay let's go with NCS. easy.

## contributing
to contribute, you can simply git clone this repository, and start editing the main HTML file of this project (or the javascript):

```sh
git clone https://github.com/Lolo280374/tetrmp3.git
cd tetrmp3
```

you may then request your modifications via a PR.

## reporting issues
this is a community project, and your help is very much appreciated! if you notice anything wrong during your usage of this software, please report it to the [GitHub issues page](https://github.com/Lolo280374/tetrmp3/issues/)!

## credits
many thanks to these who without them, the project may have never seen the light of day (or it would just have sucked):

- [Lucide Icons](https://lucide.dev/) - once again, absolutely goated icon pack, just works and super easy to import. love using it.

- [MusicTempo](https://cdn.jsdelivr.net/npm/music-tempo/+esm) - used for calculating the BPM of each imported song, works pretty well!

- [the artists that did the demo songs, check home page](https://tetr.lolodotzip.tech/) - well i definitly needed songs for the demo of the game, and thanks for making your stuff copyright-free!!

- [JSfxr](https://sfxr.me/) - allowed me to make the sound effects by myself! super cool tool i had never heard of, but thanks!

and probably some others I forgotten.. sorry in advance, but thanks for being here!

## license
this project is licensed under the MIT License which you may check [here](https://github.com/Lolo280374/tetrmp3/blob/master/LICENSE/).
<br>if you have any questions about this project or inquieries, please reach me [at lolodotzip@hackclub.app](mailto:lolodotzip@hackclub.app).
