# smartm2m-zena
[Technical Test DevOps ] SMARTM2M Indonesia - Zena Firdaus

I worked on this using Virtual Box with 3 VMs, specifications as follows:

Loadbalancer node 1CPU 2GB RAM 50GB HDD with ip 192.168.1.100

2 Backend nodes 1CPU 2GB RAM 50GB HDD with ip 192.168.1.101-102

for master Ansible I use WSL Ubuntu on my local computer.
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/377eee18-cd82-4d7d-b318-9865354eb4f8)

backend group if we hit IP hostname
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/45881356-8b1a-4bad-b90f-9b052efb835e)

for my Kubernetes cluster I use microk8s installed on node-master and node-worker

![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/3322c23f-1bb2-40b2-91ea-3570d2dfc413)

After initializing the master, do the microk8s add-node command, then a token will appear for the worker node
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/d3f8c18f-32fd-4717-9943-a5f255e937c3)
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/6b11d2ac-5771-4ae0-9271-ada4e60947a1)

