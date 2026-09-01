NotRyxenYT KVM Bot - converted from the supplied LXC bot

Changes:
- Replaced LXC/liblxc lifecycle operations with KVM/libvirt/virsh/qemu-img/virt-install.
- Ubuntu 20.04/22.04/24.04 and Debian 10/11/12/13 use official cloud images.
- Added cloud-init setup for root SSH, qemu-guest-agent and tmate.
- Branding: NotRyxenYT.
- Main admin ID: 1520903362667876523.
- Discord logo URL updated to the requested server icon.
- Existing database/Discord command structure is retained where possible.

KVM host prerequisites:
sudo apt update
sudo apt install -y qemu-kvm libvirt-daemon-system libvirt-clients virtinst qemu-utils cloud-image-utils curl

Recommended:
sudo usermod -aG libvirt,kvm $USER
sudo systemctl enable --now libvirtd

The bot should have permission to access libvirt and /var/lib/libvirt/images.
Set DISCORD_TOKEN before running.
