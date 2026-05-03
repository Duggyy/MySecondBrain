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

**0:00** · Hey guys, so today I couldn't be happier to announce the release of Jesse 2.0.

**0:04** · This is one of the biggest releases we've ever had, so I couldn't be more excited. And in this video, I'm going to show you the highlights of it. So, let's get right into it. Now, right out of the bag, you're going to see that the entire dashboard has been redesigned. And we no longer have a navbar here. Instead, we have a sidebar, which you can also minimize. Now, I actually like the minimize version better because it saves me some space so that I can see charts and and things like that better. Next, you can see that the homepage have been redesigned.

**0:31** · And depending on whether you are a new user or someone who has already run some sessions, you're going to see different things. But for me, as you can see, I can see some of the recent access sessions or any other sessions that I've run. And I'm getting some useful stats, but this part specifically is the one that I I would like to show you, which is it shows us how much of the CPU and RAM we are using. Now, this may not look like something that you would actually need.

**0:57** · You would probably think, okay, we already had apps for this. Well, yes, you did. But if you were running just on a production server, then keeping an eye on the resources of the your server was going to be really important, right? So, you want to make sure that you never run out of resources and this is going to make it easy for you to keep an eye on it. Next, we have new back test metrics.

**1:22** · So, we have the max underwater period.

**1:25** · We have separate mean rates for shorts and long trades. But as you can see, we also have new charts. So before we only had the equity curve chart here, but now not only we have that, we also have it in the log scale version. We also have the max drawdown chart which also shows us the worst five periods. And it will also show us like how much each of them were losing. And we can also click on the chart to see it in bigger sizes. And as you can see like my worst max draw down period for this strategy was minus7% which was this period.

**1:54** · And if you also read this max underwater period you can also see that it was 50 days. So this period right here was 50 days which basically tells me that if I were to run this strategy for 50 days I was going to have a really hard time until I was able to basically make back whatever I lost in this period.

**2:17** · Next we have the underwater plot and then the monthly returns heat map which is also super helpful and the monthly returns distribution chart and trade panel distribution chart. So some of these are completely new and some of them you've probably seen in other libraries such as the constats which at some point we were actually using inside JC itself but then we had to discontinue that and now I'm happy to say that we have access to these charts again but this time they are all built in in the house. Also, I've made some changes to the layout.

**2:49** · So, now the performance metrics is in here in the sidebar and not here, which actually makes it really easier to read.

**2:56** · Next, and probably the biggest change in this release is the rule significance test, which is this statistical test that which will tell you whether or not the entry rule of the Euro strategy has any predictive power or not. Now as you can see here we have the distribution chart and this line here and the conclusion of it is that this my strategy actually has a very significant in rule and we also have some and we

**3:26** · also have some raw data which can help you further such as the analyst return of the inter rule the observed mean and the number of observations and the simulations that we run for this. Now to show you an example to understand what this does. Well, let me show you some actual code. And for it, we're going to run the rule significance test inside the terminal because I also added it to the research module of Jesse. And in fact, just so you know, the one that I added to the research module is completely free for everybody. But the one that is accessible via the dashboard is for premium users only.

**3:57** · But in the usage, they all do the same. So let's just check it out. Now here we have this strategy that if I were to actually run it I would have made money. So you can see the inter rule of the strategy is 7.4%.

**4:12** · Now by the way this is just for the inter rule of the strategy. Okay? So it's not the entire strategy. Now if you don't fully understand what I'm talking about it doesn't matter because I am going to record a full video just about this topic because it definitely deserves its own separate video because I spent months on this topic and I had to read the whole book just to understand it. But for now in this video I just want to show you the highlight of it. So here we have a strategy that is making money. But the reason that it is making money is because it was trading purely a huge uptrend.

**4:40** · And in fact if I show you the code for the strategy that I am running here all that it is doing is that it's trying to open a long position with 80% certainty. And in other times it either doesn't open a position or it opens the short position.

**4:59** · However, because I was running this test during a huge uptrend in the Bitcoin market, then it is simply making money.

**5:07** · But as you can guess, such a strategy does not have any predictive power, right? We're just being lucky here. If I were to execute this strategy during a bare market, we were going to get slaughtered without any doubt. And as a result, if I run this strategy, the result of the test is that it says the random signals have no edge. and that my integer rule is not significant because the p value is above well uh this value although in the final results I've actually said that I want a p value below 10%. Okay.

**5:37** · So even above 5% it might have some significance but in here you can see it's actually even slightly above 10%. So it definitely has no edge.

**5:50** · And if I show you the distribution chart you can see the returns of the strategy is not by far more than the random ones.

**5:58** · So we're going to conclude that it does not have any actual edge. Here I have another strategy which actually does have some edge. So it has some actual interior rule that is checking the data and making decision based on that. So it does have some predictive power. And if I run the same test on the same period for this one, I'm going to get this result which basically is below 10%. So we're going to conclude that it does have some significance. Now by the way, I wrote this part before. So I need to update it. So please ignore this part that it says it's not significant.

**6:26** · So the important thing is that the p value is low. Also one other reason that I'm getting this result and not something like yeah your inter rule is super significant that's because the period of the back test is actually very low. So sometimes you need to increase that to get a more accurate results. And if we take a look at the distribution and if you take a look at the distribution chart we can see that the returns of the uh actual strategy is actually better than most of the simulated ones. Also once again the one that I have here is actually a better example.

**6:57** · So this one is running on a full year and on a lower time frame. So it means that we are running more simulations. And the more simulations you run with any kind of randomization test, the more accurate results you're going to get. And as you can see, it's telling me that the interior rule of the strategy is indeed very significant. And the p value is actually even below 1%. So there you go.

**7:19** · All this test does is it's going to tell you if the inter rule of the strategy has some predictive power or not. It's not going to tell me if my strategy is ready for production or whether or not it is overfit. It is nothing like that.

**7:33** · But the way this is helpful is because imagine you have an idea for an inter rule to write a strategy based on it.

**7:40** · Now before you spend time like hours on that strategy to get the position size right right to get the exit rules right.

**7:49** · So before doing any of those things, you just simply test your integer rule. And if it says that it is not sign significant, then you're just going to drop it right there. You're not going to waste time on it. But if it says that the inte rule is significant, then you can spend time on it to develop an actual strategy and hopefully you will get some good results. But again, so it doesn't tell you that the strategy is definitely awesome, but it can tell you if it definitely isn't. Does that make sense?

**8:17** · Now anyways, you definitely need to do more research on this topic because it is actually very helpful and important and I am making a video about it. So stay tuned for that. But in the meanwhile, you can also read the documentation that I wrote for it and we have a page fully describing the steps and why it matters and like the underneath method that I am using as a statistical test for this mode and how to exactly read the results that you are getting. And as I mentioned, you can also use this inside the research module.

**8:48** · So if you need to run it via a program or you can have the AI to write some code for you if that's what you want to do, you can use the research module of JC which you can find the documentation for it right here. Now the next thing that I did is that I added the optimization mode as a function to the research module. So before we didn't have this, you could only run optimization sessions v the dashboard of JC which is pretty beautiful and helpful and then it's like awesome. But there are some cases that you want to run the optimization session via a program.

**9:20** · Again, maybe you want to have your AI to write the code for you or control it even if that's what you want to do then the research module is the one that you want. And there were actually many requests for the optimize mo function in the research module and that's what I did. So now we have it. And by the way, just so you know, we are going to have Jess's own MCP very soon. So that is also definitely coming. Now, while we are in the documentation, I should also give a shout out to the machine learning stuff that we added.

**9:46** · So if you watched my previous video about machine learning, then you know this was added just recently, but it wasn't in the previous major release. So you need to know this that this is also new. But at the moment, it is only supported inside the research module. And I'm not even sure if you're going to add it to the dashboard because the way you're going to use machine learning is very flexible and very unique to your own strategy.

**10:10** · And I'm not sure how to add that to the UI like what sort of use case we're going to have for it. But as a function, it is super helpful and you can use it in unlimited ways. And I made a video about it. So go watch it if you want to know like how I use it. But definitely the documentation for it is also really helpful. Like if you read this whole thing, you may not have to read like a whole book about machine learning just to be able to use it like I had to.

**10:34** · And just so you know, our machine learning supports regression models and the binary models and multiclass classification. So it is pretty flexible. Now I wouldn't say like it is handling like 100% types, but I think it can handle most use cases of machine learning in trading. Now, by the way, this is a video that I was talking about. So if you haven't watched it, definitely make sure to give it a watch.

**10:58** · It is a very interesting topic. Now you might be thinking, okay, so now that we are in version two, does that mean there have been some breaking changes? Well, I made my best to lower the breaking changes and the the only one that actually most of you have to worry about is related to the back test function of the research module. So if you were using Jess's back test using the function so not the mode in the dashboard then you're going to check to ensure that you are using the correct API for the charts and things like that.

**11:31** · So that's the only change that we had.

**11:33** · Now we also had some small changes. So for example if you are in the back test settings and you want to quickly look up the exchange that you need to change settings. Well before you had to just look for it which was a bit annoying but now we have a search box for it. So these sort of small adjustments have been done in the entire dashboard, but I didn't document those. But hopefully you're going to be happy about it because these are based on your direct feedback in the past few months and years. So that's it guys. I've been focused on development only for the past like god knows how many weeks.

**12:04** · And starting now, I'm going to go back to do some research for myself and making more videos for you guys. So definitely stay tuned for that because new videos are coming soon. And as always, if you had further feedback about like any changes you want in the dashboard or new features that you want to be added or improvements to the existing ones, just pay me on our Discord server. Thank you so much for being a part of the JC community and thanks for watching this video. I'll see you in the next one soon.