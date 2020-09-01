---
layout: post
title:  "XInput and DirectInput"
date:   2020-07-13 19:00:00 -0700
categories: [Games, Controller]
---

<p style="font-size: 0.9rem;font-style: italic;"><img style="display: block;" src="https://upload.wikimedia.org/wikipedia/commons/6/6a/Logitech_Rumblepad_F510%2C_1.jpg" alt="File:Logitech Rumblepad F510, 1.jpg"><a href="https://commons.wikimedia.org/w/index.php?curid=28971501">"File:Logitech Rumblepad F510, 1.jpg"</a><span> by <a href="https://commons.wikimedia.org/wiki/User:Morn">Morn</a></span> is licensed under <a href="https://creativecommons.org/licenses/by-sa/3.0?ref=ccsearch&atype=html" style="margin-right: 5px;">CC BY-SA 3.0</a><a href="https://creativecommons.org/licenses/by-sa/3.0?ref=ccsearch&atype=html" target="_blank" rel="noopener noreferrer" style="display: inline-block;white-space: none;margin-top: 2px;margin-left: 3px;height: 22px !important;"><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc_icon.svg" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-by_icon.svg" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-sa_icon.svg" /></a></p>

XInput is an API that allows applications to receive input from the Xbox Controller for Windows.
The DirectInput API is used to process data from a joystick, or other game controller. 
Use of legacy DirectInput is not recommended, and DirectInput is not available for Windows Store apps.

Microsoft introduced XInput as a new API with better support for advanced controllers. 
Around 2011 Microsoft deprecated DirectInput, Some controllers have a hardware switch to toggle modes.

["Xbox 360 Controller Emulator"](https://github.com/x360ce/x360ce) 
program could be used to translate XInput calls to DirectInput calls - supports old, non-XInput compatible GamePads.


### References:
- [XInput and DirectInput](https://docs.microsoft.com/en-us/windows/win32/xinput/xinput-and-directinput)
- [PC gamepads: DirectInput vs XInput](https://nelsonslog.wordpress.com/2018/12/24/pc-gamepads-directinput-vs-xinput/)
- [DirectInput vs XInput](https://en.wikipedia.org/wiki/DirectInput#DirectInput_vs_XInput)
- [How to Remap Xbox, PlayStation, and Other Controller Buttons in Steam](https://www.howtogeek.com/234427/how-to-remap-buttons-on-your-steam-controller/)
- [TocaEdit Xbox 360 Controller Emulator](https://www.x360ce.com/)