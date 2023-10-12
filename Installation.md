# Install Home Assistant Operating System

- [DOWNLOAD THE APPROPRIATE IMAGE](https://www.home-assistant.io/installation/alternative/)

- [VirtualBox (.vdi)](https://github.com/home-assistant/operating-system/releases/download/10.5/haos_ova-10.5.vdi.zip)

- [KVM/Proxmox (.qcow2)](https://github.com/home-assistant/operating-system/releases/download/10.5/haos_ova-10.5.qcow2.xz)

- [VMware ESXi/vSphere (.ova)](https://github.com/home-assistant/operating-system/releases/download/10.5/haos_ova-10.5.ova)

----

- ### KVM

```bash
cd /var/lib/libvirt/images/
```

```bash
virt-install --import --name hassos \
--memory 8192 --vcpus 8 --cpu host \
--disk /var/lib/libvirt/images/haos_ova-10.5.qcow2,format=qcow2,bus=virtio \
--network bridge=virbr0,model=virtio \
--osinfo detect=on,require=off \
--graphics none \
--noautoconsole \
--boot uefi
```

```bash
virsh list --all
virsh autostart hassos
```

```bash
virsh net-list
virsh net-info default
virsh net-dhcp-leases --network default
```

- Install qemu-agent on vm host

```bash
virsh list --all
virsh domiflist hassos
virsh domifaddr hassos
```

```
http://127.0.0.1:8123
```

----
- HASSOS Set Static IP Address

```bash
- ha network info

- ha network update enp0s2 --ipv4-address 192.168.122.90/24 --ipv4-gateway 192.168.122.1

/sbin/reboot now

```
http://192.168.122.90:8123

----
### Docker installation

```cmd
docker pull homeassistant/home-assistant

# docker run -d –name = homeassistant -v your_home_directory:/config –net=host homeassistant/home-assistant

docker run --name home-assist -p 8123:8123 -d homeassistant/home-assistant

docker ps -a
```



----
