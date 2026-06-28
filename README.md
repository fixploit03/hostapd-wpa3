# hostapd-wpa3

Binary [hostapd](https://w1.fi/hostapd/) statik dengan dukungan WPA3 yang dapat dijalankan di semua distro Linux tanpa perlu menginstal dependensi tambahan.

## Konfigurasi AP

```bash
nano hostapd_wpa3.conf
```

Isi dengan:

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

## Jalankan AP

```bash
sudo hostapd hostapd_wpa3.conf
```
