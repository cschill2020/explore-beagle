# Setting up Beaglebone Black in 2024 :)

# Grab latest image:
# https://www.beagleboard.org/distros
# AM335x 11.7 2023-09-02 4GB eMMC IoT Flasher

# Install WiFi drivers
# bash wifi_drivers.sh
# Should see wlan0 appear in 'ip a'

# Setup connection to WiFi AP by modifying wpa_supplicant: /etc/wpa_supplicant/wpa_supplicant-wlan0.conf
# https://docs.beagleboard.org/latest/boards/beagleplay/demos-and-tutorials/connect-wifi.html
network={
  ssid="your ap"
  psk="your pwd"
  proto=RSN
  key_mgmt=WPA-PSK
  pairwise=CCMP TKIP
  group=CCMP TKIP
}

