# SDP
clusteredSBC

-Acquired Rpi-5's for clustering through Kubernetes K3S on standard 64-bit OS.

-install K3S through website commands. 

-**master node **

  -enable control groups for containerized environments

  -do this by through nano /boot/firmware/cmdline.txt and add "cgroup_memory=1 cgroup_enable=memory" save/exit, and proceed to (curl -sfL https://get.k3s.io | sh -)

  -get node-token with (/var/lib/rancher/k3s/server/node-token)

-**worker nodes **

  -(curl -sfL https://get.k3s.io | K3S_URL=https://myserver:6443 K3S_TOKEN=mynodetoken sh -)

  -K3S_URL = ip address of master node

  -K3S_TOKEN = value from "node-token" above

  -Repeat for each node pi

<img width="248" alt="Screenshot 2025-03-18 at 12 19 49 AM" src="https://github.com/user-attachments/assets/6904609a-35ba-44cc-acff-d6f8badd8b10" />



-install docker through website commands.


<img width="332" alt="Screenshot 2025-03-18 at 12 39 08 AM" src="https://github.com/user-attachments/assets/e95f1494-da9d-4224-8c68-1728d7d57601" />


3/18/25: Working on containeriizing code for deployment and implementing some power over ethernet (PoE) for a more professional setup.


