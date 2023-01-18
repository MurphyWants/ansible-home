ansible.cfg: https://github.com/ansible/ansible/blob/stable-2.9/examples/ansible.cfg

# Ansible Home

## How to use

## Ansible.cfg

## Inventories

### Groups
Used for roles, apps, features etc
Used for locations & groups

### Variables
Used for customizations

### Tags
Used for specific commands

## Playbooks
Plan:
- main.yml
  - pkg_update.yml:
    - pkg_rhel7.yml: Setup repos, gpg keys
    - pkg_rhel8.yml: Setup repos, gpg keys
    - pkg_rhel9.yml: Setup repos, gpg keys
    - pkg_almalinux9.yml: Setup repos, gpg keys
    - pkg_update.yml: update everything, install everythig
  - podman_0_main.yml: Install podman, configure app layer??
    - podman_1_freshrss.yml: Pull latest podman, Install, setup, configure freshrss, systemd etc. WHEN app_freshrss
    - podman_1_nextcloud.yml: Pull latest podman, Install, setup, configure nextcloud, systemd etc. WHEN app_nextcloud
    - podman_1_vaultwarden.yml: Pull latest podman, Install, setup, configure vaultwarden, systemd etc. WHEN app_vaultwarden