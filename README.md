# tunnelkeeper
### TunnelKeeper keeps SSH tunnels open

Install it as a service with `tunnelkeeper install`.

Edit the config file with `tunnelkeeper config` (or edit `etc/tunnelkeeper.conf` manually).

If you make changes to tunnelkeeper.conf, run `tunnelkeeper restart` or `systemctl restart tunnelkeeper`.

- It's an ssh config file, so see `man ssh_config` for information. TunnelKeeper will connect to each host listed, and make sure every connection in `tunnelkeeper.conf` stays open in the background.
- There are 3 options that aren't available in normal ssh config files:
  - `Watch N` : Enables an echo test on the host at intervals of **N** seconds.
  - `Password` : Uses screen to log in with a password. This is **insecure**, since the password is in plaintext, so use passwordless auth if possible.
  - `Debug [0..3]`: Debug logging levels 0 (no logging) to 3 (too much logging).
