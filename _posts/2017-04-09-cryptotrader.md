---
layout: post
title:  "cryptotrader"
categories: blog projects
---

So this is my newest most developed project and I super hope it works out. What cryptotrader does effectively is look at the price of different cryptocurrencies over the period of an hour and decides whether to buy or sell them accordingly. It is based on the [Bitfinex](bitfinex.com) api and can trade any cryptocurrency they have on there platform (I havent tested this, im just pretty sure its true). Im super stoked for this because if it works out that means that I will have a way of passively making money to buy coffee and other drinks with occasionally, or as i say 'coffee money' (definition: not a lot of money but a $1-2 a day, enough to buy a coffee).

## Why

So for a while now I have been interested in Trading, on the market, with cryptocoins, precious metals, etc. but I never had a way to actually do this. With the market its so heavily regulated any api's are very difficult to use, with precious metals, thats mostly done in person from what I know, but with cryptocurrencies its different, its a more or less unregulated market, with a lot of opensource platforms which allows apis, official and unofficial to be build surrounding the platform. I choose Bitfinex because they used REST and JSON to get and send information which is cross language compatible, they have low trading fees, and a lot of documentation on the apis.

Anyway the reason I wanted to do this was because *I LOVE AUTOMATION*. I have come to terms with the fact that automation is a passion of mine. And having created a framework to trade I can now develop the program to trade based on other factors I can derive from a list of points such as a change over time percent and the general trend and trade based on that instead of only percent change per point in the last hour.

## You Want to Use it?

Yeah so while it is open source and you can use it if you want I would recommend against actually using it because it is still a work in progress and more than likely will lose you money instead of making it and *I am not responsible if you lose money* just be aware of that otherwise feel free to modify it and change it just give me credit or something. Im still figuring out the whole legal side of Github.

## Finally

This is my most developed program to date I think and while it is a work in progress and I need to test it to see if it actually makes money. I will update this if it makes me rich or if it loses everything. Im hoping for the former, would rather the latter not happen.

_Update: 8.4.17_

So it worked alright, made me a few cents here and there but I have decided to rewrite it in Go, a language I find much easier to work REST with as well as use in general. At run there were some glaring issues including the fact that it wouldn't always check if a trade went through and if it failed then it the program wouldn't register this. So theres a lot more work to be done.

I also had the idea that it might be possible to predict the price of bitcoin in the next few minutes based upon the current orderbook volume, so this is in the works. What cryptotrader has done in the past is just buy when its low and sell when its a certain percentage above the buying price, this was fine but not exactly a great method of trading. There are two methods of trading I am hoping write in soon

1. Percentage based trading but scaled down so i can trade a lot of money at smaller gains much quicker

2. Using the orderbook to determine the next buying or selling price so i can buy or sell accordingly

Out of these I feel like 2 is going to be more successful but I am not sure.

Gage Coprivnicar
