---
layout: post
title:  "ECCO Internship"
categories: blog personal
---

## ECCO Internship

[ECCO Safety Group](http://www.eccosafetygroup.com/) (ESG) is a global company that designs and manufactures safety equipment for a large array of vehicles, the core business of the company is manufacturing and exporting Backup Alarms and Light Bars. They are based out of Boise Idaho (conveniently enough where I live) but have bases everywhere from the UK to Australia.

## Background

I have been aware of the company for a while now, the old CEO's son went to the same High School as me. I had a class called 'Design Technology' the purpose of which was to give the students an idea of what the design process from start to finished looked like and one day the teacher invited the ECCO CEO in to talk to us, he came in a lot because his son went there and there company donated a lot of design equipment to our school. So I had connections to the company, knew what they did, knew the CEO and his son, and was just starting to learn Python.

So fast forward to Thanksgiving, I am at my Grandmothers and we were at the dinner table and her neighbor is over, we get to talking and he tells me he works for ECCO, I tell him I know of the company and I am going to Colorado School of Mines. Then after dinner he tells me if I am interested he is willing to hand out my resume to the people at the company. I take him up on his offer and a week or two later I give him a resume and forget about it for a while.

Few months later I get an email from the Head of Engineers and we start emailing back and forth, sounds like they dont exactly have the funds for a whole internship program but he is talking to his bosses about what they can do. So we are talking on the phone a bit and I am calling him once a week or so and during one of these calls its comes up that I am a programmer and that I am alright for my age. So he takes this and turns around a week later saying i'm in, i've got the internship!! So yeah thank you to everyone so much for helping me in getting this amazing opportunity!

## What I Do

So the internship has lasted from May to August and in this time I have been working on a testing fixture to test the lights they putting into there light bars. Initially there was a huge learning curve of having to learn about CAN Communication, a standardized protocol used on vehicles to communicate between the different electronics, Arduino flavored C, and how to work in a business professional environment.

On the test fixture project I was working with another intern in the St Louis office of ECCO, we had communicated largely over slack, and around once a day we had a standup meeting over teleconference. This whole thing was totally new to me and I enjoyed learning the in's and out's of an office environment and the way all the different people worked together to make a product. I worked closely with one of the electrical engineers here on the project and he was very helpful in explaining the basics of CAN Communication and how it worked in conjunction with the firmware he was writing for the lights himself.

At the start of the project I thought that it was going to be much easier than it turned out being. First issue we ran into is that when sending a CAN message it is formatted like so

```
canData = {0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07}
{0x3F123FD, 0x01, 0x01, 0x08, canData}
//canID, extendedID, rtrBit, Data length, Data
```

I dont need to go into detail about what those all do you just need to know that the rtrBit is what signals to the receiver that the sender is expecting a message back. Well the [CAN Arduino Library](https://github.com/Seeed-Studio/CAN_BUS_Shield) we used to send the CAN Message to the lights was written that it had the rtrBit, but it wouldn't send it. So as the first real test of my programming knowledge I had to read through the library code itself and figure out why the rtrBit wasn't sending. This took a few days as I had never had to really dive into someone elses code and it was an incredibly valuable but tiresome experience. In the end the rtrBit wasn't being sent all the way through the different functions that should have been accepting them so while it was sent, it was always sent as 0x00, instead of 0x01. I had to rewrite the library and do a pull request that can be seen [here](https://github.com/Seeed-Studio/CAN_BUS_Shield/pull/46). Pretty proud of myself for that. After that every week or so the other intern and I would overcome some big problem and think "Hey we are probably going to be done next week!", but then the next week would come and we would run into another big problem we would have to overcome. This whole process lasted for about a month and a half till we both mutually realized we had no idea what problem we would run into the next week.

It was an amazing internship opportunity that I am hoping to do again in the future! The people were great and I really appreicate all those who helped me before, during and after the internship!

Gage Coprivnicar
