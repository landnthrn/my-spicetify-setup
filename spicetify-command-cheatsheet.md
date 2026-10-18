# SPICETIFY COMMAND CHEATSHEET

- Run in PowerShell
- For commands that have <angle brackets>, replace them for what they state to have. 
  (e.g. `spicetify config current_theme <theme-folder-name>` --> ``spicetify config current_theme StarryNight`)
         

## VIEW CURRENT CONFIGURATION

```powershell
spicetify config
```

## INSTALLING & UPDATING

### INSTALL SPICETIFY & MARKETPLACE (OFFICIAL INSTALLER)

```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/cli/main/install.ps1 | iex
```

### INSTALL SPICETIFY VIA SCOOP

```powershell
scoop install spicetify-cli
```

### INSTALL SPICETIFY VIA WINGET

```powershell
winget install Spicetify.Spicetify
```

### INSTALL SPICETIFY VIA CHOCOLATEY

```powershell
choco install spicetify-cli
```

### INSTALL / UPDATE MARKETPLACE SEPARATELY

```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/marketplace/main/resources/install.ps1 | iex
```

### UPDATE SPICETIFY

```powershell
spicetify update
```

## UNINSTALLING 

### UNINSTALL SPICETIFY & MARKETPLACE

```powershell
spicetify restore

Remove-Item "$env:APPDATA\spicetify" -Recurse -Force
Remove-Item "$env:LOCALAPPDATA\spicetify" -Recurse -Force
```

### UNINSTALL MARKETPLACE ONLY

```powershell
Remove-Item "$env:APPDATA\spicetify\CustomApps\marketplace" -Recurse -Force
spicetify config custom_apps marketplace-
spicetify apply
```

### IF INSTALLED BY SCOOP

```powershell
spicetify restore
scoop uninstall spicetify-cli
```

### IF INSTALLED BY WINGET

```powershell
spicetify restore
winget uninstall Spicetify.Spicetify
```

### IF INSTALLED BY CHOCOLATEY

```powershell
spicetify restore
choco uninstall spicetify-cli
```

### TEST IF IT'S GONE

```powershell
spicetify
```

## BACKUP, RESTORE, RESET

### RESTORE TO BACKUP

```
spicetify restore
```

### MAKE BACKUP

```
spicetify backup
```

### RESET TO DEFAULT

```powershell
spicetify restore
spicetify backup
spicetify config current_theme SpicetifyDefault
spicetify apply
```

## LOCAL THEMES

### SET TO USE THEME FROM MARKETPLACE

```powershell
spicetify config current_theme marketplace
spicetify apply
```

### APPLY LOCAL THEME

```powershell
spicetify config current_theme <theme-folder-name>
spicetify apply
```

### UNAPPLY LOCAL THEME /  APPLY DEFAULT

```powershell
spicetify config current_theme SpicetifyDefault
spicetify config color_scheme default
spicetify apply
```

### APPLY LOCAL THEME COLOR SCHEME

```powershell
spicetify config color_scheme <the-[scheme-name]-mentioned-in-the-theme's-color.ini>
spicetify apply
```

### UNAPPLY LOCAL THEME COLOR SCHEME
```powershell
spicetify config color_scheme = # leave blank after '=' 
spicetify apply
```

## LOCAL EXTENSIONS

### CHECK APPLIED LOCAL EXTENSIONS

```powershell
spicetify config extensions
```

### APPLY LOCAL EXTENSIONS

```powershell
spicetify config extensions waveform.js 
```

*(if your file is *`.mjs`* and doesn't work after applying then rename it to *`.js`*)*

### UNAPPLY LOCAL EXTENSION

```powershell
spicetify config extensions waveform.js- # <-- Minus sign 
```

## LOCAL CUSTOM APPS

### CHECK APPLIED LOCAL CUSTOM APPS

```powershell
spicetify config custom_apps
```

### APPLY LOCAL CUSTOM APPS:

```powershell
spicetify config custom_apps history-in-sidebar
```

### UNAPPLY LOCAL CUSTOM APPS:

```powershell
spicetify config custom_apps nameofcustomappfolder- # <--Minus sign
```

## SPOTIFY DEV-TOOLS

## ENABLE DEV TOOLS

```powershell
spicetify enable-devtools
```

## DISABLE DEV TOOLS

```powershell
spicetify config always_enable_devtools 0
spicetify restart
```

## ERROR INFO

- On Spotify startup, if you see `Error initializing fullscreen.js extension. Top Bar Component not available.` it's likely just that Spicetify isn't up to date with the latest Spotify version. 