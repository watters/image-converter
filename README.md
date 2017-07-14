# Image Converter

This is an experimental script that can be used to create a Triton KVM
image from a from a given qcow2, vmdk or raw image file.

See `convert-image -h` for usage.

## Prerequisites

This script is known to work with `qemu-img` version 0.14.1 and *should*
work with newer versions of `qemu-img` as well.

This script expects to be run on a Triton/SDC compute node with privileges
to create a VM using `vmadm` and directly access the associated zone's
zvol (e.g. `/dev/zvol/rdsk/zones/"$VM_UUID"-disk0`)