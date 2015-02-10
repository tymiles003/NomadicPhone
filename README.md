Nomadic Phone - The webphone for Digital Nomads
===============================================

This is a **quick prototype** of a web application build with the Twilio API.

Why use this webapp?
--------------------

### You are a digital nomad, you travel around the world and you work remotely.

- Use a real phone number to manage your business
- Make a phone call in your home country directly from your web browser
- Send and receive SMS from the browser
- Email notification when you got a phone call or a SMS
- Choose what you want to do on incoming calls:
  - Send everything to the voicemail
  - Redirect the call to another phone number, for example a local prepaid phone
  - Answer directly to the call inside your browser

### You are minimalist, you don't use a mobile phone but you need a phone number for banks and public services

- Yes, it's possible to live without a mobile phone!
- Prepaid plans are so expensive, especially in Canada if you compare to Twilio pricing (Telus = $0.30/min and Twilio = $0.02/min)

### You live in many countries, you need to have a local phone number for each one

- For example, I have a bank account in France and another one in Canada, so I need a local phone number for each country
- I want to call my family from oversea but I don't like Skype and my mum doesn't know how to use Skype, my mum can use a real phone...
- Use a local Twilio phone number for each country and make calls locally with your browser

Features
--------

- No dependency (copy/paste/edit config file)
- Handle incoming calls: send to the voicemail, redirect to another number, answer from the webapp
- Make a call from the browser (use Flash or WebRTC)
- Calls history
- Listen recordings from the browser (HTML5 audio)
- Send a SMS to any phone number
- Receive SMS (only for some countries)
- Email notification when you got a call or a new SMS
- Display GeoLocation of SMS and calls when possible
- Access protected by a password (HTTP Basic Authentication)
- Free Software (License GPLv2)

Requirements
------------

- A webserver to host PHP scripts
- PHP >= 5.3
- PDO (Sqlite)
- HTML5 browser
- Headphone or integrated micro (works on a Macbook Air)
- Twilio Account

Todo
----

- Add a blacklist
- Add contacts
- Choose how to handle an incoming call when a contact call you
- At the moment, this project is a quick and dirty PHP script :)
- Make a real webapp, not just a proof of concept

Installation
------------

1. Create a Twilio account and a Twilio Application (You can try with their trial mode)
2. Setup your Twilio Application

  - Voice request URL: http://yourwebsite/?handler=receive-call
  - Voice status callback URL: http://yourwebsite/?handler=callback-call
  - SMS request URL: http://yourwebsite/?handler=receive-sms
  - SMS status callback URL: http://yourwebsite/?handler=callback-sms

3. Copy all PHP scripts inside the directory of your choice
4. Make this directory writeable
5. Change values inside the file config.php
6. Enjoy!

Screenshots
-----------

### Incoming calls

![Incoming Calls](https://raw.github.com/fguillot/NomadicPhone/master/screenshots/incoming_calls.png "Incoming calls")

### Make a call

![Make a call](https://raw.github.com/fguillot/NomadicPhone/master/screenshots/make_call.png "Make a call")

### Calls history

![Calls history](https://raw.github.com/fguillot/NomadicPhone/master/screenshots/calls_history.png "Calls history")

### Send a SMS

![Send a SMS](https://raw.github.com/fguillot/NomadicPhone/master/screenshots/send_sms.png "Send a SMS")

### SMS history

![SMS history](https://raw.github.com/fguillot/NomadicPhone/master/screenshots/sms_history.png "SMS history")
