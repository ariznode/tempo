# Tempo
Guide How to Run Tempo Node

### Specifications
- CPU	8 cores.
- RAM	16 GB.
- Storage	250 GB SSD.
- Good Internet Connection.

### Install Dependencies


#### Dependencies

```sh
sudo apt update && sudo apt upgrade -y
sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev -y
```

#### Install Tempo

```sh
curl -L https://tempo.xyz/install | bash
source ~/.bashrc
```

#### Check Version

```sh
tempo --version
```

Make sure to see

Tempo Version: 0.7.5
Commit SHA: d1c2d656fb657e3c6f46a8bc3889bdb595d45576
Build Timestamp: 2025-12-15T16:14:58.647380962Z
Build Features: asm_keccak,default,jemalloc,otlp
Build Profile: maxperf

#### Install Rust

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

```sh
echo 'export PATH=$PATH:/usr/local/bin/bin' >> ~/.bashrc
source ~/.bashrc
 ```
 
##### Build and install from source using cargo

```sh
cargo install --git https://github.com/tempoxyz/tempo.git tempo --root /usr/local/bin
tempo --version
```

#### Download Snapshoot

```sh
export RUST_HTTP_TIMEOUT=600
tempo download
```
