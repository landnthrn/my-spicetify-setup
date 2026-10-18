
![Modified StarryNight PREVIEW](https://github.com/user-attachments/assets/3c9c4c33-d704-45e3-803e-3aaff9734bf5)

This is my personal Spicetify setup, for those that want a great starting point to build on, or skip configuring and simply acquire what I consider to be a proper collection and configuration of Spicetify. 
I've purposely left out parts that I felt were too opinionated for the common person.  
Also includes "downpour-black" a theme I made using **[Spotify-Dark](https://github.com/SyndiShanX/Spotify-Dark)** as a starting point.

---

### Notes

- Use all the commands listed in this guide in PowerShell *(no admin needed)*
- See **[spicetify-command-cheatsheet.md](./spicetify-command-cheatsheet.md)** if you're unfamiliar with Spicetify's CLI
  - In the commands provided, make sure to replace `<noteslikethis>` for what they state
- Spicetify usually needs to be updated when Spotify does, whenever Spicetify developers release an update use `spicetify update` then `spicetify apply`
  - If a Spotify update breaks it, you downgrade until Spicetify updates,  **[suggest using this tool](https://github.com/amd64fox/Rollback-Spotify)** or read how in the FAQ channel of Spicetify's Discord Server
- Recommend to join the **[Spicetify Discord](https://discord.com/invite/spicetify-842219447716151306)**  

---

### Installing Spicetify

1. Make sure your Spotify install is desktop, not from Microsoft store *(square Spotify icon indicates Microsoft Store)*
2. Run the official install command in PowerShell:
```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/spicetify-cli/main/install.ps1 | iex
```
3. Use `y` when prompted to install the marketplace

For more info, see their official page: **[Spicetify Installation Guide + Info](https://spicetify.app/docs/advanced-usage/installation**)

---

### Apply My Marketplace Settings

1. Select the gear icon Spicetify Marketplace
2. Backup/restore > open > import from file *(If you already have a marketplace setup of your own, export it first so it isn't lost.)*
3. Select the setting `.json` you want from `settings\` folder provided in this repo
   - My `marketplace-settings-starrynight.json` export is the same as my `marketplace-settings-universal.json` just with a couple less add-ons that sorta ruined the look of StarryNight. 
4. Restart/Reload Spotify

---

### Apply a Theme

1. Copy or move the folders inside `themes-modified-by-me\` &/or `themes-by-me\` to Spicetify's local theme location:
```
%localappdata%\spicetify\Themes
```
2. Apply your desired theme: (replace `<themefoldername>` with the theme folder name)
```powershell
spicetify config current_theme <themefoldername>
spicetify apply
```

#### Apply a Color Scheme

For themes that come with multiple color schemes, pick the want you to apply.

1. Open the theme's `color.ini`, scheme names are wrapped in [square brackets] 
2. Apply the one you want by running: 
```powershell
spicetify config color_scheme <schemename>
```

- My StarryNight modified color scheme you see in the preview is called `downpurp`

---

### Apply Local Extensions & Custom Apps

- The Marketplace makes installing add-ons easier, but plenty more can be found elsewhere & applied locally. This also gives freedom for add-ons to be more customized
- Use `Appdata\Roaming` locations for local custom apps & extensions

#### Local Extensions

- Place an extension file in this location:
```
%appdata%\spicetify\Extensions
```
- Apply with:
```powershell
spicetify config extensions <nameofextensionfile.itsformat>
```

#### Custom Apps

- Place the custom app folder or file into this location:
```
%localappdata%\AppData\Roaming\spicetify\CustomApps
```
- Apply with:
```powershell
spicetify config custom_apps <nameofcustomappfolderorfile>
```


---

### Credits

#### Spicetify

- **[Spicetify Website](https://spicetify.app)**
- **[Spicetify Github](https://github.com/spicetify)**
- **[Spicetify Discord](https://discord.com/invite/spicetify-842219447716151306)**  

#### Themes
- **[StarryNight (Newer)](https://github.com/Carlitos999yt/StarryNight-Repair-New-Version)** by **[Carlitos999yt](https://github.com/Carlitos999yt)**
- **[StarryNight (Original)](https://github.com/spicetify/spicetify-themes/tree/master/StarryNight)** by **[b-chen00 (Brandon Chen)](https://github.com/b-chen00)** & **[laignelet16 (Julissa Laignelet)](https://github.com/laignelet16)**
- **[Spotify-Dark](https://github.com/SyndiShanX/Spotify-Dark)** by **[SyndiShanX](https://github.com/SyndiShanX)**

#### Add-ons in my marketplace exports

**Extensions**
- **[Song Stats](https://github.com/rxri/spicetify-extensions)**, by **[CharlieS1103](https://github.com/CharlieS1103)**
- **[Display full Album date](https://github.com/huhridge/huh-spicetify-extensions)**, by **[huhridge](https://github.com/huhridge)**
- **[Full Screen](https://github.com/daksh2k/Spicetify-stuff)**, by **[daksh2k](https://github.com/daksh2k)**
- **[Save Playlists](https://github.com/daksh2k/Spicetify-stuff)**, by **[daksh2k](https://github.com/daksh2k)**
- **[Toggle DJ](https://github.com/ohitstom/spicetify-extensions)**, by **[ohitstom](https://github.com/ohitstom)**
- **[Tracks To Edges](https://github.com/ohitstom/spicetify-extensions)**, by **[ohitstom](https://github.com/ohitstom)**
- **[Queue Time](https://github.com/Theblockbuster1/spicetify-extensions)**, by **[Theblockbuster1](https://github.com/Theblockbuster1)**
- **[Cover Ambience](https://github.com/Theblockbuster1/spicetify-extensions)**, by **[Theblockbuster1](https://github.com/Theblockbuster1)**
- **["Made for you" shortcut](https://github.com/Pithaya/spicetify-apps)**, by **[Pithaya](https://github.com/Pithaya)**
- **[Playlist icons](https://github.com/jeroentvb/spicetify-playlist-icons)**, by **[jeroentvb](https://github.com/jeroentvb)**
- **[Reeeewiiiind](https://github.com/NickColley/spicetify-rewind)**, by **[NickColley](https://github.com/NickColley)**
- **[HomeWhereYouBelong](https://github.com/yodaluca23/spicetify-extensions)**, by **[yodaluca23](https://github.com/yodaluca23)**
- **[GoToSong](https://github.com/huhridge/huh-spicetify-extensions)**, by **[huhridge](https://github.com/huhridge)**
- **[Quick Queue](https://github.com/ohitstom/spicetify-extensions)**, by **[ohitstom](https://github.com/ohitstom)**
- **[Copy Lyrics](https://github.com/Aimarekin/Aimarekins-Spicetify-Extensions)**, by **[Aimarekin](https://github.com/Aimarekin)**
- **[Spicy Lyrics](https://github.com/Spikerko/spicy-lyrics)**, by **[Spikerko](https://github.com/Spikerko)**
- **[Add to Multiple Playlists](https://github.com/JimMarley420/spicetify-extension)**, by **[JimMarley420](https://github.com/JimMarley420)**
- **[Sort Play](https://github.com/hoeci/sort-play)**, by **[hoeci](https://github.com/hoeci)**
- **[Play Without Context](https://github.com/JimMarley420/spicetify-extension)**, by **[JimMarley420](https://github.com/JimMarley420)**
- **[Playlist Smart Search](https://github.com/Yumppe/spicetify-playlist-smart-search)**, by **[Yumppe](https://github.com/Yumppe)**
- **[Play Next](https://github.com/daksh2k/Spicetify-stuff)**, by **[daksh2k](https://github.com/daksh2k)**
- **[Wave Player](https://github.com/03x1/Wave-Player)**, by **[03x1](https://github.com/03x1)**
- **[Waveform Playback Bar](https://github.com/Konsl/spicetify-extensions)**, by **[Konsl](https://github.com/Konsl)**

**Snippets**
- **[Hide Mini Player Button](https://github.com/Ender-Wang/marketplace)**, by **[Ender-Wang](https://github.com/Ender-Wang)**
- Hide now playing view button, by **[Resxt](https://github.com/Resxt)**
- **[Hide 'Scroll through previews'](https://github.com/Donaldino7712/marketplace)**, by **[Donaldino7712](https://github.com/Donaldino7712)**
- Hide What's New Button, by **[tsuliwaensis](https://github.com/tsuliwaensis)**
- Remove Popular sections from homepage, by **[SunsetTechuila](https://github.com/SunsetTechuila)**
- **[Rotating Cover Art](https://github.com/edicik/spicetify-marketplace)**, by **[edicik](https://github.com/edicik)**
- Remove Duplicated Fullscreen Button, by **[MigProPlayer](https://github.com/MigProPlayer)**


---

## Found this useful?<img src="https://media.tenor.com/23NitOvEEkMAAAAj/optical-illusion-rotating-head.gif" width="30"><br>

[![Follow Me <3](https://img.shields.io/badge/Follow%20Me%20%3C3-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/landnthrn)   
[![Find More of my Creations on GitHub](https://img.shields.io/badge/Find%20More%20of%20my%20Creations%20on%20GitHub-311A82?style=for-the-badge&logo=github&logoColor=white)](https://github.com/landnthrn?tab=repositories)  
[![Gists: landnthrn](https://img.shields.io/badge/Gists-311A82?style=for-the-badge&logo=github&logoColor=white)](https://gist.github.com/landnthrn)  
[![Discord: landn.thrn](https://img.shields.io/badge/Discord-311A82?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/users/831735011588964392)  
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-311A82?style=for-the-badge&logo=buymeacoffee&logoColor=white)](https://buymeacoffee.com/landn.thrn/extras)  
[![PayPal](https://img.shields.io/badge/PayPal-311A82?style=for-the-badge&logo=paypal&logoColor=white)](https://www.paypal.com/donate/?hosted_button_id=K4PLHFVBH7X8C)

![](https://github-view-counter-1-0-0.vercel.app/api?username=landnthrn-Goat-Spicetify-Setup-for-Spotify&label=false&bgColor=20164C&color=6a5acd&iconColor=6a5acd)
