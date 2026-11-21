# monerod Commands and Flags Reference: configuration examples

Source: https://monero.love/guides/monerod-commands/

Start with `monerod-local.conf`, create `/srv/monero` with write access for your dedicated daemon account, and run `monerod --non-interactive --config-file /absolute/path/monerod-local.conf`. Administrative RPC stays on loopback and ZMQ is disabled.

The public-RPC file is an optional fragment. Merge its keys into a copy of the base file, replacing existing keys instead of concatenating duplicate settings. It exposes restricted daemon RPC on IPv4 port 18089. Keep the administrative listener on loopback and apply your intended firewall policy. Restricted daemon RPC is not wallet RPC and is still an externally accessible service.

The TLS fragment requires your own certificate and private key at the configured paths. Keep keys outside this repository, readable only by the service account. Review remote-wallet compatibility and certificate validation before enabling it.

The source article inventories v0.18.5.4. Confirm the options with your selected binary's `--help`. The examples are separate choices, not one combined configuration.

References: [configuration syntax](https://docs.getmonero.org/interacting/monero-config-file/), [daemon options](https://docs.getmonero.org/interacting/monerod-reference/).

## Files

- `monerod-local.conf`
- `monerod-public-rpc.fragment.conf`
- `monerod-tls.fragment.conf`

`ARTICLE-EXAMPLES.md` preserves the published code blocks for context. It is a reference, not a script to execute in one pass. `SOURCE.json` identifies the fetched page and packaged file hashes. No services were installed or restarted when preparing this repository.
