---
title: "All about Screen 🖥 command"
datePublished: Sun Jun 05 2022 18:46:29 GMT+0000 (Coordinated Universal Time)
cuid: clr2f3vpq000108jy6fkzcq0o
slug: all-about-screen-command
tags: linux, devops

---

Hey there everyone have you ever run a service and wondered why the hell this service does not have detached mode ( detached mode means a service which runs in background and does not freeze your terminal ) so this is the one stop solution for you

## What is screen command

You can assume screen command as a new screen for you inside terminal where can you create multiple virtual screen to run multiple services

This command is very useful if you are in server using ssh and want to run a service in background but service itself does not provide a detached mode. ( e.x. ElasticSearch )


If you have unix system ( linux or macos ) screen command should be available to you 

To check screen command is available to you or not just run 
```bash
screen -v
```
it it returns any version like this voila you have screen command installed.

![Image descroption](https://cdn.hashnode.com/res/hashnode/image/upload/v1704566615674/860c345d-6ef3-4529-b251-18644c03d17a.png)


Now let's have a look how it works 

You can create a screen with below command
```bash
screen -S SCREEN_NAME
```
it will create a screen put you into that screen
to create a screen without entering into it you can run
```bash
screen -dmS SCREEN_NAME
```
it will create a screen but it won't go into screen

2. Now that you have created a screen if you want to see a list of screen you have created you can use below command
```bash
screen -ls
```
it should give you the list of screens you have created!
[Screen Version](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d7q2igvnwbxtu4wykhu2.png)
 
3. Now that you have created and listed out screens you can enter into any screen by typing below command
```bash
screen -dR SCREEN_NAME
```
in case you can see your screen in ```screen -ls``` command but unable to enter it try to enter into screen by using full name of screen with pid.SCREEN_NAME

pid is id which you can see in screen -ls command 

4. Now that you can created, listed and entered into screen and did you stuff now you want to make sure it runs in background so to come out from screen and run in background you have to press ```CONTROL+A+D```
by pressing this you will come out of screen and it will run in background

5. How to delete a screen to delete a screen enter into the screen and press ```CONTROL+D``` it will terminate your screen and you will see an output like this

![Screen Terminating](https://cdn.hashnode.com/res/hashnode/image/upload/v1704566617015/222abc7c-b746-4326-a78c-74938d6d21b9.png)

So this is all basics about screen command which you have inside your system to know more about it type ```screen --help``` you will get all the options available there.

Thanks for reading!

