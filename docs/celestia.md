## Lum Network

create validator

```bash
celestia-appd tx staking create-validator \
    --amount=1000000000celes \
    --pubkey=$(celestia-appd tendermint show-validator) \
    --moniker="polkachu.com" \
    --chain-id=devnet-2 \
    --commission-rate=0.1 \
    --commission-max-rate=0.2 \
    --commission-max-change-rate=0.01 \
    --min-self-delegation=1000000000 \
    --website "https://polkachu.com" \
    --identity "0A6AF02D1557E5B4" \
    --details "Polkachu is the trusted staking service provider for blockchain projects. 100% refund for downtime slash. Contact us at hello@polkachu.com" \
    --from=chani \
    --keyring-backend=test
```

Delegate

```bash
celestia-appd tx staking delegate celesvaloper1pcmran05kpxjw8g9fja2aqk2q8e49hgzmgznxd 800000celes \
    --chain-id=devnet-2 \
    --from=chani \
    --keyring-backend=test
```

Unjail

```bash
celestia-appd tx slashing unjail --from celes1pcmran05kpxjw8g9fja2aqk2q8e49hgz79d339 \
    --chain-id=devnet-2 \
    --from=chani \
    --keyring-backend=test

```
