# NetSweeper: Network Rogue Device Detector

NetSweeper is a Python script designed to identify rogue devices in a network using Nmap.

## Description

NetSweeper is a powerful tool aimed at safeguarding your network infrastructure by detecting rogue devices that may compromise its security. With its intuitive interface and robust scanning capabilities, NetSweeper empowers network administrators to proactively identify unauthorized devices lurking within their network.

Using advanced techniques, NetSweeper conducts comprehensive scans of your network, pinpointing devices that deviate from the authorized inventory. Whether it's unauthorized computers, smartphones, IoT devices, or network peripherals, NetSweeper efficiently sifts through the network landscape, highlighting potential threats with precision.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/Elinvicto/NetSweeper.git

2. Install the required dependencies:
   ```sh
   pip install python-nmap

## Usage
 
1. Run the script by executing the following command:
   ```sh
   python NetSweeper.py

2. Follow the prompts to input the IP range to scan and the path to the file containing authorized devices.

3. Review the output to identify any rogue devices found on your network.

Note: Ensure that the file containing authorized devices contains each device's IP address on a separate line.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

You can copy this content into a file named `README.md` and place it in the root directory of your GitHub repository. Adjust the URLs, installation instructions, and other details as needed.
