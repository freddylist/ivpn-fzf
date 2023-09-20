# IVPN FZF interface

This is an alternative interface to IVPN using their wireguard configuration files.

## Disclaimer

I am not responsible for any bad things that might happen when you use this.
Use these scripts at your own risk!!!

## Requirements

- `fzf`
- `doas` (replace with `sudo` yourself if you desire)

### Probably already installed:

- `wireguard`
- `curl`
- `jq`

## Instructions

1. Log in to [IVPN](https://www.ivpn.net/account/login).
2. [Generate and download configuration files.](https://www.ivpn.net/account/wireguard-config)
3. Create `/etc/wireguard` if it does not exist.
    - Make sure it is readable by your user,
      for example if you are in the group `wheel` you could do as root
      `mkdir -p /etc/wireguard && chown root:wheel /etc/wireguard && chmod g+rx /etc/wireguard`.
3. Unzip the configuration files into `/etc/wireguard`.
    - As root, `cd /etc/wireguard && unzip /path/to/configs.zip`
4. Put `connect-ivpn` and `disconnect-ivpn` somewhere in `$PATH`
5. Profit!
