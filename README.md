flask-relay-control
===================

It's a small script to simply control attached relays over HTTP.

----------

![Screenshot](https://github.com/ycbayrak/flask-relay-control/blob/master/screenshot.png)

Install Guide
-------------
Clone the repository. 
```
git clone https://github.com/ycbayrak/flask-relay-control.git
```
Globally install Flask and RPi.GPIO libraries from **pip** or use **virtualenv**.
```
pip install flask rpi.gpio
pip install virtualenv
```
You may need supervisor to automating launcher script. You can find the **launcher.sh** and the **relay-control.conf** in the root directory.
```
pip install supervisor
```
Wiring Guide
------------------
In **main.py** file you will notice the **pins** dictionary it takes the **GPIO.BCM** number as the key. You can add your *PINS* directly to the **pins** dictionary with value containing **{name: string, state: boolean, status: string}**

A few notes about Launcher
------------------------------------------------
In **launcher.sh** you will notice the git commands for the repository. It automatically check out the master branch and updates the source code.


Start Controlling the Relays
----------------------------------------
Navigate to the **http://raspberrypi.local:8000** and start switching the relays.