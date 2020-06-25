# Cross-Game Chat
Encrypted websocket cross-game chat with an invite-to-server feature. Only works on Synapse X.

## How to test it:
1. Load `demo.lua` in your editor.
2. Change your color/role settings as you'd like.
3. Run it.

To toggle sending, chat "!c" or "!chat".

To invite people to your server, chat "!invite".

To join an invite you received, chat "!join".

## How to setup your own private chat:
> Note: This should work with any platform supporting Node.JS apps, but for simplicity, this example will use an Ubuntu VPS.
#### Server Setup
1. Get an Ubuntu VPS (Virtual Private Server).
2. [Optional] Get a domain name and point it to your VPS (Steps depend on your domain registrar/VPS provider).
3. Connect to your VPS with SSH.
4. Run `sudo apt update && sudo apt upgrade` and enter `Y` if asked.
5. Run `sudo apt install nodejs && sudo apt install npm` and enter `Y` if asked.
6. [Optional] `cd` to a directory where you'd like to install the server app.
7. Run `wget https://raw.githubusercontent.com/xxaim/cross-game-chat/master/server.js`.
8. [Optional] Run `nano server.js` and edit the port.
9. Run `npm install ws http`.
10. Run `nohup node server.js &`, and close your SSH connection.
#### Client Setup
1. Open `demo.lua`.
2. Replace the value for `getgenv().WS_URL` with `"ws://YOUR_URL_OR_VPS_IP_HERE:YOUR_PORT"`. The default port, if you didn't edit it, is `17584`.
3. Generate or enter a strong encryption key, and set it as the value of getgenv().ENCRYPTION_KEY. This is like a password that you share with authenticated users.
4. Save the file and share it to whoever you want in your chat. Other users may edit the other settings as they'd like.

## Credits
	Main Script: Aim
	Colors, Roles, etc: 7n7o
	Chat hook: Riptxde
