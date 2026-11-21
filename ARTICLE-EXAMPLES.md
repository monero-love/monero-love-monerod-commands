# Published examples

Source: https://monero.love/guides/monerod-commands/

Read the article for the ordering, prerequisites and version limits of these separate examples.

## Block 1

```text
./monerod --version
./monerod --help
```

## Block 2

```text
./monerod --prune-blockchain --out-peers 16
```

## Block 3

```text
status
sync_info
print_cn
```

## Block 4

```text
./monerod status
./monerod --rpc-bind-ip 127.0.0.1 --rpc-bind-port 18081 sync_info
```

## Block 5

```text
# Example: a pruned node with local administrative RPC.
data-dir=/srv/monero
prune-blockchain=1
rpc-bind-ip=127.0.0.1
rpc-bind-port=18081
no-zmq=1
out-peers=16
log-level=0
```

## Block 6

```text
./monerod --non-interactive --config-file /etc/monerod.conf
```

## Block 7

```text
fast:async:250000000bytes
```

## Block 8

```text
./monerod --prune-blockchain --p2p-use-ipv6
```

## Block 9

```text
network-type,proxy[,max_connections][,disable_noise]
```

## Block 10

```text
./monerod --tx-proxy tor,127.0.0.1:9050
```

## Block 11

```text
--anonymous-inbound YOUR_SERVICE.onion:18083,127.0.0.1:18083
```

## Block 12

```text
rpc-bind-ip=127.0.0.1
rpc-bind-port=18081
rpc-restricted-bind-ip=0.0.0.0
rpc-restricted-bind-port=18089
public-node=1
```

## Block 13

```text
rpc-ssl=enabled
rpc-ssl-private-key=/etc/monero/tls/node.key
rpc-ssl-certificate=/etc/monero/tls/node.crt
```

## Block 14

```text
./monerod --zmq-pub tcp://127.0.0.1:18083
```

## Block 15

```text
./monerod --start-mining <PRIMARY_ADDRESS> --mining-threads 2
```

## Block 16

```text
./monerod --block-notify '/usr/local/bin/monero-block-hook %s'
```

## Block 17

```text
start_mining <PRIMARY_ADDRESS> 2 true false
```

## Block 18

```text
status
sync_info
print_cn
print_net_stats
```

## Block 19

```text
print_pool_stats
print_tx <TXID> +json
```

## Block 20

```text
set_log 1
```

## Block 21

```text
set_log 0
```

## Block 22

```text
./monerod --rpc-bind-ip 127.0.0.1 --rpc-bind-port 18081 stop_daemon
```
