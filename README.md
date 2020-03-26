# PortScanner

Syntax for Scanner:


    scanner.exe [arg1] [arg2] [arg3] ... 
    
    
Argument Keys:


    hosts   - Required. Comma separated list of hosts. This can be computer name or IP address.
    ports   - Required. Comma separated list of ports, or one of the following preconfigured port lists:
                admin - 135, 139, 445, 3389, 5985, 5986
                web - 21, 23, 25, 80, 443, 8080
                top20 - 21, 22, 23, 25, 53, 80, 110, 111, 135, 139, 143, 443, 445, 993, 995, 1723, 3306, 3389, 5900, 8080
    timeout - Optional. Length of time in milliseconds for scanner to wait for a response. EX: 5000 = 5 seconds.
                Note: Lowest value is 500 milliseconds which it will default to if no value is given.
    outfile - Optional. File to write results out to on disk. Writes to current folder if none provided. Slows scanning.
              If no file is specified, output will be written to the console.


Example Usage:


    Scan 127.0.0.1 and localhost for ports 21, 22, and 23, with a 5 second timeout.
        scanner.exe hosts=127.0.0.1,localhost ports=21,22,23 timeout=5000
    
    Scan 127.0.0.1 for for the ports defined in the preconfigured "admin" port list.
        scanner.exe hosts=127.0.0.1 ports=admin
