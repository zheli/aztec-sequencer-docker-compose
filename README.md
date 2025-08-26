# aztec-sequencer-docker-compose
Docker Compose file for Aztec Sequencer in my local environment

## Steps
1. Clone the repository
2. Go into the folder and run `docker compose up -d`
3. Register your validator at https://testnet.aztec.network/add-validator
4. Check the queue at https://dashtec.xyz/queue

## Runbooks
### Check node status
```
curl -s -X POST -H 'Content-Type: application/json' \
-d '{"jsonrpc":"2.0","method":"node_getL2Tips","params":[],"id":67}' \
http://localhost:8080 | jq -r ".result.proven.number"

```