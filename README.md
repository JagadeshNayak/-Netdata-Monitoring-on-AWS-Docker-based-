# 📊 Netdata Monitoring on AWS EC2 Ubuntu (Docker-based)

**🚀 Objective**

Install and run Netdata using Docker on an AWS EC2 Ubuntu server to monitor system resources like CPU, memory, disk, and Docker containers in real-time.

# 🛠️ Tools Used
Netdata (Monitoring tool)

Docker (Container runtime)

AWS EC2 (Ubuntu server)

# 🧰 Prerequisites
**✅ 1. Update the System**
sudo apt update 

**✅ 2. Install Docker (if not already installed)**

sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker

**Verify Docker:**

docker --version

# 🐳 Run Netdata with Docker

docker run -d --name=netdata -p 19999:19999 netdata/netdata

<img width="955" alt="4" src="https://github.com/user-attachments/assets/1f16edc9-34ed-479d-ae8b-48327f6dd14f" />

# 🌐 Access Netdata Dashboard

In your browser, go to:

http://<your-ec2-public-ip>:19999

<img width="959" alt="6" src="https://github.com/user-attachments/assets/e8b434d2-7ca1-468b-a715-a445045942c8" />


# 📌 Make sure port 19999 is open in your EC2 security group settings:

Go to EC2 Dashboard > Security Groups

Edit Inbound Rules

Add a rule:

Type: Custom TCP

Port: 19999

Source: 0.0.0.0/0 (or restrict to your IP)

<img width="958" alt="5" src="https://github.com/user-attachments/assets/44b824f8-f8c4-418b-8da7-8c2ed73ee5f0" />

# 📈 What You Can Monitor
CPU Usage

Memory (RAM)

Disk I/O

Network Traffic

# 🔔 Explore Alerts and Logs
Logs
To view logs inside the container:

docker exec -it netdata bash

cd /var/log/netdata

ls

<img width="945" alt="log" src="https://github.com/user-attachments/assets/469bfea9-c02f-406b-ab66-8afe16d8358a" />

# As per the project objectives
**CPU of Netdata**:Displays real-time CPU usage, including system, user, nice, and idle time, helping identify processing load and bottlenecks.

<img width="952" alt="Directories" src="https://github.com/user-attachments/assets/9a088af0-2390-40c1-a2d7-17c1628e8874" />

**Directories**: Monitors disk usage and I/O for each directory, showing read/write stats and storage consumption to track file system health.

<img width="952" alt="Directories" src="https://github.com/user-attachments/assets/b5a8afc5-b5c5-4ded-9419-5a8488b16c48" />

**I m happy to share the successful completion of my mini-project: Monitoring System Resources Using Netdata on an AWS EC2 Ubuntu Server with Docker.**

In this project,:

Deployed Netdata in a Docker container

Monitored CPU, memory, disk, and Docker container metrics

Accessed real-time system performance via a web dashboard

Explored Netdata alerts, charts, and logs for deeper insights

This hands-on task helped me strengthen my understanding of system monitoring and containerized deployments on cloud infrastructure.

**Thanks to  Elevate Labs**

 # Gugulothu Jagadish













