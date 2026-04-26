---
title: "UNLIMITED FREE Deepseek-V4 PRO AI Coder: THIS IS CRAZY!"
source: "https://www.youtube.com/watch?v=e5aud8zON8o"
author:
  - "[[AICodeKing]]"
published: 2026-04-26
created: 2026-04-26
description: "In this video, I'll be telling you about the new DeepSeek V4 Pro and DeepSeek V4 Flash models, and how you can try them for free through NVIDIA NIM APIs usin..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=e5aud8zON8o)

## Transcript

**0:02** · \[music\] Hi, welcome to another video.

**0:07** · So, DeepSeek V4 is now actually here.

**0:11** · And this time there are two models that matter for developers.

**0:14** · DeepSeek V4 Pro and DeepSeek V4 Flash.

**0:17** · And the really interesting part is that you can already try them through NVIDIA NIM APIs, basically for free through the NVIDIA API catalog.

**0:26** · So, if you want to test the new DeepSeek V4 Pro API or the faster DeepSeek V4 Flash API without setting up your own GPUs and without immediately paying per token through the official DeepSeek platform, this is one of the easiest ways to do it right now. Now, before we get too excited, I do want to be precise with the wording here.

**0:44** · NVIDIA describes this as free access to NIM API endpoints for prototyping and development through the NVIDIA developer program. So, for trying models, testing apps, coding workflows, and building demos, this is a really good free option. But it is still under NVIDIA's API trial and developer terms. So, don't think of it as an unlimited production backend that you can just throw thousands of real users at forever. For development though, this is kind of amazing. So, let's get right into it.

**1:10** · First, what are these models? DeepSeek V4 Pro is the big one. According to NVIDIA's model page, it is a mixture of experts model with 1.6 trillion total parameters and around 49 billion active parameters. It also supports up to a 1 million token context window, which is just huge. This is the model you would try for harder reasoning, coding, long context agents, tool use, document analysis, and basically anything where you want the strongest DeepSeek V4 experience. Then there is DeepSeek V4 Flash. This one is smaller with 284 billion total parameters and around 13 billion active parameters.

**1:41** · It still supports the same 1 million token context window, but it is designed to be faster and more efficient.

**1:48** · \[clears throat\] So, the simple way to think about it is this. Use V4 Pro when you want the best quality. Use V4 Flash when you want speed, cheaper inference, routing, summarization, chat, or lighter coding tasks. And honestly, this split makes a lot of sense. Not every task needs the 1.6 trillion parameter model. If you are just summarizing a file, generating a small utility script, routing a request, or doing a quick chat response, Flash may be the better option. But if you are asking it to work across a large codebase, reason through a hard bug, write a complex plan, or do agentic coding, then Pro is the one I would test first.

**2:19** · Now, the other important thing is that both of these are available as NVIDIA NIM endpoints. NIM stands for NVIDIA inference microservice. And in simple terms, it means NVIDIA is giving you a hosted API endpoint that runs the model on their GPU infrastructure while still exposing a normal developer friendly API. And the best part is that the API is OpenAI compatible. So, if your tool supports an OpenAI compatible provider, you can usually connect NVIDIA pretty easily.

**2:48** · The base URL is integrate.api.nvidia.com/v1. The chat completions endpoint is integrate.api.nvidia.com/v1/chat/completions. And the model names are deepseek-ai/deepseek-v4-pro and deepseek-ai/deepseek-v4-flash. So, don't confuse this with the official DeepSeek API names on DeepSeek's own API. The model names are deepseek-v4-pro and deepseek-v4-flash. On NVIDIA NIM, the model names include the provider prefix. So, they are deepseek-ai/deepseek-v4-pro and deepseek-ai/deepseek-v4-flash.

**3:23** · That detail matters because if you put the wrong model name into your tool, it may just fail or not show up. Now, let's talk about how to use it. First, go to build.nvidia.com. You can also use the filtered models page that I will put in the description, which shows the preview NIM models. Then search for DeepSeek V4. You should see DeepSeek V4 Pro and DeepSeek V4 Flash from DeepSeek AI.

**3:46** · Open the model page you want. If NVIDIA shows you a third-party model warning, just read it and continue. Once you're on the model page, you can actually test the model directly in the browser first.

**3:55** · This is useful because before setting anything up in your code editor or terminal, you can just type a prompt and see if the model is working for your account. So, for example, you can open DeepSeek V4 Flash and ask it to summarize a long document or open DeepSeek V4 Pro and ask it to plan a coding task. If that works, then the next step is getting the API key. On the model page, click get API key. If you do not have an NVIDIA account, it will ask you to sign in or create one.

**4:20** · This also joins you to the NVIDIA developer program, which is what enables the free developer access. Then copy the API key and save it somewhere safe. That is the main thing you need. Now, if you want to use it from code, the easiest way is the OpenAI SDK. Install the OpenAI package in your project. Then create the client with the base URL set to integrate.api.nvidia.com/v1. Use your NVIDIA API key as the API key.

**4:46** · Then call chat completions with the model set to deepseek-ai/deepseek-v4-pro or deepseek-ai/deepseek-v4-flash. And that is basically it. You do not need a special NVIDIA-only SDK for the basic chat API. You do not need to learn a completely new format. You can use the same messages structure that you already use with OpenAI compatible APIs with a system message, user message, and assistant responses.

**5:15** · This is why I like this kind of endpoint. The model may be different, the provider may be different, but the integration pattern is familiar. Now, there is one very important parameter here, and that is reasoning effort. NVIDIA's docs show that the DeepSeek V4 endpoints support reasoning effort values. You can set reasoning effort to none, high, or max. None disables thinking and gives you the faster non-thinking mode.

**5:39** · High gives you the normal reasoning mode and is the default. Max gives you the strongest reasoning mode, but it will usually be slower and more expensive in terms of tokens. So, for DeepSeek V4 Flash, I would usually try none or high. For DeepSeek V4 Pro, I would try high for normal coding and max for the really hard tasks.

**5:57** · This is actually a very useful setup because you don't have to switch to a totally different model just to change the behavior. You can use the same model with a different reasoning effort depending on the task. Now, small caveat here.

**6:08** · DeepSeek's own API docs talk about a massive maximum output length, but NVIDIA's NIM endpoint currently documents max tokens up to 16,384 on these V4 endpoints. So, do not assume that every host exposes the exact same limits just because the underlying model supports huge context. The model has a 1 million token context window, which is very impressive, but your actual tool, endpoint, account, and request settings still matter.

**6:34** · This is especially important for AI coding tools because some tools do not send the full repository anyway. They chunk files, summarize context, or use their own prompt limits. So, think of the 1 million context as a capability of the model family, not a promise that every tool will magically use one 1 million tokens perfectly.

**6:53** · Now, let's talk about using it in coding tools. If you use Codium CLI, this is very simple. Open Codium CLI, run {slash} connect, choose NVIDIA, and paste your NVIDIA API key. Then run {slash} models and select DeepSeek V4 Pro or DeepSeek V4 Flash if it is available in the model list. That is the cleanest route. And this is basically the same idea that I showed in my previous NVIDIA NIM free models video.

**7:16** · You connect NVIDIA once and then you can switch between the models that NVIDIA exposes through the catalog. Now, if you use OpenCode, the same general idea applies. Connect the NVIDIA provider, paste the key, and choose the model. If the built-in NVIDIA provider in your tool has not refreshed the model list yet, then use the OpenAI compatible route manually. Set the base URL to integrate.api.nvidia.com/v1. Set the API key to your NVIDIA key.

**7:42** · Set the model to deepseek-ai/deepseek-v4-pro or deepseek-ai/deepseek-v4-flash. This same approach should also work in tools like Kite, RueCode, Cursor, Aider, through Light LLM, and other apps that support custom OpenAI compatible providers.

**8:00** · API key, model name, that is it. Now, how would I actually use these models?

**8:06** · For V4 Flash, I would use it for fast tasks. For example, quick repo explanations, small code edits, summarizing docs, writing tests for a simple function, generating commit messages, extracting information from long text, or acting as a router model before sending only the hard tasks to Pro. Flash is the model I would keep around when I want a quick answer and I do not need the absolute best reasoning.

**8:28** · For V4 Pro, I would use it for proper agentic coding. Ask it to inspect a project, find the architecture, understand the current patterns, implement a feature, run tests, and then explain what changed. Or ask it to debug a hard issue where the answer is not obvious from one file. Or ask it to work with a lot of context like a long design doc, API docs, and multiple source files. That is where the big model should make more sense. And if you want to test the difference yourself, do not just ask one random question. Try the same real workflow with both models. Ask both to implement the same small feature. Ask both to fix the same bug.

**9:01** · Ask both to summarize the same long document. Then compare speed, cost, correctness, and how much cleanup you need afterward. That is much more useful than just asking one benchmark riddle and declaring a winner. Now, why is this release interesting?

**9:13** · Because DeepSeek has always been one of the most important companies for people who care about cheaper and more OpenAI models. V3 and R1 changed the conversation a lot. Then V3.2 made the long context and sparse attention side more interesting. And now V4 is clearly going after long context agents, coding, tool use, and serious reasoning workflows.

**9:33** · NVIDIA hosting it through NIM makes it even easier to test because you do not need to wait for every coding tool to add a dedicated DeepSeek V4 integration.

**9:41** · If the tool supports OpenAI compatible endpoints, you can usually wire it in yourself. That is the whole point. So, in summary, here is the setup. Go to build.nvidia.com, search for DeepSeek V4 Pro or DeepSeek V4 Flash. Open the model page, click get API key, copy your Nvidia API key, then use integrate.api.nvidia.com/v1 as the base URL. Use deepseekai/deepseekv4pro for the strongest model. Use deepseekai/deepseekv4flash for the faster model.

**10:07** · And if your tool supports reasoning effort, use none for fast non-thinking mode, high for normal reasoning, and max for the hardest tasks. That is all you really need. This is a really good option for students, developers, and anyone who wants to test the new deepseekv4 models without immediately paying for every experiment.

**10:23** · Just remember the caveat. Free developer API access is amazing, but model availability, rate limits, and terms can change. So, use it for testing, prototyping, and coding experiments. And if you're building something serious for production, read the actual Nvidia terms and plan accordingly. Still, for what it is, this is pretty great. You get deepseekv4 pro and flash through an OpenAI compatible API with a free developer access path hosted on Nvidia infrastructure and usable in real coding tools. That is chef's kiss.

**10:52** · Overall, it's pretty cool. Anyway, let me know your thoughts in the comments. If you like this video, consider donating \[music\] through the super thanks option, or becoming a member by clicking the join button. Also, give this video \[music\] a thumbs up and subscribe to my channel. I'll see you in the next one. Until then, bye.