# tunnelkeeper
### TunnelKeeper keeps SSH tunnels open

Install it as a service with `tunnelkeeper install`.

Create a config file `/opt/tunnelkeeper/etc/tunnels.conf`. It's an ssh config file, so see `man ssh_config` for information. TunnelKeeper will connect to each host listed, and make sure every connection in `tunnels.conf` stays open in the background.

If you make changes to tunnels.conf, run `systemctl restart tunnelkeeper`.
