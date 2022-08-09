#
Commands to replace addrbook file in Sifchain 
# 

```sh
systemctl stop cosmovisord
rm $HOME/.sifnoded/config/addrbook.json
wget -O $HOME/.sifnoded/config/addrbook.json "https://raw.githubusercontent.com/Firstcomes/Mainnet/main/Sifchain/addrbook.json"
systemctl restart cosmovisord && journalctl -u cosmovisord -f
```
