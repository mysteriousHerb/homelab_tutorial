# homelab_tutorial


---
### SECTION 1: TAILSCALE know-it-all
### Add tailscale to any docker container 
- https://github.com/2Tiny2Scale/tailscale-docker-sidecar-configs
- Use network_mode: service:xxx to put the tailscale container and the other container (e.g. adguard home) in one namespace
- to access the service directly without specifying the ports and use HTTPS, use serve (reverse proxy)

### Tailscale with another VPN?
- https://github.com/ryanlim/tailscale-nordvpn/tree/main
- qdm12/gluetun#2201
- https://lemmy.world/post/7281194

### Tailscale with caddy:
- https://www.youtube.com/watch?v=Vt4PDUXB_fg
- in the video, the private server is put on public dns, but it is only accessible when on tailnet. Also the tailscale is installed onto the caddy container / service to make them accesible. 

### Tailscale subnet (access other devices on the same IP address):
- subnet basically allows any device on the same IP address (192.168.1.xxx) to be accesible on the tailnet -> e.g. 192.168.1.2:8888
- Follow this to make it work https://tailscale.com/kb/1019/subnets?tab=linux#verify-your-connection

### Add cloudflare to any container
- https://www.reddit.com/r/homeassistant/comments/zp9l61/cloudflare_tunnel_for_ha_in_docker/
- https://www.reddit.com/r/homeassistant/comments/znjomt/ha_core_and_cloudflared_with_docker/


----
# Section 2: PROXMOX
### Make proxmox access to internet
- ensure dns is set (8.8.8.8)
- ensure the enterprise repo is unticked

### Helper code to install things into LCX
- https://tteck.github.io/Proxmox/#adguard-home-lxc
- can install the tailscale using the above thing, and then follow subnet thing to make the main host available





