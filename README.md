# PolyBar_Autohide
Polybar is a beautiful bar but in some cases for example if you have a small screen it might take too much space so I've made a simple script that hide Polybar when there are windows in the current workspace, the script shows the bar if you move the cursor where the bar is or if you don't have any windows in the workspace that you're using.

# How to Install
1. Clone the git repo in your home: 
     ```
     git clone https://github.com/arkeane/polybar_autohide.git ~/polybar_autohide
     ```
     - Install nedeed software: `polybar` `xdotool` `xdo`

2. Move to the script directory `cd ~/polybar_autohide`
     
3. Make adjustments to the script
     - You can adjust polybar_height definition to change sensibility.
     - You can also change paths but be carefull!!!

4. Compile the script `g++ polybar_autohide.cpp -o autohide -lX11`

5. Autostart the script
     - Add the `autohide` file to your autostart system
          - If you use i3wm add this to your config file, change $USER with your username:
               ```
               exec --no-startup-id /home/$USER/polybar_autohide/autohide
               ```
          - If not just use your usual autostart system.
     - The script create a file `~/.windowlist` for the windowcounter function DO NOT DELETE.

# How to use Hotkeys
1. The program automatically create a file `~/.togglefile` that contains a value (0) read by the script DO NOT DELETE.

2. To use the toggle you have to bind the script `~/polybar_autohide/toggle.sh` with wathever you want
     - Remember to run `chmod u+x ~/polybar_autohide/toggle.sh` to make it executable
     - For i3wm users add thi to your config file, change $USER with your username and the binding if you want:
          ```
          bindsym $mod+Shift+p exec --no-startup-id /home/$USER/polybar_autohide/toggle.sh
          ```
     - For other users, bind the script with your favourite binding system 

# Known Problems (working on)
- Dual monitor setup works but in a strange way 
- Trying to convert all the shell commands to c++ syntax to avoid external programs
- Multiple bars support


If you want to support me [PayPalMe](paypal.me/LudovicoPestarino)
