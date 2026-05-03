---
title: "I Built a Local AI Agent with Gemma 4 — Runs Fully Offline"
source: "https://www.youtube.com/watch?v=VhjshBCqwrQ"
author:
  - "[[Prompt Engineer]]"
published: 2026-04-26
created: 2026-05-03
description: "👉 Try RunPod for Amazing GPUs: https://get.runpod.io/pe48In this video, I show how to set up a local AI agent using Gemma 4 (4B model) on your system — no i..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=VhjshBCqwrQ)

## Transcript

### Intro

**0:00** · You can see that Gemma 4 E4B is running on my local system using 67%age of my CPU and 33% of my GPU and it's running in an agentic mode using continue and I can do all these works locally not even connected to the internet. So in this video I'm going to show you how to set this up. Imagine yourself in a secluded island where you have your laptop and now you want to use your agent. you're not connected to the internet but definitely you need internet when you are setting this for the first time but then it's a piece of cake.

**0:31** · So you have Gemma 4E 4B running on Olama and Olama exposes this into a port on your PC and then continue uses that port uses that LLM and you can see here it's Gemma 4 E4B it's using that LLM and doing all these works. So what I started with was I asked it to make a front-end page here. So this is a beautiful front-end page. But again, I wanted the dark theme.

**0:58** · So I asked it to change to this dark theme and it went ahead and did the changes for me. Now it's waiting for me to accept and I can just accept the difference and I can see the output here. Let me refresh this. So this is the dark background. You can go ahead and iterate with this. But you can see the agentic performance of this model.

**1:18** · This model is really amazing. Gemma 4.

**1:22** · It's a local model from Google. And let's go ahead and uh try to set this up on your local system. So the first and foremost thing that you need is VS Code or any code editor for the matter. In this example, I'm using VS Code. So go ahead and download this for Windows.

### Tech-Stack

**1:36** · We'll get an .exe file and then we will have the VS code here. Then in the VS code, we need one extension of continue.

**1:43** · Continue. If you go to the extensions here on the VS code and again search for continue you can see that this is continue an open-source AI code agent.

**1:53** · So using continue we can use different closed source and open source LLMs and one of the providers is Olama. So we are using that Olama. Now we also need to have Ola installed. So go ahead and use install Olama. You can go ahead and just copy this command to PowerShell and that get it installed. But basically once you have that installed if you go to a command prompt you can see that uh you just type in Olama to make it start and once you start Ola what you can do is you can see the list of models that we have. Okay. So I have Gemma 4 E4B which is a 9.6 model size.

**2:25** · So if you go to Gemma models Gemma 4 and based on your local configurations you can use any of these. Now my PC has an 8 GB GPU and uh 16 GB RAM. So the best thing that I could make it work was this model which is gema 4 E4B. So E is effective 4 billion and then copy this and what you need to do is you need to say Olama pull and the name of the model. So this will pull the model. Now it will start to manifest.

### Ollama Pull Model

**2:55** · It will pull the model and since I already have the model loaded so it is showing immediately but in your case it will take definitely take some time to get the model loading. Now once you have that you can go ahead and run this here itself. You can say ola run jma 4 e4b but I'm not interested in running this as just as a model but what I'm interested is running this as an agent. So for getting that agendic behavior once you have installed continue it will be available here. Let me close all of these.

**3:23** · So once you install continue it will be available here on the right. So if you close this and this it will be available here. So you can see that this is one of the open source AI code agent. So we have other agents such as client uh and copilot and cloud code. But in this case we are using continue. So if you go to continue and click here to start up a new session you can go ahead here and then go to models and then set up. So I click on the settings here configure here and then set up the model. So you can set up the model like this which goes like model gemma 4.

### Setup Models

**3:53** · So you need to write this thing here and then this model will be auto setup here. You can add models here using this button. You can add models as well. So the first time when you do it, you can choose Olama here and then you can do auto detect and just say connect and you can see that it will come as an auto detect here. But what we need is but what we need is this model. So we are going to change it manually to this format where we have provider as the title is this and the model is this.

**4:20** · So once you have that you're going to save this and then your model is perfectly ready to use. So go back. So go back and ask it any questions. So let me close this. And what you can do for a demo is you can go to an open folder here. You can open up a new folder. I'm going to create this new folder called local AI and then open up VS code. So you can see that we have continue here. And one of the other things that I would like to show you is the use of tools.

**4:45** · So what you can do is you can go to the settings now and inside the settings of continue you can see that we have all these options. Uh show session tabs. Yes, I would like to display wrap code blocks.

### Settings

**4:59** · Wrap long lines instead of showing horizontal scrolling. Yes, show site scroll bar text to speech output. We can leave that for now. And we have all these settings. The thing that I was able to show you is this. I've already shown this is the models. You can go ahead and add models here. I've added a local model which is Gemma 4 E4P. There are different rules that you can add just like cloud code rules. You can add your own rules. Add your own rules here and your prompts here.

**5:20** · You can go to tools and you can see that we have 14 number of built-in tools and in your first time when you are starting this up you would have this as ask first or exclude as something like that you can go ahead and see and uh do this automatic for example if you feel like it should be automatic so ask first run terminal command file glob searches automatic read currently open file u automatic so you can make this automatic as per your choice it's up to you but you can add another tools as well you can add mcp piece.

**5:50** · So you go ahead to the plus button and then you can add in your own MCP servers and that's for a different video. You can go to config now and click on local config. Click on the settings file and this will open up the config file. So in the config file we have just one model but we have other things that you can use there as well.

**6:09** · Now let's go ahead and test this out. So we are in continue and we are in this new folder which is the local AI folder here. I'm going to close everything. I'm going to ask I can say create a simple login page for a training session like AI for developers. As simple as that.

### Test

**6:26** · So you can see the speed. This video is not sped up or anything like that. You can see the speed. It's pretty amazing.

**6:33** · Would you like to proceed with the basic HTML CSS mockup? I can do this voice as well. Yes, I would like to go ahead with the HTML CSS mockup and just send over and you can see that it's pretty fast. So the resources that we are using you can go here and uh we can say lama ps to see uh what is being used. So we have this context length of 8192 and using something like this 67%age of the GPU and 32% of my CPU. So you can see that it has started.

**7:08** · So the earlier settings uh that we have done where we can scroll this now. So you can see that we are able to scroll this and you can see this is pretty amazing. It's so fast. Go back one year and you can see that these models were not that powerful. But now Jamaa for the game has changed. So it it has created the index.html file that's done. And you can see here we have created the CSS as well. The index HTML and CSS are now set up with a clean modern responsive look.

**7:41** · You can see the inference speed. It's really amazing. But what things that you have to make sure just like if you're working on cloud code or anything is that you need to be aware of the context that you're in. So if you feel like that you are using too much of the context since we have very less context here, you can go ahead and start up the fresh context or you can get a summarized thing that you have done till now and use that summary to proceed further. So let me go back to the folder here and then open up.

**8:10** · So this is in this folder which is local AI and here we have these two files. So let me open up this. It's a pretty amazing pretty beautiful for developers training session. I can say make it dark theme and let's see I will update style CSS. You can see the speed.

**8:28** · I have all the recording instruments going on. I have OBS recorder and all the other things that is going on but still it is able to bring this output to me so fast. Uh when I don't have the recording on it's even faster. So you can see that this is itself is a very strong local model that you can use. Now depending on your hardware if you have a 24 GB RAM you can go ahead to the other models like 21 billion or the 26 billion.

**8:52** · So this models that you have you can go for this models you need about 26GB GPU then you can use this 31 billion model as well and that will be will have even more context and it will be better outputs but for the basic task for example basic automations basic web designs you can use this so you can see that continue is editing the style dot CSS all right it has updated it seems the style is successfully updated to a sleek dark theme let's refresh you can

### Summary

**9:20** · see the dark theme how amazing is that This is local model running on your system. In summary, what I have is Gemma 4 E4 billion model is running on my local system using Olama and basically Ola exposes a port called 11434.

**9:36** · And what continue is doing is that it is sending commands to this 11434 port getting the output and giving you the response. But the reason we're using continue because you know agentic behavior. So for example you know tool use that we see here automatic changing understanding the context. So all these agentic things you cannot get it on a simple cmd run. So we are using the model via lama and punching and linking with continue so that you can use this better. Now instead of the VS code you can use other instead of continue you can use other AI agents.

**10:05** · Instead of Olama, you can use LM Studio, but basically you can use this same model in your local system. There are different pipelines that you can use this model that you can use to use this model, but I've shown you the basic and the most easy one and you can go ahead and give it a try. If you're facing any issues, please let me know in the comment section and I will be happy to resolve all the issues. Now, what you can do is you can go ahead to Hermos Agent and Deepseek V4 which is a new model. Go ahead and watch out this video. This is really exciting. See you there.