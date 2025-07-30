````markdown name=README.md
# Wifite

**Wifite** is an automated wireless attack tool written in Python. It is designed to simplify the process of auditing WiFi networks by automating the steps required to capture handshakes and perform attacks against WEP/WPA/WPA2 encrypted networks.

## Features

- Scans for nearby WiFi networks in monitor mode
- Supports WEP, WPA, WPA2, and WPS encrypted networks
- Automatically captures handshakes for WPA/WPA2 networks
- Automates the process of cracking captured handshakes using various tools (e.g., aircrack-ng, pyrit, cowpatty, tshark)
- Supports multiple wireless interfaces
- User-friendly command-line interface

## Requirements

- Python 2.7 or 3.x
- Wireless card capable of monitor mode and packet injection
- External tools such as:
  - `aircrack-ng`
  - `pyrit`
  - `reaver`
  - `bully`
  - `tshark`
  - `cowpatty`

## Installation

Clone the repository and install any dependencies:

```bash
git clone https://github.com/derv82/wifite2.git
cd wifite2
sudo python setup.py install
```

Or run directly:

```bash
sudo python ./wifite.py
```

> **Note:** You must run Wifite as root for full functionality.

## Usage

Start scanning and attacking nearby WiFi networks:

```bash
sudo wifite
```

Common arguments:

- `-i <interface>`: Specify wireless interface (e.g., wlan0)
- `--kill`: Kill interfering processes
- `--no-wpa`: Do not attack WPA networks
- `--no-wep`: Do not attack WEP networks
- `--wps`: Only attack WPS networks

Example:

```bash
sudo wifite -i wlan0 --wps
```

## Disclaimer

This tool is intended for educational and authorized penetration testing purposes only. Unauthorized use against networks without permission is illegal.

## Contributing

Pull requests and improvements are welcome! Please file issues for bugs or suggestions.

## License

[GNU General Public License v2.0](LICENSE)

## References

- [Official repository](https://github.com/derv82/wifite2)
- [Aircrack-ng Suite](https://www.aircrack-ng.org/)

````
