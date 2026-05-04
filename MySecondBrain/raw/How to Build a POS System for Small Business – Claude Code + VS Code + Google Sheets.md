---
title: "How to Build a POS System for Small Business – Claude Code + VS Code + Google Sheets"
source: "https://www.youtube.com/watch?v=i9kOEIDyvPw"
author:
  - "[[Mohammad Rameez Imdad]]"
published: 2026-04-30
created: 2026-05-03
description: "In this tutorial, I'll show you how to build a complete POS System for Small Business from scratch — using Claude Code, Visual Studio Code, Google Apps Scrip..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=i9kOEIDyvPw)

## Transcript

**0:00** · What if I told you I built this entire wood raiding point of sale system with login role based access, OTP password reset, A4 invoices and a full inventory dashboard in just few minutes using one cloud code prompt and Google apps skip for free hosting. No servers, no database, no subscriptions. Stick with me. I will show you the prompt, the setup and the live system how you can do that. I am Ramse and on this channel I build real business systems with artificial intelligence.

**0:30** · Today we are building a complete point of sales system for a wood trading business. But the same blueprint works for any small business, garments, grocery, hardware, anything. The total cost is zero. No hosting fees, no API cost, just a Google account. Let me show you what we are going to build today. Then I will hand you the exact prompt so you can try it yourself. and watch this video complete.

**0:58** · So I will explain you everything step by step. Okay, let's get started. Now we will check out that how we can write a code. So for that we need to open the visual studio code and once we open our visual studio code here you will see this kind of interference and you just simply go to your extension sections.

**1:13** · Okay. And if you don't have the Visual Studio Code, you will just simply go to your Chrome browser and simply search it here the Visual Studio Code. Okay. So that is your Visual Studio Code. go to this particular website and click on the download for Windows and that's it. And uh now let's go back to our visual studio codes. So there is the extension.

**1:30** · You just simply need to search it here the cloud code. So when you search it here the cloud code you will see the extension in the list. So this is a cloud code. You will see the option the install. Just simply hit the install button and that's it. Now what you need to do you just simply go to here and click on this open folder. Go to your desktop and create a new folder. So let take example I am going to create a folder for our point of sale system and then simply select this particular folder. So when I select this folder now you can easily able to see here the folder is selected and here you will see a cloud icon.

**2:01** · Just simply press on it here and login with your cloud account and then that's it. So this is the thing. Now we need to enter our prompt.

**2:10** · So there is a prompt. I will leave the link in the description. Just simply copy this prompt and paste it here. And now the cloud do everything for you.

**2:17** · Click on this send. So when you click on this send it will examine and it will writing a code for you and it will automatically create the code.js and index do file html for you. Okay. So once it's completed we will just simply copy paste the code and go to our Google sheets and paste it there and then we will check out that is it really working or not. So it have created the code and asked for the permission. We just simply click on this yes allow edits in this session.

**2:44** · And now you can easily able to see here it have writing the code code.js and the file is here successfully. So we will wait for the index.html and then we will simply copy and paste into our Google sheets and check out them. Well the index html is also created. Now let's test it out. So we just simply go to our chrome browser and just simply enter here sheet dot new and uh then we need to pass on this extension and click on this app script.

**3:12** · So when I click on this appcript as of now you can able to see here this is a appcript editor interference. So we need to copy paste our code. So this is a code.js. We just go back to our code and just simply copy the code js and paste it here. And then we just simply click on this plus and add a file and click on this HTML. And now we need to enter here index. Let's go back to our Visual Studio Code and copy our index html and paste it here. So now all set we just simply click on this save. Okay.

**3:42** · And now let's press on this deploy and uh click on this new deployment. So when I click on this new deployment, you will see this interference. Simply select this setting icon web application who has access anyone and click on this deploy and authorize access. So once we authorize the access it will provide us a public web app URL. Just simply click on this advanced go to untitled project unsave select all and click on this continue.

**4:09** · So now we will see the web app URL and then we will set up the demo data in our Google sheet as well. Okay.

**4:17** · So this is updating the deployment link and that is the link what we can use to access our web application. Okay, you understand them trading point of sales system. Now let's go back to our code.js. Here you will see a option function names. So we just simply search a setup demo data and now simply click on this run. So when I click on this run now you will be able to see it first created a temp setup file. Then it will delete all the files and then it will create all the files with demo data automatically. Okay, understand them.

**4:48** · This is the setup demo data function. It is available in all of our previous web applications. Okay. So now let's go to the users admin at the rate demo and we just simply paste it here our username and password and click on this login. So when I click on this login as of now you can easily able to see here this is the dashboard where you can take the overview of the complete system and in this system we have the multiple roles.

**5:13** · Okay what kind of roles we have the admin the manager the cashier and the warehouse staff. So now let's check it out how it will work. So this is a dashboard where you can take uh check out the customer has overdue payment and when we click on this here and as of now you can able to see here it is the due reminder sections and we can check it out the dual reminders we have implemented the SWR technology.

**5:34** · So once you uh go to any section it will load in your local storage and then when you come back to that particular section it will load instantly and update the data in the background silently. So this is a point of sales system where we just simply select a customer and if we need to add a customer we just simply click on this new and create a new customer and then that customer will automatically appeared in the dropdown.

**5:59** · We just simply select it here and now that is our items we just simply search it here as per our own needs. If we if you don't want to search just simply select it here this product available two quantity we just simply select it here one and now one is remaining. Okay, understand them. And if we select it here now, you will see there is only one quantity remaining. We have added them.

**6:21** · Now in the available wood that is not shown. So the customer have paid you full amount, half amount and the non- amount you just simply select it here or any custom amount you can simply enter it here. The payment method they have used Bcash, bank cash, check etc. And if you want to complete the sale you just simply click on this complete sale.

**6:39** · Otherwise if you want to take a print you can take a print. And if you want to save a image received, you can simply save it here. I just simply click on this complete sale. So when I click on this complete sale, as of now, you can able to see it's completing the sale.

**6:52** · And if you want to take a print of A4 size, you can take as well. Otherwise, you can save image or thermal print as well. Now let's go to the sales list. In the sales list, all the sales we have made is available. And if you want to make a duplicate sale for this particular customer and the same wood, you just simply click on this here duplicate sale. And if you want to take a print, you can simply take a print from here. And if you want to edit them, you can edit them. And if you want to delete, you can delete it here.

**7:18** · Now the thing is that there is a receive payment option that is a customer to and they have purchased this amount of uh items from us. They have paid zero and that is the amount. Just simply click on this receive payment. And now what we need to do, we need to enter the amount here.

**7:35** · Let take example that is the 11550 cash amount optional and debt optional and click \[clears throat\] on this record payment. Okay. Uh 11550 and simply click on this record payment. So when I click on this record payment now you can easily able to see here it's going to be saved successfully. And once it says have saved successfully you can easily able to see here the paid amount is this and the due is this. Okay understand them. And that is our receive payment.

**8:00** · That is our customers list where we can add the customer, edit the customer, delete the customer or even block or unblock the customer and check out the ledger as well. Let take example that is our customer. Do we just simply click on this customer ledger and now we will see the complete details of this particular customer. We have paid the 11 11,500 right now 50 is due and that is the pending and etc. Now that is our wood inventory section. In the wood inventory section, if you have purchased the wood from the vendor, you just simply click on this add wood and enter the details.

**8:32** · And if you want to add the wood image, you can simply add it here. And if you don't want to add the information manually, simply click on this bulk import. Select what kind of wood. Okay.

**8:42** · So this is a carbon raw wood that is the buy rate that is the sell rate. Just simply download the CSV template, open it and enter your information and then simply select it here. That particular file and import. So when you click on this import the duplicate data will not be added and the unduplicate data which is not available is import complete successfully. So you can easily able to see here that is our purchase section where you can add the purchase, edit the purchase or delete the purchases as well. Okay, understand them.

**9:09** · And that is our supplier sections where you can add supplier, edit supplier or delete supplier. And the same thing is that you can also check the supplier ledger as well. Okay, understand them. Yes, you understand them. And now this is a payment section where you can check the customer payments and the supplier payments list easily and that is a good feature I think. Okay, so this is the thing and you can apply the filters.

**9:34** · That is our expense section where you can add the expenses for your businesses and you can keep track recording. Few reminders you already know that is the report section where you can check the profit loss report, sales summary report, stock aging report, customer analysis and the car shipment and PL reports. Okay. Now this is a subcategories cars where you can add the subcategories of the car sections. This that is the category section where you can add the category and in the subcategories you can add the subcategory for this particular section.

**10:03** · Okay. And that is again the bulk import.

**10:05** · Uh we have added the separate section for import different things that is our user management where you can add the user, edit the user, update the user or delete the user. And now the last thing is that that is our settings sections where you can update the application name, the phone number and the address and the currency symbol of the overall web application. And that is the formula for wood calculation. And now that is the thing that is our activity logs to keep record of the complete system login activity. And this is my account section where you can check out your account and edit profile and also you can change the password. Now you can check it here.

**10:39** · There is a user roles and permission table. I have explained you complete admin side. But if you want that you want to check manager what manager can do, what cashier can do, what warehouse warehouse can do. Let me uh give you this table inside the about app section.

**10:55** · So view dashboard all users can do view all users only admin can see and the same like that you can simply visualize them and lastly if you want any kind of customized project for your businesses professionally and you want a and you want a highly enterprise level web applications so it that will solve definitely your business problems you can contact us and we will create a very good projects for you. So we thank you very much.

**11:20** · Subscribe to our channel if you like this video and if you want that I will create this kind of more videos you just simply subscribe and leave the comments that uh you want this kind of videos so we will make it. Thank you very much. Take care.