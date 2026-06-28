# hostapd-wpa3

A static [hostapd](https://w1.fi/hostapd/) binary with WPA3 support that can be run on any Linux distribution without the need to install additional dependencies.

## AP Configuration

```bash
nano hostapd_wpa3.conf
```

Add the following content:

```bash
interface=wlan0
driver=nl80211
ssid=hostapd-wpa3
hw_mode=g
channel=6
wpa=2
sae_password=12345678
wpa_key_mgmt=SAE
rsn_pairwise=CCMP
ieee80211w=2
```

## Run the AP

```bash
sudo ./hostapd hostapd_wpa3.conf
```

Or run it using the script:

```bash
Usage: sudo ./hostapd-wpa3 <interface> <ssid> <channel> <password>
```
