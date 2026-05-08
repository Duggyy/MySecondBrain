---
title: "Private AI on the go… a new trick"
source: "https://www.youtube.com/watch?v=PqBrnip-ZLw"
author:
  - "[[Alex Ziskind]]"
published: 2026-04-01
created: 2026-05-06
description: "I put a tiny MacBook Air between me and some ridiculously large local AI models... and it worked.Power Your Spring Essentials 🌱 Meet the @Jackeryusa Solar G..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=PqBrnip-ZLw)

## Transcript

**0:00** · I've been carrying this MacBook Pro 16inch around with 128 gigs of memory and this lets me load and run pretty large models on my machine like this GPT OSS 12B which is 60 GB. Yeah, all that needs to be loaded into memory in order to run and more because you need some context. Metalama 70B is 70 GB. Those can all fit. But wait a minute, what's this? Quen quarter 4580 billion. That's a huge model and it's 251 GB. Can I add some context? 50,000 load model. What is your name? Oh my gosh, this is working.

**0:35** · My name is Quen. How's this possible?

**0:38** · Well, I know I'm being a little dramatic here, but there is a really cool new feature. And LM Studio, the tool that I'm using to run this, is actually not sponsoring this video, but I think this feature is so cool that I had to show you. And in fact, I'm going to get rid of this machine.

**0:54** · Not forever, but for now. This is 128 GB. I'm going to show you what I can do with this machine, which is just a MacBook Air with 16 GB of memory. This is a lot more portable. But how am I going to run huge models and quickly?

**1:09** · After all, I don't want to have to take this gigantic hardware with me everywhere I go. Flashback.

**1:31** · We waiting on.

**1:32** · Yeah. Oh, thank you.

**1:40** · End of flashback. Now, normally I can load this Gemma 3 4 billion parameter model. A pretty small model. Write a story. And there it goes. It's working.

**1:52** · But look at my memory usage here. 14 GB is being used with everything out of the 16 available. Pretty usable. But this model is not going to be the best quality uh that you're going to get. For example, if I hook it up to VS Code right here, Gemma 34B that's pointing at the local LM Studio instance and I have it hooked up to the VS Code agent describe this file. It's going to take a while because well, first of all, the hardware is not that powerful.

**2:19** · Second of all, yes, I'm serving this from local LM Studio, but there's a lot of prompt processing that has to take place. Look how slow that's going. Yeah, that's in real time. 35 37% 39%. That's prompt processing. It's important. The agent has sent the prompt along with this file over to LM Studio to process it. And it's just a lot. Well, Alex, why don't you just use Claude Opus or Sonnet or GPT 5.3?

**2:49** · This is how I sound like when I'm I don't know, somebody else. I guess a commenter that's not happy. Well, we're talking about running things loc.

**2:58** · Oh, there it goes. Look at that. It's answering me finally. Okay, let's analyze the file. Blah blah blah is doing it. It's about time. Why do we care about this? Because we want to be able to run things locally, securely, and privately. Not for everything. I mean, if you're asking for a recipe, who cares? But if you're protecting your code and your company's code, and you don't want that data to end up somewhere on some servers, who knows where, training other people's models, then you use local. I spent a lot of time thinking about chips, performance, and local AI. But none of that matters if the power is the weak link.

**3:28** · So this spring, one of the smartest upgrades I can make isn't another computer. It's backup power that I can actually use every day. Jackary Plus Mac is the most powerful local AI agent setup. And this is the Jackaryi solar generator 5,000 plus. It gives me serious power without the usual generator downsides. It delivers a whopping 7200 watts with 120 volts and 240 volt support. So it's not just for phone chargers in a lamp.

**3:56** · This thing is built for real backup and real projects. I can keep essential gear running and because it's quiet and indoors safe, it actually fits into the way I work. If power cuts out, I don't want my Mac monitors or storage dropping in the middle of something important.

**4:13** · With UPS backup support, the whole point is that I keep working without that hard stop. And if I want to build this out further, it's expandable up to 60 kwatt hours. So, this can scale way beyond a basic battery box. Charging is flexible, too. I can charge from the wall. I can charge from solar. I can even combine charging methods for faster turnaround.

**4:32** · So instead of being an emergency product, this becomes part of a smarter everyday power setup. For me, this is one of those upgrades that makes the whole setup more resilient, not just more powerful. If you want to see what it can do for your space, power your life with the Jackaryi solar generator 5000 plus. Check out the link in the description for more and live life uninterrupted. Ready? Here we go. This is the new feature in LM Studio 4.5 and higher. I'm going to go to LM link and log in.

**4:57** · Yes, it is a login, but this is just to keep track of your machines because LM Studio now uses Tailcale behind the scenes to keep your connection easy and secure. You don't need to worry about any what I just said. Don't worry about it. For those of you that are familiar with Tail Scale, you know that it's going to be a secure connection. You might even have used this setup before, but it's a pain to set up yourself. Whereas here, you're just pressing a couple of buttons and yeah, just like that, I logged in to my account and now I have access to these models that I am running myself locally.

**5:31** · So, for example, my Mac Studio 1. It's actually not this one. This one's I'm using as a prop. It's that one. That one is running LM Studio and it's got 512 gigs of memory. I have a bunch of models on there and one of them is the Quen Coder 480B. So, all I need to do is go to my chat window and select that one.

**5:53** · New chat, write a story. Boom. I know you all love that prompt, but look, it's writing the story. It's doing it on a 480 billion parameter model. And my local 16 GB of memory wouldn't have been able to do that. Obviously, this is with 50,000 context window, 26 tokens per second. Not bad. But we can also go a little bit faster. This is an RTX Pro 6000. It only has 96 GB of VRAM compared to the Max 512. But still 96 is pretty decent. Oh, look at this.

**6:24** · I have Quen 3 Next 80 billion, which is 45 GB. GPU offload 100%. 48 layers. I can give it a little bit more context like let's go with 50,000. Load model. All right, this is going to be sick. Check this out.

**6:41** · Write a story. Now I'm having it write a story, but this is a really good coding model, too. The Quen series of coder models. Really good. Look how fast that's going. 152 tokens per second on an 80 billion parameter model. And that's running on this machine. Now I can hook it up to VS Code and have some serious firepower when I'm on the go.

**7:00** · All I got to do is just select my model now. Quen 3 next 80B analyze this file as an example. Oh, I'm hearing this thing spinning up a little bit higher. And there it is. It's already printing it. The prompt processing on an Nvidia RTX Pro card is insanely fast.

**7:18** · Everything is fast on that card. So, you saw how quick it just spit out that information and it's higher quality now because it's a larger model. It's faster and I'm doing it here because LM Studio just exposes this as a server that I can connect to from VS Code. Now, some of you are going to say, "Ooh, Alex, you can just set that up directly from VS Code." Of course, you could. You could open up firewall rules. You can set up your own tail scale. You can do port forwarding to the IP address of this thing on your router at home. And then, yeah, you can do all that.

**7:49** · But in LM Studio, everything is done for you. And it's easy. And it's all about saving time, which is why I really enjoy this.

**7:57** · You know what else is really cool? If I already have these models loaded on the different machines, there is zero waiting time between switching models.

**8:05** · So now I'm Quen Next 80B, I can just switch over to Quen Coder 480B. Hi.

**8:10** · Boom. And just like that, I'm using the new model. They're all now available to me all at the same time. And I've just set up another one. I'm now running full Kimmy K 2.5, a model that needs over 1 TBTE of memory. Thanks to Sircale who let me borrow this beefy Nvidia HGX B200 server where I'm hosting LM Studios headless LLMster service. Yeah, that's 8 B200s and that whole model fits in VRAM.

**8:38** · I can run huge models like this privately and totally securely whether I'm doing chat or as a coding assistant.

**8:44** · Now, you probably won't be running LM Studio on a half million dollar server.

**8:48** · You'll most likely be doing professional scenarios like using VLM, but it's just so satisfying seeing it easily munch through that task. Thanks for watching the video, and I think you're going to like this one next. See you next time.