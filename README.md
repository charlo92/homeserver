# How I did it

1. Install `>= ansible2.5`
2. Fill in inventory file `prod` with ssh connection information to a server
3. SEn
4. Create .vault_pass with password for decrypt during provision
5. Make sure you have the angstwad.docker_ubuntu role in your `~/.ansible/roles/` path
        ansible-galaxy install angstwad.docker_ubuntu
6. run
        ansible-playbook -i prod site.yml --vault-password-file .vault_pass

## Containers used

Below is a list of the containers used with links to their source. All credit to them, I stand on the shoulders of giants.

NOTE: Due to the way docker interacts with the file system, all static config directories should be on the docker host and not from a Network Drive. Media files are ok, but no config files.

@linuxserver/docker-plex: Your friendly-neighborhood media player
@haugene/docker-transmission-openvpn
@linuxserver/docker-radarr
@linuxserver/docker-sonarr
@linuxserver/docker-jackett

## Other Stuff

### Caddy

This pla

### Glances

This playbook installs glances on the host and runs its web application as a service to help monitor OS metrics. Also keeps a list of active containers.

### .kitchen.yml file

It is useful to have a quick way to test the playbook and not change the server at all. Test-kitchen has a plugin to provision vagrant boxes with Ansible. Makes testing really easy.  

## Things to Fix

## Improvements

Simple nginx proxy server to route traffic between containers with pseudo-DNS names.

Post system requirements.

## Legal Stuff

This code is posted exclusively for private use and should not be used for any illicit activity.
