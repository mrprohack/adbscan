# adbscan

adbscan is a Bash script that scans for Android Debug Bridge (ADB) devices using Shodan and connects to them for further testing. 

## Prerequisites

Before running the script, make sure the following tools are installed:

- [libpcap0.8](https://packages.debian.org/stretch/libpcap0.8)
- [libpcap0.8-dev](https://packages.debian.org/stretch/libpcap0.8-dev)
- [libpcap-dev](https://packages.debian.org/stretch/libpcap-dev)
- [parallel](https://www.gnu.org/software/parallel/)
- [masscan](https://github.com/robertdavidgraham/masscan)
- [nmap](https://nmap.org/)
- [adb](https://developer.android.com/studio/command-line/adb.html)

You can install these dependencies on Debian-based systems using the following command:

sudo apt-get install libpcap0.8 libpcap0.8-dev libpcap-dev parallel masscan nmap nload adb -y

## Installation

To use My Project, you will need to install Python 3 and the following libraries:

- pandas
- requests

Once you have these installed, you can run the project by typing the following command in your terminal:

`python3 myproject.py`
