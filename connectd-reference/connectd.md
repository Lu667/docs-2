# connectd

## **Download remote.it**

```bash
wget https://github.com/remoteit/misc_bins_and_scripts/raw/master/connectd/connectd.x86_64-osx
chmod u+x connectd.x86_64-osx
mv connectd.x86_64-osx /usr/local/bin/connectd
```

* [ ] Make this into a one liner that supports OSX, Windows, Ubuntu, Debian, etc…
* [ ] Release versions of connectd on public Github repo

## Running connectd

```bash
connectd -c \
  BASE_64_USER \
  BASE_64_PASSWORD \
  DEVICE_UID \
  BIND_PORT \
  ENCRYPTION_MODE \
  LOCAL_HOST_ADDRESS \
  MAX_OUTSTANDING
```

### Options

| Option | Description |
| :--- | :--- |
| `BASE_64_USER` | Your Base64 encoded username \(probably your email\) |
| `BASE_64_PASSWORD` | Your Base64 encoded remote.it password |
| `DEVICE_UID` | The ID \(also called address\) of the device you want to connect to |
| `BIND_PORT` | The port you want to bind the connection to on your local machine \(eg 3000\) |
| `ENCRYPTION_MODE` | The level of encryption to use. Choices are: `1` or `2` |
| `LOCALHOST_ADDRESS` | The address to bind to on your local network. This is normally either 127.0.0.1. |
| `MAX_OUTSTANDING` |  |

#### Example: 

```bash
connectd -c \
  eW91cm5hbWVAZXhhbXBsZS5jb20= \   # Base64 encoded username/email
  c3VwM3JzZWtyZXQh \               # Base64 encoded password
  80:00:00:00:00:00:00:F1 \        # Device ID on remote.it
  T3000 \                          # Port to bind to, prefixed with "T"
  1 \                              # Encryption mode (1 or 2)
  127.0.0.1 \                      # Localhost address
  12                               # Max outstanding
```

### **Other options**

* `-d` run in daemon mode, meaning keep the connection running in the background

