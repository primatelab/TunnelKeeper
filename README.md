# tunnelkeeper
### TunnelKeeper keeps SSH tunnels open

Install it as a service with `tunnelkeeper install`.

Edit the config file `/opt/tunnelkeeper/etc/tunnelkeeper.conf`. If you make changes to tunnelkeeper.conf, run `systemctl restart tunnelkeeper`.

There are 3 sections:
#### settings
- `debug [0..3]`: Debug logging levels 0 (no logging) to 3 (too much logging)
#### ssh
- It's an ssh config file, so see `man ssh_config` for information. TunnelKeeper will connect to each host listed, and make sure every connection in `tunnelkeeper.conf` stays open in the background.
#### passwords
- `host password`: Passwords of the hosts in the ssh section. They are stored in plaintext, so don't use it if you can avoid it.
