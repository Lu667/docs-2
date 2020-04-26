# Making connections in macOS

Make sure your connection is active \(blue\).

![](../../../.gitbook/assets/image%20%2815%29.png)

If you see the green "Connect" button, click on it and wait until it turns blue as shown above.

![](../../../.gitbook/assets/image%20%28377%29.png)

### Launch URL

You can see the connection URL and port, e.g. **localhost:33001**.  You can use this directly, or you can create a Launch URL to streamline certain operations if your browser supports application launching.  Application launching through the browser is more common on macOS. 



#### Launch URL for SSH

![](../../../.gitbook/assets/image%20%28145%29.png)

* \[username\] is only available for SSH connections.  It is the SSH username you specified.
* \[host\] is usually localhost, or 127.0.0.1.
* \[port\] is the port assigned to this connection.

## SSH Connections

* The SSH username is a user-configurable login name that will be included in the connection login string.  This setting only appears on SSH connections.  

![](../../../.gitbook/assets/image%20%28441%29.png)

* When you select the clipboard icon, the SSH string, including the supplied SSH Username, is copied to the clipboard.  You can then paste it into a terminal or command prompt to initiate an SSH connection.

![](https://github.com/remoteit/docs/tree/ac0b32dabd0132c644ae46ce3793623867217237/.gitbook/assets/image%20%28372%29.png)

* This is the "SSH string":

```text
ssh -l pi 127.0.0.1 -p 33002 -o "StrictHostKeyChecking=no" -o "UserKnownHostsFile /dev/null"
```

* Pasting that into a Windows 10 command prompt gives:

```text
C:\Users\me>ssh -l pi 127.0.0.1 -p 33002 -o "StrictHostKeyChecking=no" -o "UserKnownHostsFile /dev/null"
Warning: Permanently added '[127.0.0.1]:33002' (ECDSA) to the list of known hosts.
pi@127.0.0.1's password:
Linux raspberrypi 4.19.97-v7l+ #1294 SMP Thu Jan 30 13:21:14 GMT 2020 armv7l

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
Linux raspberrypi 4.19.97-v7l+ #1294 SMP Thu Jan 30 13:21:14 GMT 2020 armv7l

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Tue Mar 24 07:31:50 2020
pi@raspberrypi:~ $
```

You can use the SSH string in Linux and Mac terminal as well.

## VNC Connections

* When you select the clipboard icon, the VNC string is copied to the clipboard.  You can then paste it into your VNC application.

![](../../../.gitbook/assets/image%20%28245%29.png)

* This is the VNC string:

```text
127.0.0.1:33003
```

* This can be copied and pasted into the address bar of the RealVNC Viewer application.

![](../../../.gitbook/assets/image%20%2860%29.png)

* Provide the username and password to complete the VNC connection.

![](../../../.gitbook/assets/image%20%2836%29.png)

![](../../../.gitbook/assets/image%20%28456%29.png)

## Web connections

Select the arrow to launch the connection URL directly in your default browser.

![](https://github.com/remoteit/docs/tree/ac0b32dabd0132c644ae46ce3793623867217237/.gitbook/assets/image%20%28436%29.png)

![](../../../.gitbook/assets/image%20%28148%29.png)

