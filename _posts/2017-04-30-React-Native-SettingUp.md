---
layout: post
title: 'Writing a simple mobile app with React-Native Part 1. Setting Up'
excerpt: App development for both Android and iOS has evolved during the past years, let's check a very popular framework for writing both in one go...React-Native.  in this first part where we cover setting up.
permalink: /ReactNativePt1
smlogo: ReactNative.png
---
![react](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/reactLogo.png)

<h3 class="fancy">Preface</h3>

I think we are currently in a weird and wonderful transitional moment in web and mobile development, there is an excess of riches of easy and complex tools and frameworks for each one, there is also the promise that in the near future progressive apps will run everywhere and bridge the gap( I've heard this promise before, so I am not biting, but I am still hopeful ). For now, if you are or have been a web developer and have avoided coding for mobile apps ( <i>I've personally just written a few Java apps for Android </i>),want to do something more than a responsive web page or want a relatively easy way into app development, this post is for you.

<b>The Game Plan:</b>... <i>Always have a plan.</i>

We will be learning and using React-Native to make a simple mobile app for both Android and iOS, first I'd like to deal with setting up, doing a quick overview of whats possible, and then creating a simple app. Importantly this app will be have a backend, albeit a simple one.

<div class ="note"> <b>Huge Note: So why use React-Native ?</b>
<br />
Let's try a quick overview of the current (mid 2017) state of mobile app development, let's say a client asks you to make an App for both iOS (iphones, ipads) and Android Devices, what are your choices ? <br /><br />

<p>You could write an iOS app in Swift or Objective C and then the same App for Android in Java or C++, but chances are as a web developer you might not have experience in those languages.</p>

<p>Another option is to use a hybrid approach in which you write your code once ( in HTML,Javascript and related technologies) and a framework then produces iOS and Android Apps.</p>

<p>There are a few tradeoffs in choosing in between this hybrid <i>(or Native depending how close it is to a native implementation) </i> approach, and there are quite a few frameworks, a few notable ones :</p>


<ul>
    <li><a href="http://ionicframework.com" target="_blank"><b>Ionic Framework </b></a></li>
    <li><a href="https://facebook.github.io/react-native/" target="_blank"><b>React Native</b></a></li>
    <li><a href="https://www.nativescript.org" target="_blank"><b>Native Script</b></a></li>
</ul>

<p>Each one uses a different toolset and has different performance, quirks and tradeoffs, so in the end choosing one over the other is a bit of a matter of choice, I went with <b>React-Native</b> because it seems like a good place to start provided you already know some react, which I do, performance, documentation, community support and the fact that it is free are all contributing factors, but as I mentioned other frameworks are also valid and might suit your tastes or project better. </p>


</div>

<div class="speechBubble"> ( <i>Optional-ish</i> ) We will be using React,if you have never used React, here's a few introductory posts :
</div>

- [Getting started with React.js]({{ site.baseurl }}/Getting-Started-With-ReactJs){:target="_blank"}
- [More React.js Pens]({{ site.baseurl }}/More-ReactJs-Pens){:target="_blank"}

<h3 class="fancy">Setting Up</h3>

Setting up in theory is simple, at least the instructions are :<b><a href="https://facebook.github.io/react-native/docs/getting-started.html" target="_blank">React-Native Docs: Getting started.</a></b>. You might need to update a few packages in your computer and install dependencies and other programs, after a few minutes of console time I got it to work on Mac and compile a simple app on an emulator as well as some minor edits:

![React-Native Setup](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/react-native/SetupPt1v2.jpg)

On the Android side, my experience was unfortunately less than pleasant, to use React-Native (and do Android development in general), you need to install an IDE (Android Studio), and deal with setting it up, something that took some 8+ hrs of hunting down bugs, downloading libraries and messing with the command line, additionally, Android emulators and Android Studio are on the slow side, so budget some extra time and patience for setting up your Android environment, thankfully, this is something you most likely will only do once and might fine-tune as you develop more for each platform.

![React-Native Setup pt 2](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/react-native/SetupPt2v1.jpg)


**Real Devices ?**

Having an emulator is one thing, but in the end you will probably want to test on a real device, let's hit the docs once more and see if we can run the test app in both an iOS and Android device by following their guide: <b><a href="https://facebook.github.io/react-native/docs/running-on-device.html" target="_blank">React-Native Docs: Running on Device</a></b>

Here it is running on Android which took just a few minutes and enabling developer mode on my screen cracked test phone:

![React-Native Setup pt 2 Android](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/react-native/SetupHwAndroid.jpg)

Paradoxically, on a real Iphone I had one hell of a time running the app ( <i> another 8+ hours </i> ), Apple requires a certificate you can get through Xcode ( which in turn might need to be updated, which in turn might require you to update iOS, etc, etc), but after a few tries, downloads and curses...success! :


![React-Native Setup pt 2 ios](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/react-native/SetupPt2v2.jpg)

<div class ="note"><b>Note:</b>It should be noted that at this moment you can only get a temporary <b>free</b> developer certificate from Apple, if you want a more permanent one you'll have to sign up and pay (see below) </div>


<b> We are not done yet...</b>

At some point you will want to release your react-native app to the world, in order to do this, you will have to go through each platforms guides (these are complex issues deserving of their own tutorials, so just keep that in mind ) :


<ul>
<li><a href="https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppDistributionGuide/SubmittingYourApp/SubmittingYourApp.html" target="_blank">For the ios-itunes store</a></li>
<li><a href="https://support.google.com/googleplay/android-developer/answer/113469?hl=en" target="_blank">For Android-Google Play store</a></li>
</ul>

<br />
<div class ="note"> <b>Note:</b> There is also a monetary cost to submit and sign up as a developer for each platform. ( <i> $25 for google & $100yr for Apple </i> )
</div>


<b> Hot Reloading: </b>

So our setup is nearly complete, in my case I went with Atom as the IDE ( <i>Integrated development environment </i>) and an iphone emulator for development, Android will have to be a separate activity as well as packaging and testing the app for release based on the above setup.

One last extra that is worth checking is Hot Reloading, which allows you to make changes to your code and see them as soon as you save the file, check the docs for instructions: <a href="https://facebook.github.io/react-native/docs/debugging.html" target="_blank"><b>React-Native: Debugging</b></a>

![React-Native Hot Reloading](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/react-native/ReactNative-HotReloading.gif)

<h3 class="fancy">Conclusion</h3>

React-Native is a promising framework backed by heavyweight Facebook and it promises to make developing apps for both iOS and Android a one step process using react, in this first part, I dealt with setting up, something that unfortunately is still a mayor pain point due to both the complexity and specifics of each platform as well as particular technical issues.

<b>TL;DR :</b> <i> React-Native = ios/android apps, budget a couple of days for setting up .</i>

We'll deal with checking react-natives components on the next part, till then, have fun ( and patience )  setting up.

Best,

Keno.
