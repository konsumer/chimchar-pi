<img height="100" src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/390.png" align="right" />

# chimchar-pi

This is a hardware platform I use for my pi-based projects.

Here are some projects that use it:

- [chimchirpi](https://github.com/konsumer/chimchirp) - A puredata-based synthesizer
- [pakemon](https://github.com/notnullgames/pakemon) - A network/radio hacking platform that feels like a videogame!

## hardware

I Have this hardware, so I designed it around this, but it should work with other combos, with a little hacking:

- [pizero2w](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/)
- [GPi Case](https://retroflag.com/GPi-CASE.html)
- [USB hub](https://www.amazon.com/LoveRPi-MicroUSB-Port-Black-Raspberry/dp/B01HYJLZH6/ref=sr_1_4?keywords=Pi+Zero+USB&qid=1645331418&sr=8-4) that plugs into port in back of GPi (hiding in battery compartment)

## software

For the above combo of hardware, you will need:

- the latest rasperry pi os lite. Use rasperry pi imager, choose "raspberry pi os lite (32-bit)", make sure to click gear icon and add wifi, ssh & user
- add my [GPi patches](gpi-pizero2w/boot)
- add `logo.nologo` to /boot/cmdline.txt
- install safe shutdown: `wget -O - "https://raw.githubusercontent.com/RetroFlag/retroflag-picase/master/install_gpi.sh" | sudo bash`
- [install retropie](https://retropie.org.uk/docs/Manual-Installation/). Make sure to also [start it at boot](https://retropie.org.uk/docs/FAQ/#how-do-i-boot-to-the-desktop-or-kodi) Although this is a great way to play retro-games, it's also a nice menu interface for pi that only has controller input, so we use this for the UI.
- `sudo raspi-config nonint do_boot_wait 0` to make it boot a bit faster

Additionally:

- boot quicker into emulationstation
- [nice mods](https://www.youtube.com/watch?v=jOZ-ZQHMOII)