# Namada-Shielded-Expeditions
Proofs for Namada Shielded Expedition

**IBC Task shielded-expedition.88f17d1d14**

**Nebb player:**

https://extended-nebb.kintsugi.tech/player/tpknam1qrmde98m5n2ra4232glvl3xgc2z52y9u9x0wp0y4w65rmx2sv09qzth4h39 

**Osmosis IBC wallet:**

https://www.mintscan.io/osmosis-testnet/address/osmo1q74pk6myealr82u7slvpr9tfwjph9pdq8dfu2g

**Namada IBC wallet:**
tnam1qq84w5fps984xrne6a0a6hdfgnkurhcpvur0jkxz


**Create channel Namada <> Osmosis**

```
hermes --config ~/.hermes/config.toml \
  create channel \
  --a-chain shielded-expedition.88f17d1d14 \
  --b-chain osmo-test-5 \
  --a-port transfer \
  --b-port transfer \
  --new-client-connection --yes
2024-03-11T05:29:24.647279Z  INFO ThreadId(01) running Hermes v1.7.4+38f41c6
2024-03-11T05:29:24.905899Z  INFO ThreadId(01) Creating new clients, new connection, and a new channel with order ORDER_UNORDERED
2024-03-11T05:29:40.325979Z  INFO ThreadId(01) foreign_client.create{client=osmo-test-5->shielded-expedition.88f17d1d14:07-tendermint-0}: :lollipop: client was created successfully id=07-tendermint-2434
2024-03-11T05:29:43.022206Z  INFO ThreadId(01) foreign_client.create{client=shielded-expedition.88f17d1d14->osmo-test-5:07-tendermint-0}: :lollipop: client was created successfully id=07-tendermint-2753
2024-03-11T05:30:02.890838Z  INFO ThreadId(01) :clinking_glasses: shielded-expedition.88f17d1d14 => OpenInitConnection(OpenInit { Attributes { connection_id: connection-1159, client_id: 07-tendermint-2434, counterparty_connection_id: None, counterparty_client_id: 07-tendermint-2753 } }) at height 0-109787
2024-03-11T05:30:39.191023Z  INFO ThreadId(01) :clinking_glasses: osmo-test-5 => OpenTryConnection(OpenTry { Attributes { connection_id: connection-2505, client_id: 07-tendermint-2753, counterparty_connection_id: connection-1159, counterparty_client_id: 07-tendermint-2434 } }) at height 5-5935476
2024-03-11T05:30:43.457650Z  WARN ThreadId(01) client consensus proof height too high, waiting for destination chain to advance beyond 0-109790
2024-03-11T05:30:44.024579Z  WARN ThreadId(01) client consensus proof height too high, waiting for destination chain to advance beyond 0-109790
2024-03-11T05:30:44.591815Z  WARN ThreadId(01) client consensus proof height too high, waiting for destination chain to advance beyond 0-109790
2024-03-11T05:30:45.171589Z  WARN ThreadId(01) client consensus proof height too high, waiting for destination chain to advance beyond 0-109790
2024-03-11T05:30:45.739443Z  WARN ThreadId(01) client consensus proof height too high, waiting for destination chain to advance beyond 0-109790
2024-03-11T05:31:08.808235Z ERROR ThreadId(01) failed ConnOpenAck ConnectionSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159 }: failed during a transaction submission step to chain 'shielded-expedition.88f17d1d14': failed tx: no confirmation
2024-03-11T05:31:27.502831Z  INFO ThreadId(01) :clinking_glasses: osmo-test-5 => OpenConfirmConnection(OpenConfirm { Attributes { connection_id: connection-2505, client_id: 07-tendermint-2753, counterparty_connection_id: connection-1159, counterparty_client_id: 07-tendermint-2434 } }) at height 5-5935488
2024-03-11T05:31:30.538763Z  INFO ThreadId(01) connection handshake already finished for Connection { delay_period: 0ns, a_side: ConnectionSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159 }, b_side: ConnectionSide { chain: BaseChainHandle { chain_id: osmo-test-5 }, client_id: 07-tendermint-2753, connection_id: connection-2505 } }
2024-03-11T05:31:51.385036Z ERROR ThreadId(01) failed ChanOpenInit ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159, port_id: transfer, channel_id: None, version: None }: failed during a transaction submission step to chain 'shielded-expedition.88f17d1d14': failed tx: no confirmation
2024-03-11T05:32:15.317721Z ERROR ThreadId(01) failed ChanOpenInit ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159, port_id: transfer, channel_id: None, version: None }: failed during a transaction submission step to chain 'shielded-expedition.88f17d1d14': failed tx: no confirmation
2024-03-11T05:32:46.792359Z ERROR ThreadId(01) failed ChanOpenInit ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159, port_id: transfer, channel_id: None, version: None }: failed during a transaction submission step to chain 'shielded-expedition.88f17d1d14': failed tx: no confirmation
2024-03-11T05:33:08.841559Z  INFO ThreadId(01) :confetti_ball:  shielded-expedition.88f17d1d14 => OpenInitChannel(OpenInit { port_id: transfer, channel_id: channel-707, connection_id: None, counterparty_port_id: transfer, counterparty_channel_id: None }) at height 0-109804
2024-03-11T05:33:23.954251Z  INFO ThreadId(01) :confetti_ball:  osmo-test-5 => OpenTryChannel(OpenTry { port_id: transfer, channel_id: channel-6188, connection_id: connection-2505, counterparty_port_id: transfer, counterparty_channel_id: channel-707 }) at height 5-5935517
2024-03-11T05:33:49.349166Z ERROR ThreadId(01) failed ChanOpenAck ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159, port_id: transfer, channel_id: channel-707, version: None }: failed during a transaction submission step to chain 'shielded-expedition.88f17d1d14': failed tx: no confirmation
2024-03-11T05:33:49.349206Z ERROR ThreadId(01) failed ChanOpenAck ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159, port_id: transfer, channel_id: channel-707, version: None }: failed during a transaction submission step to chain 'shielded-expedition.88f17d1d14': failed tx: no confirmation
2024-03-11T05:34:08.133495Z  INFO ThreadId(01) :confetti_ball:  osmo-test-5 => OpenConfirmChannel(OpenConfirm { port_id: transfer, channel_id: channel-6188, connection_id: connection-2505, counterparty_port_id: transfer, counterparty_channel_id: channel-707 }) at height 5-5935528
2024-03-11T05:34:11.250365Z  INFO ThreadId(01) channel handshake already finished for Channel { ordering: ORDER_UNORDERED, a_side: ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-2434, connection_id: connection-1159, port_id: transfer, channel_id: channel-707, version: None }, b_side: ChannelSide { chain: BaseChainHandle { chain_id: osmo-test-5 }, client_id: 07-tendermint-2753, connection_id: connection-2505, port_id: transfer, channel_id: channel-6188, version: None }, connection_delay: 0ns }
SUCCESS Channel {
    ordering: Unordered,
    a_side: ChannelSide {
        chain: BaseChainHandle {
            chain_id: ChainId {
                id: "shielded-expedition.88f17d1d14",
                version: 0,
            },
            runtime_sender: Sender { .. },
        },
        client_id: ClientId(
            "07-tendermint-2434",
        ),
        connection_id: ConnectionId(
            "connection-1159",
        ),
        port_id: PortId(
            "transfer",
        ),
        channel_id: Some(
            ChannelId(
                "channel-707",
            ),
        ),
        version: None,
    },
    b_side: ChannelSide {
        chain: BaseChainHandle {
            chain_id: ChainId {
                id: "osmo-test-5",
                version: 5,
            },
            runtime_sender: Sender { .. },
        },
        client_id: ClientId(
            "07-tendermint-2753",
        ),
        connection_id: ConnectionId(
            "connection-2505",
        ),
        port_id: PortId(
            "transfer",
        ),
        channel_id: Some(
            ChannelId(
                "channel-6188",
            ),
        ),
        version: None,
    },
    connection_delay: 0ns,
}
```

**Running relayer transaction from namada -> Osmo (with memo)**

```
namadac --base-dir $BASE_DIR \                                      
    ibc-transfer \
    --amount 1 \
    --source relayer \
    --receiver osmo1q74pk6myealr82u7slvpr9tfwjph9pdq8dfu2g \
    --token naan \
    --channel-id channel-707 \
    --node https://rpc-namada-testnet.whispernode.com:443 \
    --memo tpknam1qrmde98m5n2ra4232glvl3xgc2z52y9u9x0wp0y4w65rmx2sv09qzth4h39
MASP parameters not present, downloading...
MASP parameter download complete, resuming execution...
Enter your decryption password: 
Transaction added to mempool.
Wrapper transaction hash: D090D0DE2CB58B36186CB930E1249EFF48F0616D2AB502FB8EDBCB6A27C83938
Inner transaction hash: C8822850CA96226B072968DB6CFAEA940EE4EF2E95EFA305A9A2A160D6067895
Wrapper transaction accepted at height 109877. Used 26 gas.
Waiting for inner transaction result...
Transaction was successfully applied at height 109878. Used 6193 gas.
```

**Running relayer transaction from Osmosis -> Namada**

```osmosisd tx ibc-transfer transfer \      
  transfer \
  channel-6188 \
  tnam1qq84w5fps984xrne6a0a6hdfgnkurhcpvur0jkxz \
  1000000uosmo \
  --from relayer-osmo-test-5 \
  --gas auto \
  --gas-prices 0.04uosmo \
  --gas-adjustment 1.2 \
  --node "http://127.0.0.1:12557" \
  --home "$HOME/.osmosisd" \
  --chain-id osmo-test-5 \
  --yes \
  --keyring-backend file
Enter keyring passphrase (attempt 1/3):
gas estimate: 131157
code: 0
codespace: ""
data: ""
events: []
gas_used: "0"
gas_wanted: "0"
height: "0"
info: ""
logs: []
raw_log: '[]'
timestamp: ""
tx: null
txhash: 0E7BFA28C86B5AC3A73671DAA401DCE72B0C1C17720412B9681F9EBF267158CF
```

**Osmosis Wallet - proof of IBC transfer (1 NAAN token in balances)**

```
osmosisd q bank balances osmo1q74pk6myealr82u7slvpr9tfwjph9pdq8dfu2g
balances:
- amount: "1"
  denom: ibc/D9FCEC061CC77A532B1FB7925E686DC61D8BB06B2E057E9D16A663ADF6877DD2
- amount: "47781992"
  denom: uosmo
pagination:
  next_key: null
  total: "0"
```

**Namada wallet - proof of IBC transfer (1 $OSMO token on channel-707)**

```
 namadac balance --owner relayer --node https://rpc-namada-testnet.whispernode.com:443
naan: 23.5
transfer/channel-707/uosmo: 1000000
```

**Osmosis: explorer proofs**
https://testnet.ping.pub/osmosis/tx/0E7BFA28C86B5AC3A73671DAA401DCE72B0C1C17720412B9681F9EBF267158CF
https://testnet.ping.pub/osmosis/tx/8A44788D6A956C82DCC4B46CD1902EA4C6B2CB74639F713ADA4389CFF519FC1B
https://testnet.ping.pub/osmosis/tx/2F42299E6080B5C3653E2DED85B05DB3D9F5308452019295509FDA515CFD0296

