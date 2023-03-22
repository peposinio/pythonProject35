# pythonProject35


import socket

for port in range(2259,2262):
    x = socket.socket()
    x.settimeout(1)

    try:
        x.connect(("172.30.230.69", port))
        print(f"the port {port} is open")
        print ("Port: %s => service name: %s" %(port, socket.getservbyport(port, protocolname))) 
    except:
       print(f"the port {port} is close")
    finally:
        x.close
