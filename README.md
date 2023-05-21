# rc-car-1
simple rc car using ESP8266 and L298n

Based on https://www.youtube.com/watch?v=gsM5tWcCq9E but using ESPAsyncWebServer lib on pleateform.io  with vscode.

Note that it uses a static IP address, you might want to change it

Once the code is uploaded on the nodeMCU board it should run the webserver on port 80 using the static IP address (192.168.100.101 by default).

You can now drive the car using simple http request.

for instance using curl :
```
 curl http://192.168.100.101/?state=S
```
make the car go front then
```
 curl http://192.168.100.101/?state=S
```
make the car stop.

Once you made that working, we will like to allow anyone to be able to drive the car from anywhere on internet, provided we grant him the permission.

For this we need to install on a device running on the same LAN the ubiqity zone controler.

It is a program that will manage all the devices on the same local network and communicate with the ubiqity network to allow deploy applications that use the devices.