# How I did it
1. Install `>= ansible2.4`
2. Fill in inventory file `prod` with ssh connection information to a server.
2. Create .vault_pass with password for decrypt
3. Make sure you have the angstwad.docker_ubuntu role in your `~/.ansible/roles/` path
        ansible-galaxy install angstwad.docker_ubuntu
4. run
        ansible-playbook -i prod site.yml --vault-password-file .vault_pass

## Containers used
Below is a list of the containers used with links to their source. All credit to them, I stand on the shoulders of giants.

### Plex
@linuxserver/docker-plex

Your friendly-neighborhood media player

### Transmission/Open-VPN

@haugene/docker-transmission-openvpn

A combination of a bit torrent client and openvpn client.

This will require you to have VPN subscription. Highly recommend Private Internet Access.

### Radarr
@linuxserver/docker-radarr

An automation tool to track movies.

### Sonarr
@linuxserver/docker-sonarr

An automation tool to track TV

### Jackett
@linuxserver/docker-jackett

A proxy server that standardizes communication for sonarr and radarr to search.

## Testing

I have found it useful t
## Things to Fix

## Legal Stuff
This code is posted exclusively for private use and should not be used for any illegal activity.
