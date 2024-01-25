### Change input options
```
gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Alt>Shift_L']"
gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Shift>Alt_L']"
gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']"
```

### Reset icons
```
gsettings reset org.gnome.shell app-picker-layout
```

### Refresh app icons layout
```
gsettings set org.gnome.shell app-picker-layout "[]" 
```
Alternatively, you can put value [] on app-picker-layout of org/gnome/shell using dconf-editor.

### Isolate workspaces 
```
gsettings set org.gnome.shell.app-switcher current-workspace-only true
```

### Only icons while Alt-TAB 
```
gsettings set org.gnome.shell.window-switcher app-icon-mode 'app-icon-only'
```

### Privacy settings
```
gsettings set org.gnome.desktop.privacy disable-camera true 
gsettings set org.gnome.desktop.privacy disable-microphone true 
gsettings set org.gnome.desktop.privacy remember-recent-files false 
gsettings set org.gnome.desktop.privacy remember-app-usage true
```