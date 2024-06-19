# Minecraft-Server-Documentation
## Making a Minecraft server using raspberry pi

By: James

### Step 1
Check for updates
```
sudo apt update
sudo apt upgrade
sudo reboot
```
### Step 2
Install Java
```
sudo apt install openjdk-17-jdk
```
### Step 3
Create a directory for the Minecraft server
```
mkdir minecraft-server
cd minecraft-server
```
### Step 4
Download the Minecraft server JAR file
* you can do this by going to  the official Minecraft server download page and copy the link for the latest server JAR file.
* You can also go to a site like MCJars to get older server.jar files
### Step 5
Move the server.jar file to the minecraft directory
* the easiest way to do this is by putting the ***server.jar*** on a USB and copying it to the raspberry pi
* Next drag and drop the ***server.jar*** file into the minecraft directory you created
### Step 6
Next Cd into the minecraft folder and type the following command to start the server
```
java -Xmx1024M -Xms1024M -jar minecraft_server.jar nogui
```
* the server will fail to start untill you accept the eula
### Step 7
Accept the EULA
```
nano eula.txt
```
* Change nano '***eula=false***' to '***eula=true***'
### Step 8 
Run the server start command again
```
java -Xmx1024M -Xms1024M -jar minecraft_server.jar nogui
```
### Step 9
Connect to to server
* open the minecraft lunacher on your server verison and type in the raspberry pi (you can find this by using ***ifconfig*** in the terminal) and enjoy your minecraft server!
#### Notes
This server will ONLY run on your local network friends on other wifi's ***cannont*** connect to it
