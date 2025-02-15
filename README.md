# Readme

## Dependencies

```
# dependencies:
sudo dnf install ansible-core ansible-collection-community-general ansible-collection-community-libvirt
```

Notes: 

- community.general.dnf
    - python3-gobject-base provides gi.repository
- community.libvirt
    - python3-lxml

# Run

```
ansible-playbook  -bK playbooks/setup.yml
```


# DNS

Per man page of systemd-resolve:

```
/etc/systemd/resolved.conf.d/
[Resolve]
DNS=192.168.124.1
Domains=~virtual.example
```

# XML tricks

```
virsh net-dumpxml default | xmllint --xpath 'string(//domain/@name)' -
virtual.example
```
