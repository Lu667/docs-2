# Device Setup for Auto Registration

#### Clean Preparation for Single Use <a id="Clean-Preparation-for-Single-Use"></a>

 Use these published instructions to [setup a new RPi](https://docs.remote.it/platforms/quick-start-on-raspberry-pi/setup-your-raspberry-pi) with the [remote.it](http://remote.it) package.

{% hint style="warning" %}
 **NOTE:** Do not use the interactive connectd\_installer script to set up Services when using Auto Registration. They are not needed and will cause problems if cloned without removing these Services first.
{% endhint %}

If you have previously installed the connectd package on your Pi, remove it, including all provisioning \(configuration\) files with the following command:

```text
sudo dpkg --purge connectd
```

### Download the connectd 2.5.37 package. 

Now, install the connectd package following [these instructions](../../platforms/all-other-linux-flavors.md).

Copy and save the Bulk Identification Code.

{% hint style="info" %}
The Bulk Identification Code is an alphanumeric string that identifies a specific Product Definition. It must be copied to the file /etc/connectd/bulk\_identification\_code.txt on your target device’s master OS image.
{% endhint %}

 Back on the Products page, click on the ![:info:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/info_32.png) icon in the row corresponding to your desired Product Definition to select the Bulk Identification Code, save it and prepare to write it on the device to prepare the master SD card \(later in this document\).

![](../../.gitbook/assets/image%20%28258%29.png)

![](../../.gitbook/assets/image%20%28275%29.png)

#### OEM Configuration <a id="OEM-Configuration"></a>

{% hint style="warning" %}
**NOTE:** only required for non-Raspberry Pi platforms
{% endhint %}

```text
sudo vi /etc/connectd/oem_settings
```

Change the expression for system ID like … cpuid=$\(hostname\) \(OEM example\)

Change the registration key method to use … interface='enp3s0' \(Ubuntu example\)

Please contact [support@remote.it](mailto:support@remote.it) if you are not sure what to do here.





