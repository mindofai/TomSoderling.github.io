---
published: true
layout: post
title: Playing Audio and Video for Xamarin.Forms
author: mindofai
date: 2017-03-30 12:00
tags: [UWP, Android, iOS, Media, Video, Audio MediaElement, Xamarin. Forms, InTheHand.Forms]
---

My experience working with video and audio streaming in Xamarin.Forms. We had this project where we used Xamarin.Forms for developing a cross-platform chatbot (Bot Framework + LUIS.ai) application. (btw, this was my first Xamarin.Forms project) We needed to play a video and I thought it will be really easy, because in UWP development, you can just use MediaElement. I'VE NEVER BEEN SO WRONG IN MY LIFE. It's so painful, especially with UWP. We searched for other workarounds and stuff that we can use for playing videos, but we couldn't find anything. Yeah, I know only a few uses UWP apps, but still, Xamarin.Forms should've atleast created a control for it.

I've had that problem months ago, but it looks like I'm going to encounter it again. So, I searched for workarounds, thinking that there might be a NuGet package out there that I can use. Luckily, I found one! We can now play videos/audios with Xamarin.Forms using [**InTheHand.Forms**](https://github.com/inthehand/InTheHand.Forms) which can be used for Android, iOs, and ofcourse UWP. If you have used the UWP's MediaElement , this will be easy for you. Follow these steps:

1. To use this, first, you need to install [this NuGet package](https://www.nuget.org/packages/inthehand.forms) to the PCL and to all three platform-specific projects (Android, iOS, and UWP) or whichever you have. It will not show any error if you only added the package in PCL and run it, so it'll hard for you to debug this if you forgot to install it to your platform-specific projects.

2. After the installation of package, the next thing you'll do is to open the XAML page where you want to play a video and add this namespace to your XAML:


```xaml
xmlns:forms="clr-namespace:InTheHand.Forms;assembly=InTheHand.Forms"
```