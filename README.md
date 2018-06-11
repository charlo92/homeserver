# How I did it

1. Install `>= ansible2.5`
2. Fill in inventory file `prod` with ssh connection information to a server.
3. Create .vault_pass with password for decrypt
4. Make sure you have the angstwad.docker_ubuntu role in your `~/.ansible/roles/` path
        ansible-galaxy install angstwad.docker_ubuntu
5. run
        ansible-playbook -i prod site.yml --vault-password-file .vault_pass

## Containers used

Below is a list of the containers used with links to their source. All credit to them, I stand on the shoulders of giants.

### Plex

@linuxserver/docker-plex

Your friendly-neighborhood media player

### Transmission/Open-VPN

@haugene/docker-transmission-openvpn

A combination of a bit torrent client and openvpn client.

This will require you to have a VPN subscription. Highly recommend Private Internet Access.

### Radarr

@linuxserver/docker-radarr

An automation tool to track movies.

### Sonarr

@linuxserver/docker-sonarr

An automation tool to track TV

### Jackett

@linuxserver/docker-jackett

A proxy server that standardizes communication for sonarr and radarr to search.

### Muximux

linuxserver/docker-muximux

A single place for your web applications. 

## Other Stuff

### Glances

This playbook installs glances on the host and runs its web application as a service to help monitor OS metrics. Also keeps a list of active containers.

## Things to Fix

## Legal Stuff

This code is posted exclusively for private use and should not be used for any illegal activity.
