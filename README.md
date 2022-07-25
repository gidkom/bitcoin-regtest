## BITCOIN REGTEST

A simple setup for setting up and running a local bitcoin regtest network


### REQUIREMENTS
- Docker & Docker compose installed and running
### SETUP
- Clone repository
- Edit `docker-compose.yml` and `bitcoin-conf/bitcoin.conf` with values for 
  `rpcuser` `rpcpassword` and ports as necessary
- Run `docker-compose up -d` and voilà you have your own bitcoin node running.

### COMMANDS
You can run RPC commands via API by connecting to the rpc port specified
```
curl --user rpcuser --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "uptime", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:18443/

```
Alternatively you can connect to the docker container and run the RPC commands
```
$ bitcoin-cli uptime
```