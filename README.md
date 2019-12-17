# buster-setup

___

## Latest firefox installation and settings

Source @ [LINUX UPRISING](https://www.linuxuprising.com/2019/12/how-to-install-latest-firefox-non-esr.html)

```
# Unstable repo
echo "deb http://deb.debian.org/debian/ unstable main contrib non-free" | sudo tee -a /etc/apt/sources.list

# Stable is default Unstable needs to be manually installed
sudo printf "Package: *\nPin: release a=stable\nPin-priority=900\n\nPackage: *\nPin: release a=stable\nPin-priority=10" > /etc/apt/preferences.d/99pin-unstable

sudo apt-update && sudo apt uprade -y

sudo apt install -t unstable firefox -y

sudo apt purge firefox-esr
```

