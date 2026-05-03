---
title: "Jesse 2.0 Is Here! Algo-trading reimagined"
source: "https://www.youtube.com/watch?v=Rw1zLZK3XJg"
author:
  - "[[Algo-trading with Saleh]]"
published: 2026-04-30
created: 2026-05-03
description: "in this video, I will show you the highlights of the 2.0 release of the Jesse framework"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=Rw1zLZK3XJg)

## Transcript

**0:00** · Hey guys, Sal. Today, I couldn't be happier to announce the release of Jesse 2.0. This is one of the biggest releases we've ever had, so I couldn't be more excited. And in this video, I'm going to show you the highlights of it. So, let's get right into it.

**0:12** · Now, right out of the bag, you're going to see that the entire dashboard has been redesigned, and we no longer have a navbar here. Instead, we have a sidebar, which you can also minimize. Now, I actually like the minimized version better because it saves me some space so that I can see charts and and things like that better. Next, you can see that the home page have been redesigned, and depending on whether you are a new user or someone who has already run some sessions, you're going to see different things.

**0:38** · But for me, as you can see, I can see some of the recent backtest sessions or any other sessions that I've run, and I'm getting some useful stats.

**0:47** · But this part is specifically is the one that I I would like to show you, which is it shows us how much of the CPU and RAM we are using. Now, this may not look like something that you would actually need. You would probably think, "Okay, we already had apps with Well, yes, you did, but if you were running Jesse on a production server, then keeping an eye on the resources of the your server was going to be really important, right? So, you want to make sure that you never run out of resources, and this is going to make it easy for you to keep an eye on it. Next, we have new backtest metrics.

**1:22** · So, we have the max underwater period, we have separate win rates for shorts and long trades, but as you can see, we also have new charts. So, before, we only had the equity curve chart here, but now, not only we have that, we also have it in the log scale version. We also have the max drawdown chart, which also shows us the worst five periods, and it will also show us like how much each of them were losing, and we can also click on the chart to see it in bigger sizes.

**1:49** · And as you can see, like my worst max drawdown period for this strategy was minus 17%, which was this period. And if you also read this max underwater period, you can also see that it was 50 days. So, this period right here was 50 days, which basically tells me that if I were to run this strategy for 50 days, I was going to have a really hard time until I was able to basically make back whatever I lost in this period.

**2:17** · Next, we have the underwater plot, and then the monthly returns heat map, which is also super helpful, and the monthly returns distribution chart, and trade panel distribution chart. So, some of these are completely new, and some of them you've probably seen in other libraries such as the QuantStats, which at some point we were actually using inside Jesse itself, but then we had to discontinue that. And now, I'm happy to say that we have access to these charts again, but this time they are all built in in the house.

**2:46** · Also, I've made some changes to the layout, so now the performance metrics is in here in the sidebar and not here, which actually makes it really easier to read. Next, and probably the biggest change in this release is the rule significance test, which is this statistical test that which will tell you whether or not the entry rule of the your strategy has any predictive power or not.

**3:09** · Now, as you can see here, we have the distribution chart and this line here, and the conclusion of it is that this my strategy actually has a very significant entry rule.

**3:23** · And we also have some And we also have some raw data, which can help you further, such as the annual return of the entry rule, the observed mean, and the number of observations and the simulations that we run for this. Now, to show you an example to understand what this does, well, let me show you some actual code, and for it, we're going to run the rule significance test inside the terminal because I also added to the research module of Jesse.

**3:47** · And in fact, just so you know, the one that I added to the research module is completely free for everybody, but the one that's is accessible via the dashboard is for premium users only. But in the usage, they all do the same. So, let's just check it out. Now, here, we have a strategy that if I were to actually run it, I would have made money. So, you can see the entry rule of the strategy is 7.4%.

**4:12** · Now, by the way, this is just for the entry rule of the strategy, okay? So, it's not the entire strategy. Now, if you don't fully understand what I'm talking about, it doesn't matter because I am going to record a full video just about this topic because it definitely deserves its own separate video because I spent months on this topic, and I had to read the whole book just to understand it. But for now, in this video, I just want to show you the highlight of it. So, here, we have a strategy that is making money. But the reason that it is making money is because it was trading purely a huge uptrend.

**4:41** · And in fact, if I show you the code for the strategy that I am running here, all that it is doing is that it's trying to open a long position with 80% certainty. And in other times, it either doesn't open a position or it opens a short position.

**4:58** · However, because I was running this test during a huge uptrend in the Bitcoin market, then it is simply making money.

**5:07** · But as you can guess, such a strategy does not have any predictive power, right? We're just being lucky here. If I were to execute this strategy during a bear market, we were going to get a slaughtered without any doubt. And as a result, if I run this strategy, the result of the test is that it says two random signals have no edge, and that my entry rule is not significant because the P value is above, well, uh this value. Although, in the final results, I've actually said that I want a P value below 10%, okay?

**5:40** · So, even above 5%, it might have some significance, but in here, you can see it's actually even slightly above 10%, so it definitely has no edge. And if I show you the distribution chart, you can see the returns of the strategy is not by far more than the random ones, so we're going to conclude that it does not have any actual edge. Here, I have another strategy, which actually does have some edge. So, it has some actual entry rule that is checking the data and making decision based on that, so it does have some predictive power.

**6:10** · And if I run the same test on the same period for this one, I'm going to get this result, which basically is below 10%, so we're going to conclude that it does have some significance. Now, by the way, I I wrote this part before, so I need to update it, so please ignore this part that it says it's not significant. So, the important thing is that the P value is low. Also, one other reason that I'm getting this result and and not something like, "Yeah, your entry rule is super significant."

**6:34** · That's because the period of the backtest is actually very low, so sometimes you need to increase that to get a more accurate results. And if we take a look at the distribution and if you take a look at the distribution chart, we can see that the returns of the uh actual strategy is actually better than most of the simulated ones. Also, once again, the one that I have here is actually a better example, so this one is running on a full year and on a lower time frame, so it means that we are running more simulations.

**7:03** · And the more simulations you run with any kind of randomization test, the more accurate results you're going to get. And as you can see, it's telling me that the entry rule of the strategy is indeed very significant, and the P value is actually even below 1%. So, there you go. All this test does is is going to tell you if the entry rule of the strategy has some predictive power or not. It's not going to tell me if my strategy is ready for production or whether or not it is overfit.

**7:30** · It is nothing like that, but the way this is helpful is because imagine you have an idea for an entry rule to write a strategy based on it.

**7:40** · Now, before you spend time, like hours on that strategy to get the position size right right, to get the exit rules right. So, before doing any of those things, you just simply test your entry rule. And if it says that it is not signifi- significant, then you're just going to drop it right there. You're not going to waste time on it. But if it says that the entry rule is significant, then you can spend time on it to develop an actual strategy, and hopefully, you will get some good results.

**8:07** · But again, so it doesn't tell you that the the strategy is definitely awesome, but it can tell you if it definitely isn't.

**8:16** · Does that make sense? Now, anyways, you definitely need to do more research on this topic because it is actually very helpful and important, and I am making a video about it, so uh stay tuned for that. But in the meanwhile, you can also read the documentation that I wrote for it, and we have a page fully describing the steps and why it matters, and like the underneath method that I am using as a statistical test for this mode, and how to exactly read the results that you are getting. And as I mentioned, you can also use this inside the research module.

**8:48** · So, if you need to run it via a program, or you can have the AI to write some code for you, if that's what you want to do, you can use the research module of Jesse, which you can find the documentation for it right here. And the next thing that I did is that I added the optimization mode as a function to the research module. So, before, we didn't have this. You could only run optimization sessions via the dashboard of Jesse, which is pretty beautiful and helpful and and it's like awesome, but there are some cases that you want to run the optimization session via a program.

**9:19** · Again, maybe you want to have your AI to write the code for you or control it even. If that's what you want to do, then the research module is the one that you want, and there were actually many requests for the optimize mode function in the research module, and that's what I did. So, now we have it. And by the way, just so you know, we are going to have Jesse's own MCP version soon. So, that is also definitely coming. Now, while we are in the documentation, I should also give a shout-out to the machine learning stuff that we added.

**9:46** · So, if you watched my previous video about machine learning, then you know this was added just recently, but it wasn't in the previous major release, so you need to know this that this is also new, but at the moment it is only supported inside the research module, and I'm not even sure if you're going to add it to the dashboard because the way you're going to use machine learning is very flexible and very unique to your own strategy, and I'm not sure how to add that to the UI, like what sort of use case you're going to have for it.

**10:15** · But as a function, it is super helpful and you can use it in unlimited ways, and I made a video about it. So, go watch it if you want to know like how I use it. But definitely the documentation for it is really helpful.

**10:28** · Like if you read this whole thing, you may not have to read like a whole book about machine learning just to be able to use it like I had to. And just so you know, our machine learning supports regression models and the binary models and multi-class classification. So, it is pretty flexible. That I wouldn't say like it is handling like 100% types, but I think it can handle most use cases of machine learning in trading. And by the way, this is the video that I was talking about. So, if you haven't watched it, definitely make sure to give it a watch. It is a very interesting topic.

**10:59** · Now, you might be thinking, "Okay, so now that you're on version two, does that mean there have been some breaking changes?" Well, I made my best to lower the breaking changes. And the the only one that actually most of you have to worry about is related to the backtest function of the research module. So, if you were using just this backtest using the function, so not the mode in the dashboard, then you're going to check to ensure that you're using the correct API for the charts and things like that.

**11:30** · So, that's the only change that we had. Now, we also had some small changes. So, for example, if you're in the backtest settings and you want to quickly look up the exchange that you need to change the setting. Now, before you had to just look for it, which was a bit annoying, but now we have a search box for it. So, these sort of small adjustments have been done in the entire dashboard, but I didn't document those.

**11:52** · But hopefully you're going to be happy about it because these are based on your direct feedback in the past few months and years. So, that's it, guys. I've been focused on development only for the past like God knows how many of weeks, and starting now I'm going to go back to do some research for myself and making more videos for you guys. So, definitely stay tuned for that because new videos are coming soon.

**12:14** · And as always, if you had further feedback about like any changes you want in the dashboard or new features that you want to be added or improvements to the existing ones, just ping me on our Discord server. so much for being a part of the Jesse community and thanks for watching this video. I'll see you in the next one soon.