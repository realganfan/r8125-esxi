# Realtek RTL8125 NIC driver for ESXi 6.7

This source code is based on realtek official source, VMware-ESXI-67U3-ODP and VMware-TOOLS-10.2.0-ODP.

Just do these steps:
- Prepare the building environment, I did it on CentOS 7
- Log in with root, make a folder name 'build' on /, make folder toolchain and vsphere in /build.
- Copy and extract gcc-4.8.0, binutils-2.22, glibc-2.3.4-2.41 to /build/toolchain/src 
- Compile the toolchain, dest path is /build/toolchain/lin64
- Extract and copy vmkdrivers-gpl from 67U3-ODP to /build/vsphere
- Copy build-r8125.sh to /build/vsphere/vmkdrivers-gpl/
- Copy r8125 folder to /build/vsphere/vmkdrivers-gpl/vmkdrivers/src_9/drivers/net
- Run build-r8125.sh
