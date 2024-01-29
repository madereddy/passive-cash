# Passive Cash
Docker compose running proxy and bandwidth sharing applications : Honeygain, EarnApp, IPRoyal Pawns, PacketStream, EarnFM, and Repocket. 

- Have a computer ideally with Linux and Docker installed and ready to use.
- Create an account for the apps below which uses my referral code. 
    | App Name & Link | Residential/Home/Mobile IP or equivalent Proxy's IP | VPS/Datacenter/Hosting/Cloud IP or equivalent Proxy's IP | Max devices per Account | Max Devices per IP | 
    |  :--- |  :---: |  :---: | :---: | :---: |
    | Go to [Earnapp](https://earnapp.com/i/s7bb5Y5Z)  | :white_check_mark:	  | :x: | 15|1|
    | Go to [Honeygain](https://r.honeygain.me/SSINGA7A5C) | :white_check_mark:	  | :x: |10|1|
    | Go to [IPRoyal Pawns](https://pawns.app/?r=2239107)  | :white_check_mark:	  | :x: |Unlimited|1|
    | Go to [Packetstream](https://packetstream.io/?psr=5gwa)  | :white_check_mark:	  | :x: |Unlimited|1|
    | Go to [Repocket](https://link.repocket.co/fCjC)  | :white_check_mark:	  | :white_check_mark: |Unlimited|2|
    | Go to [EarnFm](https://earn.fm/ref/JEETW9E3)  | :white_check_mark:	  | :x: |Unlimited|1|
- Update .env file with the account details
- For EarnApp you will need to create and register a UUID. Follow the instructions below.

    - The UUID is 32 characters long with lowercase alphabet and numbers. You can either create this by yourself or via this command:

    - ```echo -n sdk-node- && head -c 1024 /dev/urandom | md5sum | tr -d ' -'```

    - Example output: ```sdk-node-0123456789abcdeffedcba9876543210```
- Update .env file with the Earnapp UUID that was just generated.


Start stack (first run only):

- Start stack: sudo docker compose up -d (Make sure to be in the correct directory)

- After stack has started you will need to register the UUID with Earnapp using the following URL.

- https://earnapp.com/r/UUID

- Example url: ```https://earnapp.com/r/sdk-node-0123456789abcdeffedcba9876543210``

After first run you can use 

Start/stop procedure:

- Start stack: sudo docker compose up -d (Make sure to be in the correct directory)
- Stop stack: sudo docker-compose down (Make sure to be in the correct directory)

Compatibility:

This Docker Stack should work on anything that may have docker installed. In particular, it has been tested on: 
| | Windows 11 x86_64\amd64 | Linux Ubuntu x86_64\amd64 | Raspbian OS arm64 | Synology NAS VM (Ubuntu 22) | Synology NAS Container Manager | 
|  :---: |  :---: |  :---: |  :---: | :---: | :---: |
| Tested | :green_circle: | :green_circle: | :green_circle: | :green_circle: | :green_circle:|
| on device | Desktop/Laptop PC | Desktop/Laptop PC | Raspberry Pi3b+/Pi4 | DS1522+ | DS1522+ |