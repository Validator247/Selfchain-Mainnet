# Selfchain-Mainnet

#Download gennesis & Addrbook

    wget https://raw.githubusercontent.com/Validator247/Selfchain-Mainnet/main/addrbook.json -O addrbook.json
    wget https://raw.githubusercontent.com/Validator247/Selfchain-Mainnet/main/genesis.json -O genesis.json

#Public RPC Endpoint

RPC https://selfchain-rpc.validator247.com

API https://selfchain-api.validator247.com

#Explorer

https://explorer.validator247.com/selfchain-mainnet/staking


#Snapshot & State sync

Snapshot

    sudo systemctl stop selfchaind
    cp $HOME/.selfchain/data/priv_validator_state.json $HOME/.selfchain/priv_validator_state.json.backup
    selfchaind tendermint unsafe-reset-all --home ~/.selfchain/ --keep-addr-book

    curl https://snapshot2.syanodes.my.id/selfchain/snapshot2-selfchain.tar.lz4 | lz4 -dc - | tar -xf - -C $HOME/.selfchain

    mv $HOME/.selfchain/priv_validator_state.json.backup $HOME/.selfchain/data/priv_validator_state.json

    sudo systemctl restart selfchaind && sudo journalctl -fu selfchaind -o cat

State Sync

    sudo systemctl stop selfchaind

    cp $HOME/.selfchain/data/priv_validator_state.json $HOME/.selfchain/priv_validator_state.json.backup
    selfchaind tendermint unsafe-reset-all --home $HOME/.selfchain

    peers="b307b56b94bd3a02fcad5b6904464a391e13cf48@128.199.33.181:26656,71b8d630e7c3e31f2743fda68e6d3ac64f41cece@209.97.174.97:26656,6ae10267d8581414b37553655be22297b2f92087@174.138.25.159:26656"
    PEERS="6ae10267d8581414b37553655be22297b2f92087@174.138.25.159:26656,b307b56b94bd3a02fcad5b6904464a391e13cf48@128.199.33.181:26656,34c3a8a2955b4d6e5deef15c6b091250f5878afe@18.117.74.150:26656,4c8b8296e767cf3d67355dba98781ee0348e87ea@144.76.30.94:30056,c139f537755d5614a3ceaeb0f01b03be94e7ecb5@162.19.171.121:26656,6a3a0db2763d8222d00af55cbbe35824a39c8292@176.9.183.45:34656,e22a53afe2caa3aafae89edec68531e5dffa071f@188.40.72.97:26656,7a9038d1efd34c7f3baea17d8822262a981568b1@217.182.136.79:30156,f238d6a52578975198ceac2b0c2b004d49d5613f@88.198.5.77:31656,8401cbf633c496e464a2d016b333f61ff34e9ee9@167.71.233.135:26656,aab5f0267427d9dbd840fd04e634a02837d44365@51.77.20.28:25565,c743758973f5543578949228ff623918a4b43c54@165.232.177.11:26656,e5b970c7b4e9b0281fc2fc58166c9e9af476c9a3@46.4.23.120:58656,0a67ac1518c816e1927554dfc17c47f4ee457bcb@168.119.75.88:36656,2f547f93392d7351c74a0d8cae1d44f172cf32e5@64.227.156.23:26656,55d3e1761d6752eeb72b8b86decbca0d56f6a885@159.89.173.150:26656,02982b993b659c377238db477ae3698065ebc941@13.250.113.56:26656,9512a59cf93b987aff830148421a514cacb8a1b8@170.64.141.15:26656,024aa95bbdcef24d8d55c04f9c4de2fec2bc3bf6@34.159.240.168:26656,5fec0f158870a9e82e8a48fed83a78d567fb639a@167.235.12.38:22156,7efdc46e50e03e1f1208c8f276047b7fea345cc8@34.159.40.118:26656,62771c2083623cb6db6eda99f404036759c5f4b3@65.109.99.157:16609,a96b7c56cb64c16917a629c9ae0f3b3c0aea584c@35.234.89.188:26656,b844793daeffaedfcdbd5b08688cd10e1859d678@37.120.245.116:26656,790544e857cfe673cab570668131aa7ae2be7e5d@178.63.100.102:26656,a0c70d4dcce7b979faaa375a21300efd03001c99@34.48.99.116:26656,c87c1b17045b27fd14b13d7dbb3469a2248cb1f7@95.217.204.58:24356,637077d431f618181597706810a65c826524fd74@5.9.151.56:24356,d93bbc2d467800a10581d38261041d7dc0bcc4cd@158.220.90.61:26656,e097dc629cbe874b139841dedb06775cc75435ee@65.108.237.188:20656,7bad33a03bec7c0bd174a386045d5ff583b39570@95.216.7.84:36656,c1499d43cf198e2bc5490b9e2018ef22cd657d89@65.108.81.240:26656,d0478546164151adfc225ebc52509736bb05375a@173.234.17.129:26656,ee1265e95bcbfbeff7d096befe17e24c88549c65@65.108.9.83:11356,f282af2ba286abb9d4aab611a8f39176c26d6928@213.239.207.175:61656,e9376f40ac2b672e9f2f66ad212f59801d53afe8@178.162.165.193:26656,9d7dbaa0cb7f28ab8926c738860c18bd6d00aaaf@168.119.75.89:26656,c597aa118302d417e039e5a81d722422e73c85e1@135.125.67.227:26656,a950d48fce4a648aacf7327198e6ea3e545f3112@168.119.166.138:26656,e3edeec5261ec00ba4a87cdd419f601ee5e5e063@109.199.118.239:11356,473303f1a0dff43121cff9b7a12b5b39a42bc46c@37.27.31.253:26656,75f56904bf31a89b4b085eeaaf0fcea04311abed@113.176.142.7:10056,923758c6f7adaec3c9a668dc74ba28fda7066b1c@65.109.120.211:24656,c91ca713d48dac1ac940da53db1ff99cedb3f171@154.38.172.102:10256"
    SNAP_RPC="https://selfchain-rpc.validator247.com:443"

    sed -i.bak -e "s/^persistent_peers *=.*/persistent_peers = \"$peers\"/" $HOME/.selfchain/config/config.toml 

    LATEST_HEIGHT=$(curl -s $SNAP_RPC/block | jq -r .result.block.header.height);
    BLOCK_HEIGHT=$((LATEST_HEIGHT - 1000));
    TRUST_HASH=$(curl -s "$SNAP_RPC/block?height=$BLOCK_HEIGHT" | jq -r .result.block_id.hash) 

    echo $LATEST_HEIGHT $BLOCK_HEIGHT $TRUST_HASH && sleep 2

    sed -i.bak -E "s|^(enable[[:space:]]+=[[:space:]]+).*$|\1true| ;
    s|^(rpc_servers[[:space:]]+=[[:space:]]+).*$|\1\"$SNAP_RPC,$SNAP_RPC\"| ;
    s|^(trust_height[[:space:]]+=[[:space:]]+).*$|\1$BLOCK_HEIGHT| ;
    s|^(trust_hash[[:space:]]+=[[:space:]]+).*$|\1\"$TRUST_HASH\"| ;
    s|^(seeds[[:space:]]+=[[:space:]]+).*$|\1\"\"|" $HOME/.selfchain/config/config.toml

    mv $HOME/.selfchain/priv_validator_state.json.backup $HOME/.selfchain/data/priv_validator_state.json

    sudo systemctl restart selfchaind && sudo journalctl -fu selfchaind -o cat

#WALLET MANAGEMENT

    #Add new wallet
    selfchaind keys add wallet

    #Recover Wallet
    selfchaind keys add wallet --recover

    #List Wallet
    selfchaind keys list

    #Delete Wallet
    selfchaind keys delete wallet

    #Check Wallet Balance
    selfchaind q bank balances $(selfchaind keys show wallet -a)

#VALIDATOR MANAGEMENT

    #Create Validator
    selfchaind tx staking create-validator \
    --amount=10000000uslf \
    --pubkey=$(selfchaind tendermint show-validator) \
    --moniker=$MONIKER \
    --identity="YOUR_KEYBASE_ID" \
    --details="YOUR_DETAILS" \
    --website="YOUR_WEBSITE_URL" \
    --chain-id=$SELFCHAIN_CHAIN_ID \
    --commission-rate=0.10 \
    --commission-max-rate=0.20 \
    --commission-max-change-rate=0.01 \
    --min-self-delegation=1000 \
    --from=wallet \
    --gas-adjustment=1.5 \
    --gas="auto" \
    --gas-prices=10uslf\ 
    -y

    #Edit Validator
    selfchaind tx staking edit-validator \
    --new-moniker="YOUR MONIKER" \
    --identity="IDENTITY KEYBASE" \
    --details="DETAILS VALIDATOR" \
    --website="LINK WEBSITE" \
    --chain-id=$SELFCHAIN_CHAIN_ID \
    --from=wallet \
    --gas-adjustment=1.5 \
    --gas="auto" \
    --gas-prices=10uslf\ 
    -y

    #Unjail Validator
    selfchaind tx slashing unjail --from wallet --chain-id $SELFCHAIN_CHAIN_ID --gas-adjustment 1.5 --gas auto --gas-prices 10uslf -y

    #Check Jailed Reason
    selfchaind query slashing signing-info $(selfchaind tendermint show-validator)
