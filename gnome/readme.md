## Run command line one system load

go into `~/.config/autostart/` and create a file with a `.desktop` extension.

File example : 
```desktop
[Desktop Entry]
Name=MyScript
GenericName=A descriptive name
Comment=Some description about your script
Exec=/path/to/my/script.sh
Terminal=false
Type=Application
X-GNOME-Autostart-enabled=true
```
