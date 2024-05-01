# Ubuntu 22.04 docker image with SSH setup for Kubernetes

This Dockerfile contains the following workarounds to allow SSH through Kubernetes and CHI@Edge:

- Allow Root Login 
- Permit login with public key and enable reading via Authorized_keys file
- change the behavior of the pam_loginuid.so module from required to optional
- Create an authorized keys folder (Note: the user still has to set the proper permissions on the file using chmod given that this file is created at build time in a different container with different permissions)
- Start the SSHD daemon
