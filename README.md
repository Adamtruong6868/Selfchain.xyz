# Selfchain.xyz

### 1.Update system
```sudo apt update```

```sudo apt-get install git curl build-essential make jq gcc snapd chrony lz4 tmux unzip bc -y```
### 2.Install Go
```rm -rf $HOME/go
sudo rm -rf /usr/local/go
cd $HOME
curl https://dl.google.com/go/go1.20.5.linux-amd64.tar.gz | sudo tar -C/usr/local -zxvf -
cat <<'EOF' >>$HOME/.profile
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
EOF
source $HOME/.profile
go version```
```
### 3.Install node

```cd $HOME```

```mkdir -p /root/go/bin/```

```wget https://ss-t.self.nodestake.top/selfchaind```

```chmod +x selfchaind```

```mv selfchaind /root/go/bin/```

```selfchaind version```
### 4. Initialize Node
#### Replace NodeName with your own moniker.

```selfchaind init NodeName --chain-id=self-dev-1```

Example Nodename = VNBnode, then: selfchaind init VNBnode --chain-id=self-dev-1
