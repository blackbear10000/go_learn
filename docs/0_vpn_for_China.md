# 1. Set a VPN 
I recommend [V2Ray](https://github.com/wulabing/V2Ray_ws-tls_bash_onekey) to set your VPN.  

# 2.Install Privoxy
At the same time, you should install Privoxy on your Mac. Make your ternimal to use VPN by http agency, rather than sock5.
```
brew install privoxy
```
Add something to ` /usr/local/etc/privoxy/config`
```
forward-socks5 / 127.0.0.1:1080 . # SOCKS5 agency address
listen-address 127.0.0.1:8080 # HTTP agency address
forward 10.*.*.*/ . # don't use agency
forward .abc.com/ . # don't use agency
```
Then (re)start your Privoxy.
```
sudo privoxy /usr/local/etc/privoxy/config
```
Finally, set 2 environment variables.  
```
export http_proxy="127.0.0.1:8080"
export https_proxy="127.0.0.1:8080"
```