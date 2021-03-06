# Code

## Code in Framer

Framer X let’s you do advanced interactive design without using a line of code, either by using the interactive tools, or by using components from the store that were built by others. If you are looking to build your own components you can use code to make them do anything.

Framer X uses code in a different way then you might be used to from a design tool. Framer X does not generate code for you from your designs, but instead it uses code that you wrote compose interfaces. This is better because:

* You can share code with production, your design component can be the exact same version that runs on your production website, so there is a single source of truth.
* Auto generated code ultimately almost never ends up in production, developers want to have full control over every aspect and will typically always \(re\)write it by hand according to internal standards and processes. 

## Types of Code

Framer uses code in two distinct places: **components** and **functions**.  
  
[Components](components.md) are [React Components](https://reactjs.org/docs/thinking-in-react.html). They are parts of an interface that you can compose into large applications. The code that you typically write for components concern just that component. So for a slider, it would contain the code to draw the knob and rails, plus the code to handle the scrubbing, nothing more than that.  
  
[Functions](functions.md) facilitate communication between components. To turn components into an app, they need to communicate. So the slider has to maybe change the position of something. Functions allow you to override any properties before the components get previewed, update or respond to application state, and attach event handlers to make things interactive.  
  
**Note**: functions are very minimal on purpose so that you can use them any way you like, and do things like bring your own state management like Redux if you want, or no state management at all.

## Overview

All code in Framer is expressed in plain **React** using **JavaScript ES6**. A component can be as simple as just one html tag with some css, all the way to a very complex media player with rich interactions. This also means that people with a variety of skill can make components. If you know basic web development you can learn to build them in ten minutes. If you are an advance engineer that knows React, you don’t have to learn anything new, everything will just work like you expect.

**Note**: Under the hood Framer X actually uses [TypeScript](https://www.typescriptlang.org/), a typed version of JavaScript. Types help to manage larger applications and helps us to offer really great auto complete for editors, but for you they are completely optional, you can just write ES6 if you like.

**Note**: Although there might be a way to create React Native applications in Framer in the future, we don’t offer an official way today. You are of course free to explore how far you can come yourself. Our open source Framer library should contain everything you need to get started.

## Setup and Workflow

Framer X relies on an external editor for writing code. Any editor will work, but we strongly suggest one that supports TypeScript \(for auto complete\). Our personal favorite by far is [VSCode by Microsoft](https://code.visualstudio.com/) with the optional [Prettier extension](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) installed so your code always looks nice.  
  
If you edit any Framer X code it automatically gets updated in Framer X when you save the file. So components get re-rendered on the canvas and in the preview, and functions get updated under the hood.   
  
If you get an error, the component will turn red and display the error message with optional suggestions where to look for the exact error. There are two types of errors:

* **Syntax error** – You likely made a typo in your code and de computer does not understand it. The most common ones are capitalization errors, missing brackets or comma’s.
* **Runtime error** – Something went wrong while running the code. This can be anything really.

Errors are listed in the right bottom of your screen. To deeper investigate errors, you can use the [web inspector](https://developer.apple.com/safari/tools/) by clicking on the error counter, or right clicking in the Preview and choosing “Inspect Element”.  
  
_**TBD: Editing components from the store.**_  
****  
**Note**: we recommend a window manager utility like [Magnet](http://magnet.crowdcafe.com/) to help with managing your windows efficiently between code and canvas.  
  
**Note**: we might introduce a code editor back in Framer in the future, but for now we chose to focus on the rest of the app. Building an editor as great as VSCode is very hard, and we were noticing many users in legacy Framer already using their own editor, bypassing the built-in one.  
  
**Note**: Because the code runs in both the canvas and preview, there are two inspectors. You’ll likely most often need the one for preview.  




