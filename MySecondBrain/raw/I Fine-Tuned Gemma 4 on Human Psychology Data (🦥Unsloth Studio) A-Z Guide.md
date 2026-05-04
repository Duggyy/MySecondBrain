---
title: "I Fine-Tuned Gemma 4 on Human Psychology Data (🦥Unsloth Studio) [A-Z Guide]"
source: "https://www.youtube.com/watch?v=I8IBvpCWQnM"
author:
  - "[[Prompt Engineer]]"
published: 2026-04-07
created: 2026-05-01
description: "In this video, I show how to fine-tune Gemma 4 using Unsloth Studio with the ATOMIC dataset to improve human-like reasoning.ATOMIC is a large commonsense reasoning dataset that teaches AI how humans"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=I8IBvpCWQnM)

In this video, I show how to fine-tune Gemma 4 using Unsloth Studio with the ATOMIC dataset to improve human-like reasoning.  
  
ATOMIC is a large commonsense reasoning dataset that teaches AI how humans think, react, and make decisions in everyday situations. Instead of just memorizing facts, the model learns cause-effect relationships such as intentions, reactions, emotions, and outcomes.  
  
Best GPU: https://get.runpod.io/pe48  
Unsloth Studio Docs: https://unsloth.ai/docs/new/studio  
Install Unsloth Studio: https://unsloth.ai/docs/new/studio/install#linux-and-wsl  
Dataset: https://huggingface.co/datasets/allenai/atomic  
Dataset Setup Code: https://github.com/PromptEngineer48/Atomic-Dataset  
HuggingFace tokens: https://huggingface.co/settings/tokens  
Finetuned Model: https://huggingface.co/Prompt48/unsloth\_gemma\_4-E4B-it\_FT\_Emotion  
  
Unsloth Studio makes the process simple with a no-code interface that allows fast and efficient fine-tuning.  
  
🔗 My Links  
☕ Support me: https://ko-fi.com/promptengineer  
📱 Patreon: https://www.patreon.com/PromptEngineer975  
📞 Book a Call: https://calendly.com/prompt-engineer48/call  
💀 GitHub: https://github.com/PromptEngineer48  
🔖 Twitter/X: https://twitter.com/prompt48  
  
#UnslothAI #UnslothStudio #LLM #AtomicDataset #FineTuning #LocalAI #RunPod #OpenSourceAI #MachineLearning #AITutorial #NoCodeAI #LLMTraining #GGUF #Qwen #llama  
  
Timeline:  
0:00 Intro  
1:25 Dataset  
5:31 Pre-Demo  
6:22 Set up Runpod  
7:29 Installation Unsloth  
8:53 Hyperparameters Settings  
10:22 Training  
11:20 Push to Hub  
12:53 Comparison  
15:06 Summary

## Transcript

### Intro

**0:00** · Okay, just yesterday I posted a video on fine-tuning Gemma 4 using Unsloth Studio and people really demanded a slower and a longer version of how everything is done. So, I went ahead and searched for the best dataset that will be fun to fine-tune the model. Dataset that I stumbled upon is this Atomic dataset which is really cool. We'll discuss about this. We are going to use Unsloth Studio. Basically, it's an easy-to-use UI to get your recipes, to get your data, and to fine-tune and export your models. We are going to use RunPod because I don't have that GPU on my system. And this is Unsloth Studio.

**0:31** · Just this command and everything will be ready for you to start. Now, the first thing that I went ahead and tried to look was a good dataset to train a model on. And this particular dataset, which is this Atomic dataset, I found it really interesting because this talks about social intelligence and if-then logic, reasoning, and common sense. It's really interesting. It has tons of lines, 877k lines to be specific. And I've just used 2,000 of those lines to train my model. And you can see the model training is was ran you know ran pretty good.

**1:01** · Look at the history, you can see this is the training and you can see the training loss. It was reducing consistently. And all the other parameters were really good. So, when I tested it out as well, it was performing well. So, we are going to see from the start how to get started with everything that is fine-tune one of the Gemma 4 models that is trending as of now. So, Atomic dataset. This is essentially a dataset which has these nine types of reasoning relations. So, if I open up the dataset, so if you go to the dataset, so this is the dataset which is available on Hugging Face.

### Dataset

**1:30** · So, if you download this Atomic data TGZ file and you put it in a folder, so this is the folder. And then you run this command, we make a new directory called data, and you can just use this to export the data to the data directory that we have made.

**1:44** · So, inside the data directory, you'll find all these after it extracts. So, first of all, we have this beautiful paper. So, it's not some random database or dataset that we're using, but it's really good dataset and especially a paper is there as well. And I've gone through the paper very quickly and I was able to find a very beautiful things here. So, for example, we have this incident of X repels Y's attacks.

**2:04** · Then what are the attributes of X? What could be the causes for X? What could be the effects on X? What could be the effects on Y? So, you know, it is asking the LLM to think not in terms of an LLM and get a fixed reply, but think in terms of human and have different perception and try to broaden the horizon of what you're thinking. So, if you go to this dataset, so let's open this TRN, which is the train dataset that we'll be using. This is the DV or evaluation dataset. And this will be the test dataset. So, let's open the TRN training dataset. Here, you can see that we have this event here.

**2:34** · So, let's say the person X uses person X's something to obtain. So, what will be the effect?

**2:41** · Or you can go ahead to this relationship here. So, when we say effect, so what happens after the action? So, if a person X uses its something to obtain something, then what will be the effect?

**2:50** · What will be the reaction? Okay. So, you can see this is the reaction. So, what will be the want? So, what someone wants next? So, what does he want next? What can we give the attribute? What will be the effect on X? What is the What is the intent of X? What will he need after that? So, all these things, whenever we see X in front of for example X attribute, so this is related to the X person, the person who is doing the work. And we have this O effect that is the other party that we have effect. So, essentially, the dataset was created, you know, this particular line for example.

**3:17** · So, we gave the event to a real human being and the real human being just went ahead and said something, inferred something, and then we just plotted or inserted the inferred and whatever person said here. So, each of these lines were formed of the human data. The same question can have different interpretations by different people. So, this is a very vague dataset, you know, very broad dataset to fine-tune a model.

**3:42** · I know what you're thinking, but what we have done is we need to extract from this clumsy thing, we need to make it a beautiful one. So, for that, I have used AI and written two scripts. First is the prepare fine-tune and another one is fine-tune dev. So, prepare fine-tune train So, this is using you know, it's using the different dimensions that we saw on the Excel here on the top. So, it's using those dimensions and whenever we see that for example, if you work on this fourth one, and whenever we see that we have in the reaction, so use that as the reaction.

**4:13** · We use the first one, the reaction one, and intent one, and the react one. So, use this and make one just online, which will be apparent if you see this output. So, once you run this train, so if you run this train, this will generate 2,000 samples of Atomic fine-tune train JSONL file. And if you look at this JSONL file, this will be more clear. So, what do you have here? Here, we have put a system prompt till here, which is you are an expert in social common sense reasoning.

**4:40** · A given an event description and a specific question, provide a clear and accurate reason based on likely human interactions, needs, and reactions. So, then what we do is went ahead and put in the user. What does the user say? We have this entire thing. So, event person puts the dash into operation. And question what does person X need before this? So, we have this question and the answer is to tell people about the plan.

**5:04** · We have three things. We need the system prompt, we need what the user says, and the assistant said. So, we have arranged this dataset in this format. Three columns. First is system, then is user, and then is assistant. Now, if you are wondering why we have a dash here, it's because we don't want it to relate to any particular word. Meaning, if I show you the fine-tune model, that will be clear. So, if I go back to the fine-tune model that we have, so go to chat here.

**5:27** · And we have already loaded the fine-tune model. And if I take one example from here. Let me take one example, this one till here. So, if we have this question for example, person X puts the dash into operation. So, if I say plan, what does person X need before this? What do you think? Just one word answer or one phrase answer. So, it needs to create the plan you know, before this. So, if you put a different word, he puts the money into operation. Then what do you need? To get the money. Okay. So, it's not thinking it's some kind of rigid way, but it has broadened its horizon.

### Pre-Demo

**5:56** · And you can see I'm really liking with just 2,000 samples of data, I was able to fine-tune this. This is really great.

**6:02** · And I put this model here. You can go ahead and use this model. So, for our service, I'm going to use RunPod. And in RunPod, I've used A100 here. So, if you go to deploy, if you go to deployment, before that you need to create an account. So, if I have pasted the link in the description. And if you go to the link in the description, you will see this that if you sign in for the first time, you will get $5 to $500 off bonus when you recharge for $10 for the first time. So, once you have that account, you can see your balance on the top right here. And on the pod section, if you go on the left, then you can see all these GPUs.

### Set up Runpod

**6:34** · The ones that I've used was A100. So, I can go to A100 here. And then I can just click on edit, increase this to let's say 500 GB, and put this to zero, and put some ports here, 8889, then 88 8005, and 8006 just in case, and set overrides, and select this volume disk to zero because we don't need, and then deploy on demand.

**6:55** · So, once you deploy on demand, you will be able to see some sort of like this.

**6:59** · And if you click on the pod, you'll see the options to connect. So, in the connect options, I go to Jupyter Lab. If you go to Jupyter Lab, you'll be brought here. And after that, you can go to the terminal here and run this simple command, which is the this command. So, we copy this and paste it here. So, what I've done is I recorded the entire process, so I would not have to repeat everything. So, I'm going to show you here. So, what I've done is I can start the pod. You can see that the pod is starting up. And then we can go to Jupyter Lab here. So, the Jupyter Lab opens up, then we go ahead and go to the terminal, put in the command here, which is this command, Unsloth install.

### Installation Unsloth

**7:30** · And then this is going to install everything. You can see the installation going on, and it will be ready in just a few minutes. Then you can see that 8889 port is the one in which Unsloth Studio is running. So, if you go back to RunPod, and then you go and click this 8889, you will be brought to this. So, set up a password, anything just eight characters minimum. And then you say okay. I'm going to let's say skip the onboarding, and then I'm going to say next, next. And then just press okay, change the color mode. And here, I want to select a model.

**8:00** · Let's select Gemma 4E4BIT.

**8:04** · And then need a database. So, I click that dataset that I prepared. So, if you go back, you can see that I upload the dataset of this train.jsonl. This is going to upload the data dataset. And once this is uploaded, you can go ahead and view the dataset. So, the dataset uploading is done. And then you can go ahead and view the dataset. So, you can see that we have the system prompt, we have the user, and we have the assistant. So, you can analyze the dataset here. If we need to change AI assist, so AI assist couldn't find anything different. We are doing the right thing. So, assistant is assistant, user is user, and system is assistant.

**8:35** · Then you can put in the evaluation dataset as well. So, this dev.jsonl. So, that was created using this.

**8:41** · I've already given the code. I'll paste in the code here. So, if you run this dev.py file, this will create the dev.jsonl file. So, that's one thing. So, having load the dataset, next we go ahead and set up the different parameters. So, the first parameter that discuss the parameters.

### Hyperparameters Settings

**8:57** · So, the first thing is the epochs.

**9:00** · Epochs are putting as three. Epochs means the number of times the model sees the entire dataset. So, we're putting three times, so the model sees the entire dataset three times. Then then we have the context length. This is the maximum maximum number of tokens the model reads per training example. Then we have the learning rate. So, this essentially controls how strongly the model weights change every step. Then we have these LoRA settings. So, because we're using QLoRA, we can set this rank of LoRA, LoRA rank. This this controls you know, how much the model is allowed to change during fine-tuning. We have alpha.

**9:31** · This is a scaling factor so that we get the total or effective rank that will be like the rank into or multiplied by alpha. We're putting 16 and we're putting alpha as 32 total as scaling factor, which means after multiplication of two, we get 32. Dropout it regularizes the to prevent LoRA weights from overfitting you know, small datasets.

**9:51** · So, next these target modules we are going to use and uh take all the target modules and enable Laura training hyper parameters, optimization we're using Adam's cosine batch size putting eight gradient accumulation as four and that'll give you an effective batch size of 32. So, the and weight decay is 0.05. Uh we're putting the warm-up steps of something like, you know, five is okay. Uh save steps of 30 and evaluation steps of 50. And uh using enable packing here. I think uh we are ready to go ahead and uh just click start training.

**10:21** · So, this will start up your training pipeline here. So, I can see that we are preparing everything. And now I can just, you know, just speed up everything. So, I can see that it's applying the chat template uh to all the data. It's done. Then we have 2,000 samples already. It's waiting for the first step. In the previous video, people complained I was going too fast.

### Training

**10:36** · So, in this video, I'm going to go slow.

**10:38** · So, configure Laura parameters. We have uh tokenization being done. So, almost 100% now. It's tokenizing the text.

**10:44** · Waiting for the first step, starting the training. And I can see that the training is going on. And the loss decreases so fast. I really love it. And you can see that it's really good. You can see the utilization.

**10:53** · Uh we can see the temperature. I can see the VRAM, the power consumption, and the number of steps here. Uh we can see that the completion percentage here using QLoRA. There's a model gradient norm, learning rate, loss. It's really good.

**11:05** · So, 100% is complete. And then what we can do is uh we can go ahead and basically export the model here. So, you can see uh the other parameters. Let's click on export model. And uh now we need to select the training run that we had made basically and the checkpoint.

**11:18** · So, this is the checkpoint. The final checkpoint is the E uh 4B IT, which is uh the top one, which has the minimum loss. Merge models uh we want to push to hub. My username is 48. So, if you go to this hugging face uh and just confirm my password here. And then you can just uh invalidate and refresh and get this access token. Just put it here. And the model name, just select the model name Unsloth Gemma 4E4 IT fine-tuning. I'm going to uh put one uh emotion as well.

### Push to Hub

**11:44** · So, exporting this and you can see that here you'll be able to see uh that everything is being made ready. And uh the model is being pushed as we speak.

**11:52** · Okay. So, it's pushing the model.

**11:53** · Wonderful. Okay. So, from now basically I can go live. Uh this was a recording of the recording that we're listening.

**11:59** · But from now I can go live. So, this is uh the access token. This is visible to you, which means uh I have to delete it, which is the best thing to do. And then uh now what I can do is I can go back to Unsloth and really test it out. So, when we put uh if you go to this chat section and if we go to new chat and select the older model, which is the Unsloth Gemma 4B uh you know, 4 Gemma 4E4B IT instruction tuned, which is not our model, which is the original model. Then uh putting the same system prompt here.

**12:28** · You can put the system prompt somewhere here. If you go here. So, I put the basically the same system prompt uh that we were trying out here so that everything is similar. So, we have put this system prompt. Sorry. We have put this system prompt uh till the reaction here. And basically this system prompt will be used for both the models. And uh this is loaded as you can see. Now, if I go ahead and take any example, for example, uh this example. Now, you know, we're doing fine-tuning to get a specific type of output. So, person X plays uh race in the economy. Uh what did person X need before this? Okay.

### Comparison

**13:01** · So, if I say generate based on social common sense reasoning. So, it gives all the type of output that you normally expect from an LLM. So, this is the difference, you know. You can see the difference here. So, it's it goes on and on uh looking at different examples. I wouldn't say that this is not responding or this is bad, but we needed a different output and therefore we fine-tuned it. So, we go to uh fine-tune section. This is our fine-tuned model uh and we are switching the model here. So, it's loading the model onto memory and uh will put the same question here again. Uh start up a new chat. Okay.

**13:32** · So, we can see that this model is loaded, the new one. Now, if I give this question, person X plays a race in the economy. What did person X need before this? I can see the output here. So, you can see that to learn the rules of the race. So, it's very particular. It's very clear and it doesn't have multiple options to choose from because it now understands the context just like human being. So, person X lays. Okay, let's go ahead and look at another example. So, for example, this one. Let's see. Uh person X, we call it event. Person X kills human, let's say, for food. What is the effect on person X?

**14:03** · They're hunted by authorities. Really good. Uh kills animals for food. What is the effect? They're respected by the community. Okay. I don't know about that, but you get the idea. This is how you fine-tune everything. So, in summary, what you've done is we've used RunPod to start up an A100 and then start up. So, we put this example. So, we start up this one. So, we next we select this fine-tuned model and then we start up a new chat. And now let's see uh if I can get any other example here.

**14:31** · So, let's say this one. Person X connects uh the dash together. Connects a let's say twins together. What is the effect on person X? Happy? I don't know.

**14:40** · It's not connected to the twin. Okay.

**14:42** · Connects the dots together. Let's see.

**14:44** · Really good. You can see uh the dots together. It has completed the puzzle.

**14:48** · So, it understands that grammar uh from its original pre-training model. And also it understands the nuance that uh it was trained on using the fine-tuning process. So, it has both the pre-training and the fine-tuning things.

**15:01** · Really good. So, we have uh selected the parameters correctly. So, in summary, what you've done in this video is we wanted to fine-tune our model on this atomic data set, which is really if-then reasoning data set, which is really interesting. Uh so, we used that data set. Uh we downloaded that data set. We converted that to our required format such as system, user, and assistant. And once we have that, we started up RunPod, started up A100, and then started up Unsloth Studio. And then we went to studio. And here we selected our model.

### Summary

**15:33** · And here we selected our model here. We used QLoRA and then loaded our data set here. So, once we loaded the data set, you can see that we have these three columns as required. So, this is the system prompt. This is what we will put in this format. We also need the system prompt. Whenever you want to use this model that I made, you need to have the system prompt. You need to put the user uh input in this structure. Then you will get this. Otherwise, you won't get it. Because we are fine-tuning it. So, we need to follow that particular process and particular input style.

**15:59** · So, we get the model and then we export this model and now it's sitting on my hugging face repo. You can go ahead and uh check this out. Download this model. It's a 16 GB model. Use this. But you can use this entire process to do fine-tuning for anything. So, if you want to make an uncensored model, you're going to collect data sets and just arrange in uh arrange those in this format that I've shown you. So, if you have a data set, you arrange in this format. You put in the system prompt, put in the question, and put in the answer. So, if you want me to fine-tune on any other data set, I will be happy. But this is what I found.

**16:33** · This is the most, you know, interesting as of till date that I found. This data set is really interesting. So, go ahead and check this out. Go ahead and use RunPod and uh do the fine-tuning. I will see you in this next one. You can check out the other videos on Unsloth as well.

**16:44** · Go ahead and check this out. I'll link uh on at the end of this video, Unsloth Studio fine-tuning. And subscribe to my channel so that you can see other contents that I find amazing and I think you will like them, too. Thank you and have a nice day.