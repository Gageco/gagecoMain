---
layout: post
title:  "Learning New Languages"
categories: blog personal
---

So with this new semester at Colorado School of Mines I have started taking my first official Programming Class, pretty exciting, it is in C++ which from the research I have done sounds more useful and practical than python because of more chances of optimization and better multithreading.

## Use

So with this new language it doesnt actually seem much different other python than a few syntax changes. So thats nice. I am thinking about recoding a few of my current projects in C++ namely EISA_2.0 because it seems like I could use the threading and optimization that C++ provides to make EISA work better and be better.

Another language I am looking to learn is Googles coding language 'Go'. I met a company at the Mines Career Fair called [Pivotal](https://pivotal.io) and while I am pretty good at coding already I havent had the opportunity to learn Go. So thats on my list to learn this summer. Also while I have had some experience with [Google Cloud Console](https://cloud.google.com/), I am not that great yet so I am going to get better at that as well.

It seemed to me at least that they were interested in me as a potential recruit next year over the summer when I am a Junior. Really looking forward to that, the seem like a cool company.

Update: So after some time messing with Go a bit I really like it, theres a lot of potential and some very interesting syntax. For example they have a statement that lets you essentially write a program backwards, so the last part executes at the beginning and the beginning execute at the end.  Heres an example:

````
defer fmt.Printf("World.")
defer fmt.Printf("Hello ")

>>> Hello World.
````

Yeah weird and you can also use it in things like for loops heres another example
````
for i < 6 {
  defer fmt.Printf(i)
  i+=1
}

>>>54321
````
I dont know the practical use of this yet but it has potential. Another interesting syntax choice on the behalf of the Go developers is to leave out while loops, and the like instead replacing all the loops with for loops. When first reading through some of the documentation on this a lot of people expressed a distaste for this calling it  a step backwards but I am actually liking it, it limits the actual logic you use but you are able to do much more with what you are given.

When deciding if i like a new coding language or not is if i can run it on my server over ssh. With C++ while i like the formatting of it in a general sense (the {} and the for loops), i really dont want to learn how to use make commands over ssh and having tried doing it before its just a huge pain. But with go all you have to do is a simple 'go run program.go' and it runs, its great! So with all of this said I am hoping to learn more Go through a project I found on Github called [go-bithue](https://github.com/realytcracker/go-bithue) which correlates Phillips Hue lights with the price of bitcoin. Should be interesting and as I gain more knowledge of Go I can more meaningfully contribute to this repo.

Lastly I would like to update this more about projects and ideas and other things that are happening.

Also im going to be a roboticist.
Gage Coprivnicar
