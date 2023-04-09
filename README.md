# adbscan

adbscan is a Bash script that scans for Android Debug Bridge (ADB) devices using Shodan and connects to them for further testing. 

## Prerequisites

Before running the script, make sure the following tools are installed:

- [adb](https://developer.android.com/studio/command-line/adb.html)
- [nmap](https://nmap.org/)
- [masscan](https://github.com/robertdavidgraham/masscan)
- [parallel](https://www.gnu.org/software/parallel/)
- [libpcap0.8](https://packages.debian.org/stretch/libpcap0.8)
- [libpcap0.8-dev](https://packages.debian.org/stretch/libpcap0.8-dev)
- [libpcap-dev](https://packages.debian.org/stretch/libpcap-dev)





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
adbscan --install
adbscan --shodan <directory_name> <max_parallel_jobs>
adbscan --masscan <directory_name> <max_parallel_jobs>
adbscan --pipe shell id
cat file | adbscan --connect <max_parallel_jobs>
adbscan --test id
```
`<directory_name>` is the name of the directory that will be created to store the results of the scan. `<max_parallel_jobs>` is the maximum number of parallel ADB connections that will be attempted at once.

For example, to scan for Android devices on the network and create a directory named `scan_results` with a maximum of 10 parallel ADB connections, run:

```sh
./adbscan.sh scan_results 10
```

# Disclaimer

This tool is intended for educational and research purposes only. The authors are not responsible for any misuse or damage caused by this tool. Use it at your own risk.


