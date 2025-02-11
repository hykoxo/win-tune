# win-tune
Some tools and files I use for making Windows 11 look my way.

[![Windows 11](./screenshot.png)](./![preview.png](screenshot.png))

## AtlasOS
I use AtlasOS to make Windows more performant, usable, and privacy-friendly. You can download it [here](https://atlasos.net/).

## Custom cursor
I use a custom cursor from [this](https://github.com/antiden/macOS-cursors-for-Windows) repository.

1. Download the repository.
2. Install with Install.inf. (Right-click on Install.inf and click Install)
3. Go to Settings > Devices > Mouse > Additional mouse options > Pointers > Browse and select the cursor you want.

I use the one with the shadow.

## Taskbar
I use TranslucentTB to make the taskbar transparent. You can download it [here](https://github.com/TranslucentTB/TranslucentTB).

## Windows Manager
I use FancyZones from [PowerToys](https://github.com/microsoft/PowerToys) to manage windows.

1. Download PowerToys from the releases page.
2. Install PowerToys.
3. Open PowerToys and go to FancyZones.
4. Create a custom layout and apply it.

* With that when I drag a window and click on Shift, I can snap it to the zones.

## Wallpaper
I use Wallpaper Engine to set a live wallpaper. You can download it [here](https://store.steampowered.com/app/431960/Wallpaper_Engine/).

Here is the wallpaper on the screenshot: [https://steamcommunity.com/sharedfiles/filedetails/?id=2181619161](https://steamcommunity.com/sharedfiles/filedetails/?id=2181619161)

## Custom apps icons
I use Custom Icons for apps in my taskbar.
Simply replace the icon in the properties of the app.

## Terminal
I use WizTerm. You can download it [here](https://wezfurlong.org/wezterm/index.html).

To configure WizTerm:

1. Copy the content only of [terminal](./terminal) folder to your home directory. (C:\Users\your-username)
2. Simply run the terminal and it will automatically load the configuration.

## Oh My Posh (nice terminal)
I use Oh My Posh to make the terminal look better. You can download it [here](https://ohmyposh.dev/).

To configure Oh My Posh:

1. Install Oh My Posh. (You can install it with the following command)
```
winget install JanDeDobbeleer.OhMyPosh -s winget
```
2. Copy the content of [oh-my-posh](./oh-my-posh) folder to your home directory. (C:\Users\your-username)
3. Open WizTerm and run the following command to create the profile.
```
New-Item -Path $PROFILE -Type File -Force
```
4. Open the profile with Notepad.
```
notepad $PROFILE
```
5. Add the following lines to the profile.
```
oh-my-posh init pwsh --config ~/zonny.omp.json | Invoke-Expression
```
6. Save the profile and restart the terminal.

### Compatibility
Oh My Posh works well with WizTerm but it may not work with other terminals.
On the windows terminal or vscode its not working for me, here is how you can configure it:

1. Download the font [MesloLGM Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases).
2. Search for Meslo.zip and download it.
3. Extract the zip and install the font.

4. Open the windows terminal with administrator privileges.
5. press `CTRL + SHIFT + ,` to open the settings.
6. Add/edit the following lines to the settings.
```json
"defaults": {
    "font":
    {
        "face": "MesloLGM Nerd Font"
    }
},
```
7. Save the settings and restart the terminal.
8. For vscode, modify the settings, search for `@feature:terminal font` and set it to `MesloLGM Nerd Font`.

Now you should see the nice terminal.
