---
layout: post
title:      "A portfolio tracker for cryptocurrencies"
date:       2018-01-24 18:20:47 +0000
permalink:  a_portfolio_tracker_for_cryptocurrencies
---


### an easy way to know how much money is worthed your investments

I first heard about Bitcoin in 2011 during a discussion with a bunch of friends studying finance as me.
For the following years, I've never touched or thought about buying bitcoins or other coins until I came across another discussion, similar set up (a bunch of friends sitting at one table) but different location, US instead of Italy.
This time I did my research. 

Problems:
I was surprised by the lack of information, the 'greyness' of the market and the absence of old school financial-statistical tools and analysis as a Markowitz  portfolio optimization. After all, I was a student in finance once.
I've started to buy some coins with a tiny amount of money, mostly as trading experiments. I ended up creating another old school tool, an Excel spreadsheet with my different positions and the trades that I had. I've bought some coins and sold others across the time but still I had another issue.
The fluctuation of the cryptocurrencies is well-know. In a day a coin can lose 20% of its value while gaining back its price one day later: it's a rollercoaster. Having the current value of multiple coins (i.e. a portfolio) can be a nightmare, since you have to daily get by hand the price of each coin, multiply the dollar value of each coin for your quantity and lastly sum all this up. 

User research:
Before jumping into the project, I’ve borrowed my skills and experience as human-centered researcher to study and extracts some hints from real users cases. I’ve reached out to some friends investing in alt-coins asking about their routines with these investments to create a study sample.
I was impressed by how many times they check per day how the market is going. Secondly, some of them they have similar spreadsheets as mine with some heirarical others. First the total value of the investments, secondly, other spreadsheets with each coin position and trading booksheets. Others they simply compound the gain or loss on the flight. They interest 

Moreover I am interested (as the majority of investors) firstly in the total value of the portfolio and its gain, secondly in a detailed analysis/price trends for each coin. Even if I am fan of data, I was looking for something incredibly simple.
In other words: a tool that tells me clearly and firstly how much money is worthed my investment. Nothing more. Clarity and semplicity before a Pandora's box of charts opens up.

Solutions:
First of all, I need an automated solution to get data, mainly coin prices. Coinmarketcap.com is probably the best source, thanks to his omnicomprensive listing of alt-coins and their corrispective information.
Using Nokogiri, a beatiful Ruby gem, I was able to extract the price for each coin. But it wasn't enough.
New coins come out pretty quickly, only 2017 there were 235 new ICO (source: coinschedule). I also needed to constantly get these new coin names with its prices. After creating a simple login/signup page, using the findings from the user research, I’ve built a main page where all the fundamental actions take place. On top the current total value of the portfolio, below what compose the portfolio and a immediate call to action to add a coin and its quantity to the portfolio. In this way, you can add or remove coins without going on another page. The information for each coins (like its price, value in bitcoin and so forth) are reduced to two: price and quantity.
However, you can still visit a single coin page and perform similar action while seeing more information.
