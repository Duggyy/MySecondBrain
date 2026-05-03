---
title: "OpenAI Codex The Best for AI Trading Strategies? (watch ASAP)"
source: "https://www.youtube.com/watch?v=lcCaIHqeVBA"
author:
  - "[[Michael Automates]]"
published: 2026-03-27
created: 2026-05-03
description: "OpenAI's Codex AI (GPT-5.4) is Cheaper and Faster when Creating and Improving TradingView Strategies in PineScript. Must watch if you don't want to stay behi..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=lcCaIHqeVBA)

## Transcript

### Intro

**0:00** · That's right, guys. OpenAI's Codeex can now create trading strategies for us much faster and cheaper than before. We can stop paying Claude 100 bucks a month and we can go over to Codeex and pay nothing, the free plan, right? And get to the same results. Check this out. I gave it the bull market support band indicator and asked it to create a trading strategy out of it. And this is what I got. But I didn't stop there. I gave the AI the next prompt to improve the strategy further while avoiding overfitting. The AI went to work and this is the result.

**0:31** · Even better performance. It went from 780% profit to 2,800% profit. To achieve that, it went through roughly 250 strategy variants. How long would you have taken to do the same? And making use of the back testing engine, it knows exactly how to avoid overfitting by using insample, out of sample, and as well how to do crossm market validation before it gives me a new strategy version. Amazing, right?

**0:59** · And it's so easy to use. You don't need coding skills. And in this video, I'm going to teach you everything you need to know to achieve the same results as I have. You get access to the prompts to the back testing engine. And with this video, you have the tutorial on how to apply all of this for yourself. This method works on crypto, stocks, and commodities. Anything that has a chart.

**1:19** · In times like these guys, when crypto is crashing, you need a system to get you out, but also one to get you back in when the next bull market starts. Here on my channel, we're using the autotrading system. And that system got us out of Bitcoin here at 111,000, got us out of Ethereum at around 3,800, and got us out of Solana at around 220 bucks. And that is why this video is so relevant. so you learn how to build trading strategies for yourself and only when needed consider the auto trading masterass. Let's get started.

**1:49** · And guys, make sure to like this video if it adds value to you because otherwise the YouTube algorithm will never know and also you're supporting this channel.

### Disclaimer

**2:00** · Also remember this is not financial advice. Crypto is risky. You can lose all of your money guys and that is why I run this educational channel so that you are always ahead of the herd. Subscribe and let's go. Those are the three things guys that you need to make all of this work. Trading View, OpenAI Codeex, and also the back testing engine. We're going to go through all of these and I'm going to show you how to combine them together. Now, first of all, why do you need Trading View?

### Getting started

**2:24** · It's because I want you guys to put the strategy on your chart to see every single trade it took, to see the back test, and to have all the numbers, even more KPIs, right, given to you by Trading View. And this gives you the confidence that the back test was done correctly. Another benefit of having the strategy in trading view is that you can automate it on your exchange. And that means that every single trade that your strategy takes can be sent through signum to your exchange. You can even use multiple exchanges at the same time. And that's exactly how I automate my entire portfolio as well. More on that later.

**2:57** · Then of course you need the AI to run the back test and come up with new ideas on how to improve your trading strategy.

**3:04** · But then also you need the back testing engine to make sure that it doesn't do mistakes. It doesn't look into the future. It doesn't do overfitting. It knows exactly how to convert from trading view into what the AI needs and also back. And that's why the back testing engine is the foundation for what I'm showing you here. And because the back testing engine can convert to trading view and back, you can take a strategy that you already have and give it to the AI and it will use the engine to improve your existing strategy. But you can also take an indicator and give it to the AI.

**3:36** · And again with the back testing engine, the AI will know how to use that indicator to build a new strategy on top of it or as well you can combine multiple indicators to one better strategy. But all of that needs to be done basically by the AI using the knowledge from the engine so that it can convert back and forth between trading view and what the AI needs to run the back test and do its checks. The links to all of these tools will be down in the video description.

**4:02** · And in case you're asking yourself which plan to use for trading view, I think the plus plan is the best value because it allows you to do chart data export and as well strategy data exports. But you can start with a free plan and simply upgrade only when required. And for OpenAI also the plus plan I think is the best value. But again, you can easily start with the free plan. They even mention that on their website. For most people, the free plan will be more than enough to do what I'm showing you in this video.

**4:30** · Let's start building trading strategies with AI, guys. And the first thing you need to do is to go to the Codeex website.

### Convert Indicator to Strategy with AI

**4:38** · Click to download the app. Open it. Log in. And yes, this also exists for Windows. And once you're logged in, this is what you will see. Make sure to click on new thread. And then click here to pick a folder where you want to work in.

**4:51** · And that's important because in that folder, you will also have the back testing engine, which I will show you later on how to get access to. It's a zip file. So my folder is called Codex demo trading strategies. It's any folder on your computer and also you place the back testing engine inside of it and then you open that folder. Now the AI knows exactly in which folder to work and it will find the back testing engine in there. But you might have noticed I did not unpack the zip. I definitely have to do that.

**5:19** · And now the engine will find all the files it needs. for example, the chart data that it works with, the back testing engine logic here, and also the example strategy to work with. All the strategies that it produces will be placed into the strategies folder. And by the way, to make it easier for myself, I will sort this by date modified. And the reason is simply because the latest strategies will be on top. You'll see why that's practical very soon.

**5:47** · To replicate what I've shown you in the introduction, go to trading view, click on indicators, and then search for bull market support band, and then put this one on your chart from ZKdev. And this is what you will see. And also, by the way, I'm on the Bitcoin USD 1day index chart. To get to the same chart, click here and then search for Bitcoin USD and then pick the index chart from Trading View themselves. This is the best chart for Bitcoin.

**6:18** · So, as you can see, it doesn't have any back test because it's just an indicator, right? And indicators don't give you KPIs to work with. That's why I don't like indicators without having them turned into strategies first to see the performance. So, let's do that next.

**6:34** · That's the first task I did myself. And to do that, go here with your mouse and click on these brackets to reveal the source code of the indicator. This is the source code. Quite simple. Copy the whole thing. and I want you to place it inside of the strategies folder so that the AI can see it. So, open a text editor. Just paste it in there and name it bull market support band indicator.pine.

**6:58** · Save it. And now head over to the prompt document that is linked down in the video description and copy the prompt to convert an indicator to a strategy. And as you can see, we have to replace the name of the file here. It's very simple.

**7:11** · So, copy this whole thing. Go to your codeex app, paste it in there, and make sure to replace this file name here with our file name that we have just saved.

**7:20** · And then make sure to select the right AI model. I'm working with GPT 5.4, the latest one. And also, I've set it to high. And I figured this out by a lot of testing. Just click on high and then send the prompt. And now the eye will do its work. And I will come back to you once it's done.

**7:41** · All right. The AI came up with a strategy version of this indicator. Now, let's go to the folder and check it out in the folder. As you can see, it's on the top because we sorted by date modified. Very practical. Now, double click it to open it up. Copy the code.

**7:57** · Go to trading view and click on this pine icon to open the pine editor and then click here and create new strategy and simply delete everything that is in there and paste the new code and click on the save icon. Just click save and then click add to chart. And tada, we have our converted indicator now as a strategy. And funny enough, it's even better than what I got in my first try.

**8:23** · And the reason is simply that the AI decided to use different entry and exit signals than it did in my version. And that's normal because I didn't tell it when to buy and when to sell. I just left it to the AI to make the decision.

**8:37** · And that is also a good thing because it means that you can experiment with many different ideas. You can even ask the AI to do that. And this is how you can get to amazing trading strategies just by letting the AI experiment. Of course, of course, guys, I already see the comments.

**8:52** · This is overfitting.

**8:53** · Well, no, right? Because the engine knows to avoid exactly that problem. And that is why the engine comes with 10 different assets on different time frames so that it can do cross market validation. There you go, guys. That's just the first step, guys. Now, let's go to the most exciting part of this, which is to take a trading strategy and improve it. We're going to take this one and we're going to ask the AI to stick to all the rules, right?

### Improve Strategy with AI

**9:17** · To all the best practices that it has baked in and to come up with a better trading strategy for us to go through hundreds of variations and do all the work while we sip our coffee. Let's see if the AI can even improve this strategy in the next round because the first conversion was already that good. Now go back to the prompts document and copy the improve strategy prompt and as you can see again we need to change the file name over here.

**9:44** · But first copy the entire thing go to the AI paste it in there and then copy the file name of the strategy it has just created. For me it's called bull market support band strategy version 1.pine. And here I will simply replace this file name with this new file name. And also keep in mind that if I release a new version of the engine, you might have to update this as well.

**10:06** · And that would be this folder name over here. You can just copy it and paste it in here in case it has changed. The AI is ready. Now let's send the prompt and have AI do all the work. And remember that this part here tells the AI to do in-n-out sampling and as well crossmarket validation to avoid typical overfitting. Again, I will come back to you when this is finished. All right, guys. The AI finished the job. This is version two of the strategy. Let's check it out in our folder. This is the strategy on the top. Double click it.

**10:38** · Copy the code. Go to trading view and create a new strategy here. Create new strategy. Paste it in there. Save it.

**10:46** · and then add it to the chart and taa it has better numbers than the previous one which is very nice. Let's check out the KPIs,963% net profit with even lower draw down than the previous version and more trades which makes it statistically more relevant. For reference the first version was,545% net profit with 22.67 max draw down and 23 trades.

**11:10** · In case you're asking yourself what about the version I've seen in the introduction of this video and yes it had a higher P&L but then also it had double the draw down. If we take the version that we created together and we multiply it by two because let's say we do 2x leverage then also we arrive at 40% draw down but the profit is way higher at 3,900%.

**11:39** · That is why it's so important to have a low draw down because it allows you to leverage to get to higher profits while keeping the risk low. This is what I'm talking about, guys. AI did all the work. And what I wonder is how many variations did it actually test to get to this result? Let's go and ask the AI.

**11:58** · Holy moly, guys. 6,713 variants, which is a huge amount. And you know what the best thing is? that I can be sure that this is the best variant is because the AI is able to back test exactly the same as Trading View does. So when I look at the numbers, those are exactly the same KPIs as the AI showing me here. And that means that this is the best variant of the strategy with the data the AI has access to.

**12:24** · Yes, I have a little bit better version from the point of view of profit I showed you in the introduction, but then my max draw down is 41%. That's not better. Okay, like if you do the ratio, this one is actually better that we created together. Now, you can improve the strategy further, which again brings me back to my point why it's so important to put the strategy on your trading view chart because on

**12:49** · trading view, you can see every single trade the strategy took and you can find out where it made mistakes and as well you can use indicators from the Trading View community. You can add them on top of your strategy and you can find out if combining them might help. Okay, you don't have to do it yourself, but what you can do is you can take the code of any indicator that you have access to in Trading View and you can give it to the AI and the AI can then take that combine it with your strategy to find an even better strategy.

**13:20** · In the prompts document, you have exactly the prompt for that where it says to take this second version of the pine script strategy and then adding this indicator to it so that it can improve the entries and exits. I'm not telling the AI exactly how to use it. Of course, you can, but I want the eye to figure it out, right? And of course, you need to create this file in your folder. And for that, you simply copy the code of the indicator. You paste it in a text editor and save it. I will call it super trend indicator.pine.

**13:51** · As you can see, it appears here. And when I give it this prompt, it will know exactly what to do.

**13:57** · But of course, I need to change the name of the strategy that I want to improve.

**14:01** · And in my case, it will be this strategy over here. So, in my case, my prompt will look like this. I don't want to make this video super long, and that's why I'm not going to run this prompt because anyway, you just give it to the AI, and you will see what happens. The most important one was the one I showed you before where you take a strategy and you let the AI iterate to find better versions while of course avoiding all the mistakes that otherwise people make.

**14:26** · It knows how to avoid these mistakes because I told it when I created the back testing engine. Now, how do you get access to this back testing engine that makes all this magic happen? Well, it is a onetime purchase of 99 bucks. Sorry guys, that's not for free because it's way too good to give it for free. And by the way, this is teachable.com. Somehow they have issues loading the product picture. Sorry for that. I'm already talking to the tech team. This is how it's supposed to look like. The page works fine. It's just the image that is missing. Here you're getting access to everything that you need. The source code of the back testing engine.

### Access to AI Backtesting Engine

**14:57** · You can do all the good stuff that I showed you in this video and more because you have the source code. And that means that if you have an idea on adding features to this, you can just do that, right? You don't need to wait for me. And that's why this is such a gamecher because it already comes with everything you need and you can add more to it by asking the AI to code it for you. So there is no way around this. This is the number one way to create trading strategies with AI in 2026.

**15:23** · And once you have your trading strategies, the best practice is to automate them with Signnum because the easiest way to do it. So keep in mind that this is the next step. First you create a strategy, then you automate a strategy so you have the best execution possible. No emotions. It will just happen no matter if you're sleeping, traveling, on vacation or whatever have you. This will work on tons of exchanges. This is a full list of exchanges that we support and even hyperlquid if you want to automate on chain from your wallet.

### SIGNUM Strategy Automation

**15:54** · In case you need more chart data for different coins, then simply use this prompt and adapt it to what you need. And then the AI will go ahead and it will maybe ask you a question to allow it to do something.

### Fetch chart data (crypto, stocks)

**16:06** · Just allow it and it will go ahead and use the logic it has baked in to fetch chart data from exchanges. Just make sure to read what it's asking you. You have to approve something sometimes and then it will do its job properly and will place the files into the data folder when it's done. And as you can see, this is the tower data for one day, for one week, and also for the 4 hour, depending on the coin, of course, and how far historically the exchange wants to give it a data. This is the first time stamp for the 4 hour. Let's see what date that is.

**16:36** · For that, I'm using the epoch converter. Just putting it here. And that is Thursday, 11th of April, 2024. And that means that if you run the back test with your AI, that's the first candle it can see, right? So if you run the same back test on Trading View on more data, then of course the data will look different. So make sure to keep that in mind. The good news is that this chart on Binance actually started on the 11th April 2024. So we're good here.

**17:05** · And the reason why I'm on this particular chart, which is exactly TOAO USDT, from Binance, is because the data files that the AI fetched for us are from Binance and it's TOAO USDT, right? So, you need to match that on your trading view when you're comparing the back testing numbers so that you get to the same results. Remember that the AI creates strategies with a start date and an end date.

**17:28** · And the start date is particularly useful in this case because if you don't have historic data as much as Trading View has, then simply pick the same start date as you do have in your data folder and then the back test numbers will match. If you guys want the AI to fetch stock data or commodities data so you can run your strategies on that, then simply tell the AI to do that and it will ask you from where to fetch it.

**17:52** · And I recommend that you fetch stock data from Yahoo Finance and Commodities data from a data feed that Trading View has. Just ask the AI will know what to do. But guys, if you have a larger portfolio and you don't want to mess around building your own strategies because you want to use a system that has been proven to work already, then consider the auto trading masterass, my baby, where I have all my strategies, all my knowledge in there.

### AutoTrading

**18:17** · You learn how to do risk management, how to build a portfolio, how to make sure to not put too much funds in coins that are too risky, how to calculate how much funds to put even, and as well using the trend radar to find new coins that are pumping now so that you don't miss out on new opportunities. This is a new thing that we added to the course and it's a gamecher, guys. If that's what you care about, then make sure to watch this video here and click on apply for access in case you want to join the VIP community.

**18:48** · This is limited to thousand people. We have a conversation, a video call with everybody before they join.

**18:55** · And we make sure that the mindset matches with what we're looking for, which is people that understand that building wealth takes time. There is no get-richquick scheme. You need to understand how the markets work, how to do automation properly. then make sure to apply for access, book a call, and if there is a match, you can join. That's all I have for you guys in this video.

### Next video to watch

**19:16** · And if you want to learn how to automate a trading strategy, really any trading strategy, then this is the next video you should watch. \[music\] It's trading view.

**19:27** · Uh-huh.

**19:29** · Yeah. \[music\] We know what to do. \[music\] Yeah.

**19:37** · Yeah. Yeah.

**19:40** · Stop lost set.

**19:42** · \[music\]