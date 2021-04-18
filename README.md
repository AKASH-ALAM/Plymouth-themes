# Plymouth-themes
Apple Macintosh Plymouth Themes

### How to Install Plymouth System Boot Theme on Ubuntu 20.04

If you want to take a fresh look at the Ubuntu boot screen, just install the new plymouth themes in the
/usr/share/plymouth/themes directory. But not all topics can be set in this way.
In this instruction, I will try to help avoid some errors when replacing the standard system boot theme
with a custom one.

### Install a new boot screen in Ubuntu
Some users do not really like the standard download theme, so they look for alternatives and install third-


To change Boot Splash Screen in Ubuntu, you rst need to select a new theme from gnome-look.org.
Download your favorite theme from the link above, unzip it and copy it to the
/usr/share/plymouth/themes directory, for example from the terminal

     sudo cp -r darwin /usr/share/plymouth/themes/
    
Now in the terminal, install the new Plymouth theme as the default theme using the command below.

    sudo update-alternatives --install
    /usr/share/plymouth/themes/default.plymouth default.plymouth
    /usr/share/plymouth/themes/darwin/darwin.plymouth 100
    
You need to replace “darwin/darwin.plymouth” with the original path and le name of your theme.
Then run the following command

    sudo update-alternatives --config default.plymouth
  
And change the default theme to yours (in my case it’s number 2) by entering the theme number
And the last one. For the changes to take effect, you need another team

    sudo update-initramfs -u
    
After that, restart the Ubuntu system to check the new boot screen.

Now that you know how to install and change the Plymouth theme, let’s take a look at some of the ones
on the gnome-look website.
