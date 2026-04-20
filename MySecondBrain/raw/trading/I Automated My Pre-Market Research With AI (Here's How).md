---
title: "I Automated My Pre-Market Research With AI (Here's How)"
source: "https://www.youtube.com/watch?v=sh5h0GJzjNk"
author:
  - "[[SMB Capital]]"
published: 2026-04-14
created: 2026-04-19
description: "Learn the top 3 trade setups we are using on the desk here: https://bit.ly/4tbCZvtPrompts: https://www.smbtraining.com/blog/i-automated-my-pre-market-researc..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=sh5h0GJzjNk)

## Transcript

**0:00** · Every morning before the market opens, I used to spend about an hour doing the same thing, opening a stack of research emails and newsletters, trying to piece together what actually mattered for the trading day. The information was good, but it was scattered. And by the time I'd fully synthesized it, the market was about to open. So, I built a system that does it for me.

**0:19** · Now, every weekday morning before 8:30 a.m., an AI workflow reads my market research emails, pulls out everything that matters, macro context, economic data, stocks in play, key themes, and generates a structured trading briefing along with a full dashboard that I could scan in just a few minutes. In this video, I'm going to show you exactly how it works and how you can build your own version, even if you have zero coding background.

**0:48** · I built this myself and I'm certainly not a developer. Let me show you what this actually looks like. This is the daily market rundown the system generates every morning before the open. At the top, there's a quick market snapshot.

**1:05** · This gives me the key macro setup for the day in just a few sentences. For example, it highlights the current Fed stance, the most important economic data being released that morning, and any major geopolitical developments that can influence markets.

**1:22** · Below that is the macro tone section.

**1:25** · This summarizes the most important developments driving the market so I can quickly understand the bigger picture heading into the trading day. It also expands on the key overnight developments that includes things like geopolitical events, commodity moves, or changes in investor sentiment. Next is the economic calendar. This highlights the key economic data releases scheduled for the day.

**1:50** · For each report, it shows the time of the release, the type of event, the prior number, the current estimate, and a label indicating the importance of the release. This makes it easy to quickly identify which reports are most likely to create volatility and exactly when they're scheduled to hit the market. The rundown also highlights the key earnings reports for the day.

**2:15** · These are companies reporting either before the open or after the close.

**2:19** · Earnings are one of the biggest drivers of individual stock volatility. Having them clearly listed helps me quickly identify potential trading opportunities.

**2:30** · There's also a section highlighting other important events happening during the day. This includes things like economic releases, earnings calls, conferences, or other scheduled catalysts that can influence market activity. Next is the top movers section. This is where the system identifies the stocks most likely to be active during the trading session.

**2:51** · The AI reads through my morning research emails, looks for companies with meaningful catalysts, things like earnings releases, analyst upgrades or downgrades, guidance changes, or other significant news.

**3:08** · For each name, it lists the ticker, the direction of the move, the catalyst behind the news, and a short explanation of why that stock could see volatility during the day.

**3:21** · Instead of manually scanning multiple research sources, the system consolidates the most important catalysts into one place.

**3:30** · Next is the research theme section. This is where the system pulls together the broader narratives developing in the market. As the AI reads through the research, it looks for themes that could connect multiple stocks or sectors. This could include things like AI infrastructure spending, shifts happening in software, energy developments, or changes in consumer behavior. Instead of just looking at individual tickers, this helps identify the bigger forces driving the market.

**4:02** · That context can be extremely useful when you're thinking about sector level opportunities or understanding why certain groups of stocks are moving together.

**4:12** · Next is the secondary name section. This shows additional tickers that appeared in the morning research along with their associated news. For each name, the system lists the ticker, potential direction of the move, and a short note describing the catalyst behind the news.

**4:31** · These may not be the primary focus of the trading session, but they still represent stocks with developments worth keeping on the radar. Having them organized here makes it easy to quickly scan for additional opportunities that might develop during the day. And if one of these names pops up on a scanner later in the session, I could come back here, hit controlf, and quickly see why that stock might be moving. And finally, we have the week ahead section.

**4:57** · This highlights the major events and catalysts coming up over the next several days. That can include things like key economic reports, important earnings releases, policy announcements, or other events that could impact the market. Having these laid out in advance helps me anticipate potential volatility and plan ahead for upcoming trading opportunities.

**5:21** · The goal of this entire rundown is simple, to compress everything I need to know before the open into something I could scan in just a few minutes. Now, let me show you how this system actually runs. This workflow runs inside Claude's co-work environment. Here, you can see the daily market rundown task.

**5:43** · The task is scheduled to run weekdays at 8:00 a.m. before the market opens.

**5:52** · Right now, it's active, and you can see the next scheduled runtime here. Below that, this is the run history. This shows each time the system has executed the workflow.

**6:05** · Every time it runs, the system reads the morning research emails, generates the markdown briefing or MD file, which is like a word document, and then updates the dashboard automatically.

**6:23** · So, if we click on one of those entries in the history, you'll see co-work You'll see the morning rundown, the MD file, the app that it updated. The key thing here is this runs fully unattended. I'm not manually triggering anything each morning. The only time we have to manually trigger is if Claude has an update and we need to approve access to a folder where the project lives, which we'll get into.

**6:54** · Instead of spending time reading through multiple research emails and organizing the information myself, the system does that first pass automatically before the market opens.

**7:08** · Now, let me show you how you could build a simplified version of this workflow yourself. The first step is creating a project folder where Claude can store the files it generates. On a Mac, I'll open Finder, go to the documents folder, and create a new folder for the project.

**7:26** · If you're on Windows, you would do the same thing using File Explorer and create the folder inside your documents directory. I'm going to create a folder called market rundown demo. This folder will become the working directory for the project.

**7:52** · Now that the project folder is created, we need to tell Claude to work inside that directory. This allows Claude to create and update the files for that project inside that folder. So, we'll start a new task. We'll select work in a project.

**8:15** · Choose a different folder and we'll open the market rundown demo folder.

**8:22** · Allow claw to change files in market rundown demo. Always allow. The system also needs access to the email sources that contain the morning research. To do that, you'll need to configure the official Gmail connector inside Claude.

**8:40** · Once that connector is enabled, Claude can read the research emails that come into your inbox each morning and extract the key information needed to generate the rundown.

**8:54** · So you would go to settings, connectors, and you would see Gmail.

**9:00** · Mine's already configured.

**9:03** · And once that Google connector is configured and Claude knows where the project folder is located, now we're ready to start having fun in building the workflow. The first step is defining the structure of the daily market rundown. AI works much more reliably when you give it a clear framework to organize information that you want. So before we ask Claude to generate the rundown, we first define the structure we want it to follow each day.

**9:30** · In this case, we're creating sections for the key information traders care about the most. Things like macro context, economic data, earnings, stocks in play, broader market themes, and upcoming events. Once that structure is defined, Claude can use it as the template for generating the daily rundown. So, I'm going to prompt Cla Claude and I'm going to say, I want to build a daily market rundown workflow for traders.

**9:57** · The workflow should read morning market research emails, extract the most important information, organize it into a structured daily briefing. The briefing should prioritize the information traders care about the most, including macro context, economic calendar, earnings reports, top movers with catalysts, broader market themes, secondary names with fresh news, and week ahead events. And we'll hit enter.

**10:28** · So, we want to start by defining the ideal structure for this rundown as a clean markdown outline that could be used every day.

**10:39** · So, Claude's working hard scanning through my emails and it's generating a rundown file. You can see the progress as it's going through the lists of tasks that it needs to do.

**10:56** · It's jumping ahead a little bit and it's asking me to schedule a task. We're not going to do that just yet.

**11:04** · Okay, Claude ran right into my email right away and filled out the structure that we asked it to.

**11:15** · Normally the next step and skip this step but normally the next step would be to say hey now that we have the structure we could ask claw to generate today's market rundown from the research emails but it did all of that in one step. So, the next prompt would have been, now that we have the structure, we could ask Claude to generate today's market rundown from the research emails.

**11:42** · Read the market research emails that arrived today in my inbox between 5:00 a.m. and 8:30 a.m.

**11:51** · Only use information from those email sources. Use the structure that we created with the first prompt and generate today's market rundown as a markdown briefing. which it already done and it's listed here in the working folder. Daily market rundown April 10th.

**12:11** · We just reminded of some requirements.

**12:14** · Summarize the information rather than quoting emails directly. Extract the most important macro developments.

**12:21** · Identify key economic events for the day. Highlight notable earnings reports.

**12:26** · Identify the most important stocks in play. For stocks in play, focus on names with clear catalysts. Briefly explain why the stock can move today. Prioritize stocks likely to see meaningful intraday volatility. Also include broader market themes, secondary names with fresh news, key events later in the week. The output should be a clean markdown briefing that a trader could quickly scan before the open.

**12:55** · So Claude ran away a little bit and we do not have to enter in this step two. It already went into my email and generated the daily market rundown. So let's click on that and check it out.

**13:11** · All right. And let's see the markdown file that Claude created. Macro context, economic calendar, earnings reports and previews, top movers, broader market themes, secondary names, week ahead. All right.

**13:35** · So, now that Claude has generated the markdown briefing, the final step is turning it into a dashboard that's easier to scan each morning. The markdown or MD file is simply a lightweight text format that Claude generates that we're using as the structured source document for the rundown.

**13:57** · Now, we're going to tell Claude using the Markdown daily market rundown we just generated, create a simple HTML dashboard that a trader could view in a browser. Requirements: dark theme, clean layout, clearly separated sections, easy to scan quickly before the market open, uh, and preserve the structure that we just created in that rundown. All right, Claude's thinking. It's going to create our app. All right.

**14:25** · And off to the right here, you could see our market rundown demo folder that we gave Claude access to work in. Uh we have our markdown text and we have our HTML app. Let's check the HTML app. All right, pretty good for a first run. We have macro context.

**14:51** · We have an economic calendar.

**14:56** · We have earnings reports and previews.

**14:59** · TSM pre-released earnings this morning.

**15:02** · That's good that we have that there.

**15:05** · And we have our top movers.

**15:11** · Very good. Oh, that's cool. Decided to do pre-market losers and give us some short ideas. Mostly software names.

**15:19** · Makes sense.

**15:25** · Okay. Looks pretty good.

**15:30** · The final step is scheduling the workflow so it runs automatically each morning. This allows Claw to generate the rundown before the market opens without me having to manually run anything. Prompt four, our final prompt would be create a scheduled task for this workflow. The task should run automatically every weekday morning before the market opens at 8:30.

**15:56** · Each time it runs, it should read the morning market research emails, generate the daily market rundown markdown briefing, update the existing HTML dashboard.

**16:11** · The HTML dashboard should be updated in the same file each day. So, new rundowns are appended rather than replacing previous ones. This allows a dashboard to maintain a running archive of daily market briefings that could be reviewed.

**16:29** · And I would hit enter. And then co-work would prompt me to select a time and the task would automatically execute without any manual input.

**16:42** · And just to reiterate that project lives in our folder in our documents. If we go to documents, we go to market rundown demo, you'll see the markdown file and you'll see the HTML app. If we double click there, we have our HTML app.

**17:10** · All right. So, most traders will never have a research team or even their own analyst, but they don't need one anymore. The largest hedge funds in the world have had this kind of infrastructure advantage for years. The difference now is that tools like Claude make it possible for individual traders to build something like this in an afternoon. If you want to take this further, I'll link the full prompts I used in the description below so you could start building your own version today.

**17:40** · If you found this helpful, drop a comment and subscribe.