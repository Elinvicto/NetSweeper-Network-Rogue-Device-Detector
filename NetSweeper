import nmap

def discover_devices(ip_range):
    nm = nmap.PortScanner()
    nm.scan(hosts=ip_range, arguments='-sn')
    return nm.all_hosts()

def scan_ports(device):
    nm = nmap.PortScanner()
    nm.scan(hosts=device, arguments='-p-')  # Scan all ports
    return nm[device]['tcp'].keys()

def identify_rogue_devices(ip_range):
    authorized_devices = ['192.168.1.1', '192.168.1.2']  # Replace with your authorized device IPs
    discovered_devices = discover_devices(ip_range)
    
    rogue_devices = []
    for device in discovered_devices:
        if device not in authorized_devices:
            open_ports = scan_ports(device)
            if open_ports:
                rogue_devices.append((device, open_ports))
    
    return rogue_devices

def main():
    ip_range = '192.168.1.0/24'  # Replace with your network IP range
    rogue_devices = identify_rogue_devices(ip_range)
    
    if rogue_devices:
        print("Rogue Devices Found:")
        for device, ports in rogue_devices:
            print(f"Device IP: {device}, Open Ports: {ports}")
    else:
        print("No rogue devices found.")

if __name__ == "__main__":
    main()
