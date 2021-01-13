# oktawateringhole
original project here - https://github.com/praetorian-inc/Okta_Watering_Hole but ships broken 

# Okta Watering Hole
### Authors: Alex Bainbridge, Robert Leonard

Okta Watering Hole is an automated tool for setting up an advanced Okta phishing campaign.

It supports a variety of options and should work out of the box to man in the middle all non-U2F 2FA factors. (If a given user has a U2F factor, they are prevented from using it on this phishing site)

Two servers will be created and running, as well as several supporting threads. Reserved ports are 443 and 4158 or (phish), if desired the port can be changed in the source.

*Note - The sessions thread can take a few minutes to quit due to the sleep timer


# Usage

```
Usage: Okta_Phishing_Setup.py [options] target_okta_url replace_okta_url cert.pem key.pem

ex. Okta_Phishing_Setup.py -q https://praetorianlabs.okta.com http://myphish.okta.com cert.pem key.pem

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -q, --quiet           don't print status messages to stdout
  -o LOG_FILE, --out-file=LOG_FILE
                        destination of log file for writing setup logs
  -g GO_PHISH, --go-phish=GO_PHISH
                        location of gophish listener
  -p PAYLOAD, --payload=PAYLOAD
                        location of payload to download to users desktop.
                        Named 'okta_web_update'
  -x EXTENSION, --extension=EXTENSION
                        extension for payload option. Default: 'exe
  -c CONTENT_TYPE, --content-type=CONTENT_TYPE
                        content type for payload. Default: 'application/octet-
                        stream'
```

