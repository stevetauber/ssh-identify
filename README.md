ssh-identify
============

Changes color of your Mac OS X terminal based on which system you SSH to

Thanks to http://www.rngtng.com/ for the tabc code.

Setup
=====

1. Copy dotprofile into your .profile or .bash_rc file
2. Edit .tabc to your liking
3. Create new Terminal Settings.  You'll need one named SSH, one named Default, and one for reach Profile you've created.

How it Works
============

This script uses a configuration file (.tabc) that has a list of Profiles and Systems.  When you SSH, the script looks through your systems (which can also be SSH short names).  If it finds a match, the profile is used to change your terminal color scheme; if no match is found, it uses a default SSH setting.  When you quit, it reverts to a setting named Default.

In the .tabc provided, there are three (3) Profiles: Staging, Production, Logging.  In terminal, I'll create a few new Settings.
First, I go to Terminal -> Preferences, then click on the Settings tab.  I create new settings named Default, Staging, Production, Logging, and SSH.

If I type `ssh staging', then the terminal window would use the Staging settings.  If I typed `ssh me@othercompany.example.com' it would use the SSH terminal settings.  When I quit, then it uses Default terminal settings.

Common Errors
=============

Ensure that at a minimum Default and SSH terminal settings exists. You'll also want to create a terminal setting for reach Profile you have.  Lastly, keep in mind you can use SSH short names as well as fqdn or user@fqdn.  I highly recommend using SSH short names since it simplifies your settings file.