# PressSleepKey - turn your monitor off
![GitHub](https://img.shields.io/github/license/tushev/presssleepkey) ![C#](https://img.shields.io/badge/language-C%23-green)  ![.NET 6](https://img.shields.io/badge/runtime-.NET%206-blueviolet) 


The story of this app is very simple: I had a keyboard with dedicated **Sleep** key, that I used for turning my display off. Not locking, just shutting down the display.<br>
After a while, I replaced my keyboard with a newer one, with lots of cool features, and programmable keys (CORSAIR K55 RGB PRO XT).<br> 
However, it turned out that it is not possible to make one of the keys function like dedicated **Sleep** key.

This program sends [WM_SYSCOMMAND](https://docs.microsoft.com/en-us/windows/win32/menurc/wm-syscommand) WinAPI message with `SC_MONITORPOWER, 2` params.
This message shuts the display off.

Normally, Windows should turn the monitor on if the user moves the mouse or presses any key.
However, this program does nothing to turn the display back on; it's up to the user.

* `src-console` contains console app
* `src-winforms` contains WinForms app

It seems that Corsair iCUE software does not allow to assign a console app to the custom keys (sic!). Please use WinForms version with iCUE.

