# Making connections in Windows

Make sure your connection is active \(blue\).

![](../../../.gitbook/assets/image%20%2820%29.png)

If you see the green "Connect" button, click on it and wait until it turns blue as shown above.

![](../../../.gitbook/assets/image%20%28430%29.png)

### Launch URL

You can see the connection URL and port, e.g. **localhost:33001**.  You can use this directly, or you can create a Launch URL to streamline certain operations if your browser supports application launching.  Application launching through the browser is more common on macOS. 

#### Launch URL for SSH

![](../../../.gitbook/assets/image%20%28168%29.png)

* \[username\] is only available for SSH connections.  It is the SSH username you specified.
* \[host\] is usually localhost, or 127.0.0.1.
* \[port\] is the port assigned to this connection.

## SSH Connections

* The SSH username is a user-configurable login name that will be included in the connection login string.  This setting only appears on SSH connections.  

![](../../../.gitbook/assets/image%20%28354%29.png)

Select the clipboard icon as shown:

![](../../../.gitbook/assets/image%20%28417%29.png)



The SSH string, including the supplied SSH Username, will be copied to the clipboard.  You can then paste it into a terminal or command prompt to initiate an SSH connection.  The SSH String is not the same as the editable Launch URL which only works if your browser supports that protocol.

![](../../../.gitbook/assets/image%20%28456%29.png)

* This is the "SSH string" \(assuming you entered "pi" as the SSH username\):

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

![](../../../.gitbook/assets/image%20%2834%29.png)

* This is the VNC string:

```text
127.0.0.1:33003
```

* This can be copied and pasted into the address bar of the RealVNC Viewer application.

![](../../../.gitbook/assets/image%20%28439%29.png)

* Provide the username and password to complete the VNC connection.

![](../../../.gitbook/assets/image%20%28327%29.png)

![](../../../.gitbook/assets/image%20%28263%29.png)

## Web connections

Select the arrow to launch the connection URL directly in your default browser.

![](../../../.gitbook/assets/image%20%28533%29.png)

![](../../../.gitbook/assets/image%20%28166%29.png)

