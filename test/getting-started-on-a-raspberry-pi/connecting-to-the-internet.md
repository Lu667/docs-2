# Connecting to the internet

## Setting up your network connection

Before you are able to connect to remote.it and access your Pi from anywhere securely, you need to connect your Pi to the internet.

You have **three options** when it comes to setting up your Pi to access the internet.

### Ethernet setup

The simplest option is to plug an ethernet cord from your Pi to your router so it is hard wired to your network. If that is your planned method of connecting your Pi to the internet, feel free to skip to the bottom of this page!

Using ethernet to your modem is the most reliable way to setup but means your Pi has to be plugged into your router which is not always possible or feasible. In that case, keep reading!

### Wifi setup

A common option is to connect your Pi to wifi so you can have it located anywhere your wifi network has coverage.

To do this, the easiest way is to use the built in `raspi-config` command which allows you to configure many things on your Pi. To do so, run:

```bash
sudo raspi-config
```

Then, using your keyboard arrows for navigation, do the following:

1. Arrow down to “Network Options”
2. Select “Wi-Fi” by hitting `enter` \(or `return`\)
3. Select your country \(if you're in the United States, select `US`\)
4. Type your network’s SSID \(e.g. the name of your Wifi network\)
5. Type your network password \(or leave blank if you’re on an open network\)
6. Save this and then arrow too "Finish"

Now you should be connected to your Wifi network, congrats!

{% hint style="info" %}
Once WiFi is configured your Pi may no longer be available at [raspberrypi.local](http://raspberrypi.local). 

If you need to reconnect to your Pi before you have remote.it installed you will need to make note of its IP address. 

This can be found by running `ifconfig` and searching for it at the [top of the output](https://stackoverflow.com/questions/8529181/which-terminal-command-to-get-just-ip-address-and-nothing-else).
{% endhint %}

### Celular modem

One of the key benefits of using remote.it is that we fully support connections over cellular networks. This enables you to deploy products anywhere in the world that has access to cellular and by using a cellular modem or hotspot, you will be able to securely remote access and control your devices from anywhere!

Setup is similar to the WiFi setup above, only you will configure setup to attach to a local hot-spot or cellular modem instead of a wifi router connected to DSL/Cable/Fiber.

## Check your network connection

To check that you are connected to the internet, try pinging Google:

```bash
ping google.com
```

You should see a bunch of output like this:

```bash
64 bytes from 172.217.6.78: icmp_seq=0 ttl=52 time=14.868 ms
64 bytes from 172.217.6.78: icmp_seq=1 ttl=52 time=20.153 ms
64 bytes from 172.217.6.78: icmp_seq=2 ttl=52 time=18.833 ms
```

If you see a lot of `timeout` messages, that means that you're not connected and you'll need to try and diagnose why you can't connect to your network.

To close `ping`, type `Ctrl + c`.

If you aren't able to connect to the internet, try the following:

1. Make sure your SSID and password are correct
2. Make sure your network doesn't have firewalls or other security measures in place \(sometimes corporate or public networks will have various security measures in place that make it more challenging to configure your device\)

If none of this helps, [please let us know](https://remot3it.zendesk.com) and we will try and help you troubleshoot!

Now, after all this hopefully you are ready to setup remote.it on your Pi!



