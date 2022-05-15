---
layout: post
title:  "Audio On A Spiral"
categories: blog projects
---

Using Matlab to make spiral visualizations of audio files.

I love audio, audio manipulation, and analog audio formats. I've been collecting vinyl for many years now, and I am hoping to make a vinyl lathe this summer. Before I started this, I thought I'd try a much smaller project, plotting audio onto a spiral, similar to art projects I've seen in the past. By doing this I hoped to be able to figure out how I can use my Axidraw machine in conjunction with Matlab to create records I can play!

## The Process

The first thing I had to do was figure out how to plot a spiral, figuring the Archimedean spiral was easy to program, I opened up Matlab, created an array for the angle and a decreasing radius. This was then plotted, as seen below, which leads to a classic spiral.

```
plot(radius.*cos(angle), radius.*sin(angle))
```

Then by importing the audio, plotting it over time, and taking the magnitude, I added the magnitude of the audio at any given time to the radius of the spiral. After a bit of time debugging the code, and making things a little easier, I wrapped the whole thing in a function and made a Matlab App to visualize the spiral and the options easier!

## The App

I have never made a Matlab App before, but it is fairly easy! Matlab App GUI installed, I added the function, added sliders for variables and it all worked golden!

A few tests I did, came out interesting! First was playing an F and C chord on the OP-1 and importing that into the program to see what came out. You can see that the F-Chord is much less wavy then the C-Chord, which I believe is a result of the varying loudness that can be heard in the files which I linked below the images.

![F_Chord](https://raw.githubusercontent.com/Gageco/Audio-Spiral/main/Images/F-Chord.png){:width="50%"}

*F Chord*

[F Chord Audio](https://github.com/Gageco/Audio-Spiral/blob/main/Images/F-OP1.mp3)

![C_Chord](https://raw.githubusercontent.com/Gageco/Audio-Spiral/main/Images/C-Chord.png){:width="50%"}

*C Chord*

[C Chord Audio](https://github.com/Gageco/Audio-Spiral/blob/main/Images/C-OP1.mp3)

These were really neat looking, and I'm very happy about how they came out. Next I tried plotting a voicemail I got, which also ended up very nicely, so I decided to plot it using my Axidraw.

![Voicemail](https://raw.githubusercontent.com/Gageco/Audio-Spiral/main/Images/Voicemail.png){:width="50%"}

![Frame_01](https://coprivnicar.com/images/misc/Axidraw_Audio_Spiral.jpg){:width="50%"}


Really happy with all these results, and while I'm not sure there's much else I can do with these, but they were really fun and interesting to put together!

Gage Coprivnciar
