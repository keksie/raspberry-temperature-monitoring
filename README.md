# RaspberryPi temperature-monitoring
Monitor Raspi's Temperature and shut down on critical values.

Originally from https://quaintproject.wordpress.com/2013/09/14/alert-mail-raspberry-pi/ tweaked to enable shutdown at critical temperature.


## To make this as a cronjob running every 30 min do this

mkdir -p ~/scripts
vi ~/scripts/monitoring.py

paste the code from the script above.


Then crontab -e and add this:

30 * * * * python ~/scripts/monitoring.py
close crontab editor (ctrl-x if nano or esc, then :wq if vim)
