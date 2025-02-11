# Readme

## Install

```
# dependencies:
sudo dnf install ansible-core ansible-collection-community-general
# or
ansible-galaxy role install -r requirements.yml

# setup
ansible-playbook  -bK playbooks/setup.yml
```

## Dependency Notes

- python3-gobject-base provides gi.repository
