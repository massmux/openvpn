# openvpn

this project is simply a setup for dockerized openvpn from  kylemanna. The aim is to best simplify running the vpn

## Server setup

The setup is very simple:

Be very sure that your fully qualified hostname is setup. Something like vpn.yourdomain.com . It is important, otherwise install will fail. The run the following command

```
./init
```

then follow procedure and answer questions. You will be asked to set a passphrase. This procedure will initialize server and run it. There will be no need of redoing it again if correctly completed

## Client setup

The script will ask you for the passphrase for server cert, and you will be also required to setup a passphrase for the client. This is mandatory. The script will create a .ovpn file that can be used across your client for connecting to the vpn server.

```
./client
```

You shall run this script anytime you have a new client to add to this vpn.

## Running the server

From the folder. If you run the init script, there is no need to manually run the server itself. The init script will do all necessary.

```
docker-compose up -d
```
