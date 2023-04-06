adbscan
adbscan is a bash script that uses Shodan and ADB to scan for Android devices with ADB enabled on a network.

Requirements
To use adbscan, you need to have the following tools installed on your system:

libpcap and libpcap development libraries
masscan
nmap
parallel
nload
In addition, you need to have ADB installed and configured on your system.

You can install these dependencies on Ubuntu/Debian using the following command:

arduino
Copy code
sudo apt-get install libpcap0.8 libpcap0.8-dev libpcap-dev parallel masscan nmap nload adb -y
You also need to install the Python Shodan library:

Copy code
pip install shodan
Usage
To use adbscan, simply run the adbscan.sh script with two arguments:

php
Copy code
./adbscan.sh <directory_name> <max_parallel_jobs>
<directory_name> is the name of the directory that will be created to store the results of the scan. <max_parallel_jobs> is the maximum number of parallel ADB connections that will be attempted at once.

For example, to scan for Android devices on the network and create a directory named scan_results with a maximum of 10 parallel ADB connections, run:

bash
Copy code
./adbscan.sh scan_results 10
Disclaimer
This tool is intended for educational and research purposes only. The authors are not responsible for any misuse or damage caused by this tool. Use it at your own risk.
