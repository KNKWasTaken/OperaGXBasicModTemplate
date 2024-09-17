# Mod Template
This is a mod template based on the Minecraft.GX mod by KNKWasTaken. It uses the first version of Minecraft.GX
# How to Use
There are detailed instruction given below on how to use the template:-
# Table of Contents
- [Mod Template](#mod-template)
- [How to use](#how-to-use)
- [Table of Contents](#table-of-contents)
- [Manifest.JSON](#manifestjson)
- [Mod Icons](#mod-icons)
- [Mod Details](#mod-details)
  - [License](#license)
  - [Background Music](#background-music)
  - [Browser Sounds](#browser-sounds)
  - [Keyboard Sounds](#keyboard-sounds)
  - [Webmodding (Page Styling)](#webmodding-page-styling)
  - [Shaders](#shaders)
  - [Theme](#theme)
  - [Wallpaper](#wallpaper)
    - [Static Wallpaper](#static-wallpaper)
    - [Live Wallpaper](#live-wallpaper)
    - [Interactive Wallpaper](#interactive-wallpaper)
- [How to try and debug your mod?](#how-to-try-and-debug-your-mod)
- [How to upload your mod to public](#how-to-upload-you-mod-to-public)
- [Other Resources](#other-resources)
# Manifest.JSON
Manifest.JSON is the most important part of any Opera GX Mod. It describes which file should be used for what purpose. For the mod, you will need some prerequisite knowledge on JSON. Some things you can change right now are:-
```json
{
    "name": "Minecraft.GX",
    "description": "A perfect experience for Minecraft gamers",
    "developer":
    {
        "name": "KNKWasTaken"
    },
    "version": 1.0
}
```
1. `name` is the name of you mod.
2. `description` is a short description of your mod.
3. `developer > name` is the name of the developer.
4. `version` is the version of your mod.
There are other changable things we will talk about later. This file should be saved with the name `manifest.json` without any exceptions
# Mod Icons
These represent the icon of your mod. The icons of a mod are always in 1:1 aspect ratio with any usual size. The most common dimension are 128x128, 512x512, etc.. Here are examples of how to set them:-
```json
{
    "icons":
    {
        "512": "mcico512.png",
        "128": "mcico128.png"
    }
}
```
1. Here, we will use the dimension for the key and the file for the value.
Ex. If `mcico512.png` has the dimensions 512x512, the key would be `512`.
# Mod Details
Here, we define what we want our mod to do. There are various kinds of mods, like Gamestrips (Exclusive for GameMaker), Wallpapers, etc. This is a tutorial on Mods which customize the appearance of Opera GX.
In this mod, there are several kinds of features that can be added like:-
1. License
2. Background Music
3. Browser Sounds
4. Keyboard Sounds
5. Webmodding (Page Styling)
6. Shaders
7. Themes
8. Wallpapers
An Important Note:- Every feature listed should be nested under `mod` in `manifest.json`.
## License
License describes how your mod is protected from others to use and how others are limited to use it. License are not neccessary. You can purchase a license like MIT or Creative Commons, copy the text format, and paste it in a file, say `license.txt`.
To apply a license to your mod, do the following:-
```json
{
    "mod":
    {
        "license": "license.txt"
    }
}
```
1. `license` defines the license to Opera GX
## Background Music
Background Music play in the background whenever Opera is running. They are enabled by default. The format for the background music is preferably MP3 or WAV.
To apply these, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "background_music":
            [
                "music/track_1.mp3",
                "music/track_2.mp3",
                "music/track_3.mp3",
                "music/track_4.mp3"
            ]
        }
    }
}
```
1. `payload` covers the styling functions of a mod.
2. `background_music` specifies Opera about the tracks that are to be used.
3. If there are more than one file, keep them in square brackets ([]) seprated by a comma (,).
4. It would be preferable to keep them in a seperate folder. If kept in a seprate folder, you need to specify the relative path inside the folder. Ex. If the folder name is `music`, then use the path `music/yourtrack.mp3`
## Browser Sounds
Browser Sounds are small sounds that play when you interact with the browser. They are enabled by default. The format for the bowser sounds are preferably MP3 or WAV.
To apply these, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "browser_sounds":
            {
                "CLICK":
                [
                    "sound/click.mp3"
                ],
                "FEATURE_SWITCH_OFF":
                [
                    "sound/feature_switch_off.mp3"
                ],
                "FEATURE_SWITCH_ON":
                [
                    "sound/feature_switch_on.mp3"
                ],
                "HOVER":
                [
                    "sound/hover.mp3"
                ],
                "HOVER_UP":
                [
                    "sound/hover.mp3"
                ],
                "IMPORTANT_CLICK":
                [
                    "sound/important_click.mp3"
                ],
                "LEVEL_UPGRADE":
                [
                    "sound/level_upgrade.mp3"
                ],
                "LIMITER_OFF":
                [
                    "sound/limiter_off.mp3"
                ],
                "LIMITER_ON":
                [
                    "sound/limiter_on.mp3"
                ],
                "SWITCH_TOGGLE":
                [
                    "sound/switch.mp3"
                ],
                "TAB_CLOSE":
                [
                    "sound/close_tab.mp3"
                ],
                "TAB_INSERT":
                [
                    "sound/new_tab.mp3"
                ],
                "TAB_SLASH":
                [
                    "sound/tab_slash.mp3"
                ]
            }
        }
    }
}
```
1. `browser_sounds` specifies Opera what sounds to play when the user interacts with the browser. There are limited options on what is possible.
2. `CLICK` play whenever the user clicks with his mouse.
3. `FEATURE_SWITCH_OFF` plays whenever the user toggles off a feature in Opera.
4. `FEATURE_SWITCH_ON` plays whenever the user toggles on a feature in Opera.
5. `HOVER` plays whenever the user hovers over an interactive element in Speed Dial (New Tab)
6. `HOVER_UP` plays whenever the user hovers over a pop-out element, like YouTube videos or Twitch Livestreams in thier pop-out window.
7. `IMPORTANT_CLICK` plays whenever the user clicks some specific elements in Opera.
8. `LEVEL_UPGRADE` plays whenever the user upgrades the level (version) of Opera.
9. `LIMITER_ON` plays whenever the user turns the Limiter feature on.
10. `LIMITER_OFF` plays whenever the user turns the Limiter feature off.
11. `SWITCH_TOGGLE` plays whenever the user toggles a nomal switch.
12. `TAB_CLOSE` plays whenever the user closes a tab.
13. `TAB_INSERT` plays whenever the user adds a tab.
14. `TAB_SLASH` plays whenever the user kills a tab from the Hot Tab Killer feature.
15. If there are more than one file, keep them in square brackets ([]) seprated by a comma (,).
16. It would be preferable to keep them in a seperate folder. If kept in a seprate folder, you need to specify the relative path inside the folder. Ex. If the folder name is `sound`, then use the path `sound/yourtrack.mp3`
## Keyboard Sounds
Keyboard Sounds are small sounds that are played whenever the keyboard is used. They are enabled by default. The format for keyboard sounds are preferably WAV or MP3.
To apply these, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "keyboard_sounds":
            {
                "TYPING_BACKSPACE":
                [
                    "keyboard/backspace.wav"
                ],
                "TYPING_ENTER":
                [
                    "keyboard/enter.wav"
                ],
                "TYPING_LETTER":
                [
                    "keyboard/letter_1.wav",
                    "keyboard/letter_2.wav",
                    "keyboard/letter_3.wav"
                ],
                "TYPING_SPACE":
                [
                    "keyboard/space.wav"
                ]
            }
        }
    }
}
```
1. `keyboard_sounds` specify opera what sound to play when the user uses his keyboard.
2. `TYPING_BACKSPACE` plays whenever the user presses Backspace.
3. `TYPING_ENTER` plays whenever the user presses Enter.
4. `TYPING_LETTER` plays whenever the user presses a key on the keyboard, which isn't a special key.
5. `TYPING_SPACE` plays whenever the user presses Space.
6. If there are more than one file, keep them in square brackets ([]) seprated by a comma (,).
7. It would be preferable to keep them in a seperate folder. If kept in a seprate folder, you need to specify the relative path inside the folder. Ex. If the folder name is `keyboard`, then use the path `keyboard/yourtrack.mp3`
8. Keyboard Sounds work on a very minimalist keyboard, so most of the times, sections of the keyboard like the Number Pad doesn't apply for this.
## Webmodding (Page Styling)
Webmodding changes the appearance of of certain websites or webpages by the use of CSS (Cascading Style Sheets). Prerequisit knowledge of CSS and DevTools are neccesary. First you need to create any CSS file (`.css`) for changing the appearance of a website. We then inspect the website, find the elements we need to modify, apply the CSS rule, save it and inject it through the mod.
An example of a CSS file modding the webpage of Opera is:-
```css
body {
    color: env(--opera-gx-accent-color)
    background: env(--opera-gx-background-color)
}
```
1. This is a basic CSS file that changes the appearance of text and the background of Opera.
2. `--opera-gx-accent-color` is a variable in Opera that retrieves the accent color from the theme of the broowser. Other ways to access it are mentioned in `webmodding/opera.css`
3. `--opera-gx-background-color` is a variable in  Opera that retrieves the background color from the theme of the browser. Other ways to access it are mentioned in `webmodding/opera.css`

There are other CSS files provided that change the appearance of Discord. These are `webmodding/dcmaintheme.css` & `webmodding/dcchangecolors.css`. These are not explained here but usefull comments can be helpfull.

To apply these to the mod, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "page_styles":
            [
                {
                    "css":
                    [
                        "webmodding/opera.css"
                    ],
                    "matches":
                    [
                        "https://*.opera.com/*"
                    ]
                },
                {
                    "css":
                    [
                        "webmodding/dcmaintheme.css",
                        "webmodding/dcchangecolors.css"
                    ],
                    "matches":
                    [
                        "https://*.discord.com/*"
                    ]
                }                
            ]
        }
    }
}
```
1. `page_styles` specifies Opera the files to use for Webmodding. Always keep the files inside square brackets ([]), followed by a curly bracket ({}) for individual files.
2. `css` links to the CSS files that are to be used for webmodding. This is followed by square brackets ([]) for the files. If there are more than one file, seperate them by a comma (,) in the same bracket.
3. `matches` link to the sites which will take the effect of the CSS file. This is followed by square brackets ([]) for the sites. If there are more than one site, seperate them by a comma (,) in the same bracket. Usage of asterix (*) is used for subdomains and such.
4. It would be preferable to keep them in a seperate folder. If kept in a seprate folder, you need to specify the relative path inside the folder. Ex. If the folder name is `webmodding`, then use the path `webmodding/yourmodif.css`.
## Shaders
Shaders are static or animated overlays that affect every webpages (Except a few browser-specific sites like opera://newtab (Speed Dial), opera://mods (Mods), opera://settings (Settings), opera://extensions (Extensions), opera://operius (Operius), etc.). These follow WebGL to achieve this. For making shaders, prerequisite knowledge of WebGL is needed. One example of a static green overlay is:-
```javascript
uniform shader iChunk;

const float4 TINT = float4(1.33, 0.8, 1.33, 1);

vec4 main(vec2 xy)
{
    return pow(iChunk.eval(xy), TINT)
}
```

Make sure to save the file in Text (`.txt`) format

Animated shaders are also possible. For seeing one, go to `shader/wave.txt`

To apply this to the mode, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "shaders":
            {
                "Wave":
                {
                    "animation":
                    {
                        "duration": 60,
                        "steps": 3600
                    },
                    "path": "shader/wave.txt"
                },
                "Minecraft Matrix": "shader/matrix.txt"
            }
        }
    }
}
```
1. `shaders` specify the files to be used as shaders.
2. The key will be the name of your shader wheras the value will either be curly brackets (for animated) or string (for static). The string will specify the path to the WebGL file.
3. `animation` specifies the shader is an animated one.
4. `duration` is the length of the animation in seconds.
5. `steps` is the number of steps in the animation
6. `path` is the specification to the path of the WebGL file if it is an animated one.
7. It would be preferable to keep them in a seperate folder. If kept in a seprate folder, you need to specify the relative path inside the folder. Ex. If the folder name is `shader`, then use the path `shader/yourfile.txt`
## Theme
Theme is the color of browser. Some default themes are GX Classic, Ultravoilet, Sub Zero, Frutti Di Mare, Purple Haze, Vaporwave, Rose Quartz, Coming Soon, Hackerman, Lambda, After Eight, Pay-To-Win, White Wolf, etc.
To apply this, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "theme":
            {
                "dark":
                {
                    "gx_accent":
                    {
                        "h": 125,
                        "s": 96,
                        "l": 36   
                    },
                    "gx_secondary_base":
                    {
                        "h": 16,
                        "s": 42,
                        "l": 24
                    }
                },
                "light":
                {
                    "gx_accent":
                    {
                        "h": 85,
                        "s": 100,
                        "l": 36
                    },
                    "gx_secondary_base":
                    {
                        "h": 12,
                        "s": 48,
                        "l": 46
                    }
                }
            }
        }
    }
}
```
1. `theme` specifies Opera the theme colors.
2. `dark` specifies the theme for dark mode.
3. `light` specifies the theme for light mode.
4. `gx_accent` specifies the accent (foreground) color of Opera. It is the value of `--opera-gx-accent-color`.
5. `gx_secondary_base` specifies the secondary base (background) color of Opera. It is the value of `--opera-gx-background-color`.
6. `h` specifies the color hue.
7. `s` specifies the color saturation.
8. `l` specifies the color lighting.
## Wallpaper
Wallpaper is the background of Opera Speed Dial. It is enabled by default. There are three kinds of wallpapers: Static, Live, Interactive. Here we will only learn about Static and Live Wallpapers.
### Static Wallpaper
These are image wallpapers. They are also the most common type of wallpaper. The preferable format for this is PNG.
To apply this, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "wallpaper":
            {
                "dark":
                {
                    "image": "wallpaper/minecraftbg.png",
                    "text_color": "#FFFFFF",
                    "text_shadow": "#757575"
                },
                "light":
                {
                    "image": "wallpaper/minecraftbg.png",
                    "text_color": "#FFFFFF",
                    "text_shadow": "#0B000E"
                }
            }
        }
    }
}
```
1. `wallpaper` specifies Opera what the background of the Opera Speed Dial is.
2. `dark` and `light` have the same functionality as when used in [`theme`](#theme) but instead for theme, they specify for wallpapers.
3. `image` is the image to be used for background.
4. `text_color` is the text color for the text on Speed Dial.
5. `text_shadow` is the shadow added on to the text.
6. It would be preferable to keep them in a seperate folder. If kept in a seprate folder, you need to specify the relative path inside the folder. Ex. If the folder name is `wallpaper`, then use the path `wallpaper/yourbackground.png`.

More useful tips on how to make an image for static wallpapers are provided as a PDF Document, `GXWallpaperGuidelines.pdf`
### Live Wallpaper
These are video wallpapers. The preferable format for this is VP9 but MP4 and WEBM also works (some bugs might be possible with MP4).
To applt this, do the following:-
```json
{
    "mod":
    {
        "payload":
        {
            "wallpaper":
            {
                "dark":
                {
                    "image": "wallpaper/livewallpaper.webm",
                    "first_frame": "wallpaper/livewallpaperframe.jpg",
                    "text_color": "#FFFFFF",
                    "text_shadow": "#757575"
                },
                "light":
                {
                    "image": "wallpaper/livewallpaper.webm",
                    "first_frame": "wallpaper/livewallpaperframe.jpg",
                    "text_color": "#FFFFFF",
                    "text_shadow": "#0B000E"
                }
            }
        }
    }
}
```
1. `image` will be used to specify the video.
2. `first_frame` specifies where the video will start from, based on an provided image. It can cause errors is the frame is not found in the video.
### Interactive Wallpaper
These are wallpaper you can interact with using your mouse. They are a new feature. To make this, you will need GameMaker and a different `manifest.json` version. Interactive Wallpapers are not covered in this tutorial, but you can learn how to make one from [Opera's YouTube Tutorial to Interactive Wallpapers](https://youtu.be/FshjAOMz12w?si=XdRHc4BKiDegEihH).
# How to try and debug your mod?
1. Go to the Extensions page (opera://extensions).
2. Enable Developer Mode.
3. Click `Load Unpacked`.
4. Choose your mod folder and upload it.
5. For a video tutorial, check out [Opera's YouTube Tutorial on Making A New Mod](https://youtu.be/trpdOR0WGG4?si=PmlR-swq1KUPRfhD)
# How to upload you mod to public?
1. Compress your mod folder to a ZIP File.
2. Go to GX.Create (create.gx.games).
3. Go to the mod tab, if not already.
4. Click `Upload New Mod` > `Choose File`.
5. Choose the ZIP file.
6. Check detailss and upload a Cover Art by going to `Media` > `Cover Art`.
7. Add some fitting tags and a long description in `Metadata`.
8. Go to `Publishing` > `Staging` > `Promote to Public` and toggle the `Publishing` > `Public` checkmark.
9. For uploading a new version, click `Publishing` > `Staging` > `Upload New Version` and chose the updated ZIP file.
# Other Resources
Other resources you should check out are:-
1. [The Official Modding GitHub](https://github.com/opera-gaming/gxmods)
2. [The Web Modification YouTube Tutorial](https://www.youtube.com/playlist?list=PLhIbBGhnxj5J0WOhfGKokAAGoxCEHT9gH)
3. [The Sounds and Music YouTube Tutorial](https://www.youtube.com/playlist?list=PLhIbBGhnxj5K6bC3aFiI2jAFy9kZ77jf3)
4. [The Theme and Wallpaper YouTube Tutorial](https://www.youtube.com/playlist?list=PLhIbBGhnxj5KWPRYhbreaN2l8VZy3Vshv)
5. [The Interactive Wallpaper YouTube Tutorial](https://www.youtube.com/watch?v=p9Fv8CFJjg0)
6. [The Official Mod_Template by Opera](https://github.com/opera-gaming/gxmods/blob/main/documentation/Mod_Template)
7. [Modding Documentations by Opera](https://github.com/opera-gaming/gxmods/blob/main/documentation/mods.md)
8. [Figma Template for GX.Store images by Opera](https://github.com/opera-gaming/gxmods/blob/main/documentation/GXStoreFigmaTemplate.fig.zip)