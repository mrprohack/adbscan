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

```sh
sudo apt-get install libpcap0.8 libpcap0.8-dev libpcap-dev parallel masscan nmap adb -y
```

You also need to install the Python Shodan library:

```sh
pip install shodan
```
# Usage

To use adbscan, simply run the `adbscan.sh` script with two arguments
```sh
./adbscan.sh <directory_name> <max_parallel_jobs>
```
`<directory_name>` is the name of the directory that will be created to store the results of the scan. `<max_parallel_jobs>` is the maximum number of parallel ADB connections that will be attempted at once.

For example, to scan for Android devices on the network and create a directory named `scan_results` with a maximum of 10 parallel ADB connections, run:
