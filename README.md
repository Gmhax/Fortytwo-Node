# Fortytwo-Node
Fortytwo is a decentralized AI protocol using swarm intelligence to overcome centralized AI scalability issues. It runs small AI models across distributed devices, tapping into idle computing power from laptops and desktops. This enables a scalable, efficient, and low-cost AI ecosystem.

![image](https://github.com/user-attachments/assets/ab96dfc1-c658-4b7c-b7be-ecb1181df5e9)

- Note: Before running this node, you need an activation code.
- If you haven't filled up yet: https://tally.so/r/wQzVQk

## Installation

## If Docker is already installed, skip this step.
```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl enable --now docker

```

## Navigate directory
```bash
mkdir ~/capsule-docker
cd ~/capsule-docker
```

## Create Dockerfile
```bash
nano Dockerfile
```
- Paste this code:
```bash
FROM debian:unstable

# Install required packages including libgomp1
RUN apt update && apt install -y \
    curl \
    unzip \
    libc6 \
    libgomp1 \
    nano

# Set working directory
WORKDIR /app

# Download and extract Fortytwo app
RUN curl -L -o fortytwo-console-app.zip https://github.com/Fortytwo-Network/fortytwo-console-app/archive/refs/heads/main.zip && \
    unzip fortytwo-console-app.zip

# Set working directory to the app folder
WORKDIR /app/fortytwo-console-app-main

# Copy run command only, activation code will be added manually later
RUN chmod +x linux.sh

# Default to bash so you can enter and run linux.sh manually with activation code
CMD ["/bin/bash"]

```

## Build & Run:
```bash
docker build -t fortytwo-capsule .
docker run -it --name fortytwo-dev fortytwo-capsule /bin/bash

```

## Execute
```bash
chmod +x linux.sh && ./linux.sh
```



- Select option [1-2]: 1

- You selected: Create a new identity with an invite code
- Enter your invite code: Check email

![image](https://github.com/user-attachments/assets/f92d6bbb-07b5-4d58-a0f7-1b105ebfb0ea)


- Every AI node in the Fortytwo Network has unique strengths.
- Choose how your node will contribute to the collective intelligence:



![image](https://github.com/user-attachments/assets/6bbba626-c70b-471b-b9ad-378072250b21)


- Note: you cant choose any, It depends on how much RAM is left on your system(VPS)

