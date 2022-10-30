# Youtube for Roku
Unofficial Youtube client for Roku.

## Features
- No Ads (I guess that's a feature)
- Privacy driven (uses Invidious backend)
- SponsorBlock integration (skips undesirable sections in videos)

## Installation

### Enable Roku Developer Mode
First, you need to enable developer mode on your Roku TV (if you have not done that already).

Using your Roku remote, enter the following sequence:

![DevSequence](https://image.roku.com/ZHZscHItMTc2/dev-startup1.png)

For full instructions, see [Steps to set up the development environment](https://developer.roku.com/en-ca/docs/developer-program/getting-started/developer-setup.md)

### Gather your info
By now, you show have the following
- Your Roku Dev password (setup in the previous step)
- Your Roku TV local IP address
  - You can find this information in your TV network settings. It should look like 192.168.X.X or so

### Install Youbtube for Roku

Install Youbtube for Roku as a dev channel using this command, and replace:
- `REPLACE_PASSWORD_HERE` : with your Roku Dev password
- `REPLACE_IP_ADDRESS_HERE` : with your Roku TV local IP address
```
curl -OL https://github.com/iBicha/roku-youtube/releases/download/v0.1.0/roku-youtube.zip && \
	curl --user rokudev:REPLACE_PASSWORD_HERE --digest --silent --show-error -F "mysubmit=Install" -F "archive=@./roku-youtube.zip" --write-out "%{http_code}" http://REPLACE_IP_ADDRESS_HERE/plugin_install
```
If successful, you should see some output on your terminal, ending with 200%.

You should see a new channel on your Roku TV, with "Roku Developers" Logo (we'll get this thing a logo)
