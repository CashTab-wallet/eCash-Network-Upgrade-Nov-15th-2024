# [CashTab Wallet](https://ecashtab.org/)


# eCash Network Upgrade Nov 15th 2024
In order to activate reliably at a predictable time, the network upgrade uses the “Median Time Past” mechanism. The upgrade activates when the median of the last 11 blocks reaches timestamp 1731672000 (12:00:00 UTC on November 15th, 2024)

The Network Upgrade will activate using the "Median Time Past" mechanism to ensure a predictable activation time. It is set to trigger when the median timestamp of the last 11 blocks reaches 1731672000 (12:00:00 UTC on November 15, 2024). However, the upgrade won't activate precisely at this time. In practice, it typically happens about one hour later, once 6 blocks with timestamps greater than the activation time have been mined.

The Network Upgrade will introduce the Heartbeat feature, also known as Real Time Targeting. This new block policy aims to prevent blocks from being mined too quickly, ensuring a more consistent average block time of 10 minutes. It reduces the risk of significant difficulty adjustments that could cause irregular block intervals. Miners will need to update their setups following the instructions provided on the Mining page.

# Do I Need to Upgrade My Wallet?
No, you do not need to upgrade your wallet. The network upgrade only impacts full nodes. Other eCash software, including wallets like [Cashtab](https://ecashtab.org/), are not affected by the upgrade and will continue to work as usual.


# Node Upgrade Guide

This guide outlines the steps to upgrade your node from version 0.29.13 to version 0.30.4 on Linux.

## Upgrade Process

Upgrading your node is straightforward. Follow the steps below:

### Step 1: Shut Down the Current Node

To stop the currently running node, use the following command:

```bash
./bitcoin-abc-0.29.13/bin/bitcoin-cli stop
```

### Step 2: Download the New Version
Download the new version archive from the official website:

wget https://download.bitcoinabc.org/0.30.4/linux/bitcoin-abc-0.30.4-x86_64-linux-gnu.tar.gz

### Step 3: Extract the Archive
Extract the downloaded archive:

tar xzf bitcoin-abc-0.30.4-x86_64-linux-gnu.tar.gz


### Restart the node with the new version:
./bitcoin-abc-0.30.4/bin/bitcoind -daemon

### Clean up old version and archives (optional):
rm -rf bitcoin-abc-0.29.13

rm -f bitcoin-abc-0.29.13-x86_64-linux-gnu.tar.gz

rm -f bitcoin-abc-0.30.4-x86_64-linux-gnu.tar.gz



