# Chrome Domoticz

This is a small python script using pychromecast to propegate status from my chromecast devices into domoticz and nodered, for further processing

It also implement a simple webservice to control the chromecast, which I have used in a companion dashboard

It is a quick hack at the moment, but it works for me.. If implementing this elsewehere, go through the code and update urls etc.

The listed audio / video streams (in chrome.py) is mainly for some danish tv/radio channels

the included Dockerfile can be used to build a docker image, with the following command


```
docker build -t chromecast-integrator .
```

afterwards start it with 

```
docker run --name chromecast --restart unless-stopped -v /opt/chromecast:/config -d -t --net=host -p8181:8181 chromecast-integrator
```
