# setup-minecraft-server
A quick guide to set up a minecraft server on linux

1. Make sure you have java installed. If not install it. If you are on a debian based system you can use `sudo apt install openjdk-11-jdk`
2. Download the minecraft server from the official site. https://www.minecraft.net/en-us/download/server . Then rename the file to server.jar
3. Run the `run.sh` file. Don't worry if you get an erorr:
4. Open eula.txt with your favorite text editor and change it from `eula=false` to `eula=true`.
5. Run the `run.sh` file again and everything should be working. Enjoy
6. Your server should be running on localhost:25565 or 127.0.0.1:25565
 
Important: 
  - if you are using a non premiun version of minecraft follow the guide bellow.
  - if you wan't to play with users outside your internet follow the guide bellow


# Minecraft no-premiun
If you want to be able to play on your server with non premiun accounts open the `server.properties` file and change online-mode from `true` to `false`

# Play with people outside your internet
1. Open your pc's ports. Use the following commands.
   - `sudo ufw enable` to enable your firewall
   - `sudo ufw allow in 25565/tcp`
   - `sudo ufw allow in 25565/udp`
   - `sudo ufw allow in 19132:19133/udp`
2. Open your routers same ports: 25565/tcp, 25565/udp and 19132:19133/udp. Each router has it's way of doing it so unfortunatelly I can't help you with this step. Usually the router configs are in http://192.168.0.1 . Once there usually have to enter your username and password and there search for something called like: ports, redirect ports, redirect...

3. Once this is done you can play with people outside your internet. You will have to access the server with 127.0.0.1:25565 and people outside your internet will have to access it through your ip. To find out what your ip is go the https://nordvpn.com/what-is-my-ip/ and you will see your ip. Keep in mind that the ip changes every x time so people outside your internet will have to switch IP every certain time.

Tip: if you want to get fancy you could set up a dns and link it with your pc ip so people outside your internet can access it through a dns instead of a ip. This way you don't have to worry about having the current IP since the dns name wont change.

