# 🖥️ Complete Beginner’s Guide to Building a Homelab with Proxmox VE

Ready to build your very own homelab? This guide is for absolute beginners and will walk you through setting up a home server using Proxmox Virtual Environment (VE). By the end, you'll have a working server accessible from another computer, ready to run services like Home Assistant, Plex, Pi-hole, and more.

---

## 🌟 What's a Homelab and Why Proxmox?

A homelab is your own mini data center at home. It's perfect for hosting media servers (Plex), running home automation (Home Assistant), blocking ads (Pi-hole), learning IT skills, or self-hosting your own services instead of relying on cloud providers.

**Why use Proxmox VE?**

- 🆓 Free and open-source
- 🖱️ Easy-to-use web interface
- 🧱 Supports both virtual machines and lightweight containers
- 💪 Powerful features like backups and storage management

Proxmox lets you run multiple services on one physical machine. It's perfect for beginners and grows with you.

---

## 📦 What You'll Need

- A dedicated PC or server
- A CPU that supports virtualization (Intel VT-x or AMD-V)
- At least 4 GB of RAM (8 GB or more recommended)
- A 32 GB or larger SSD or HDD (SSD recommended)
- Ethernet connection (Wi-Fi not recommended)
- A second computer to access Proxmox
- A USB stick (8 GB or more)
- Internet access

Tip: Even old desktops or used mini-PCs (like Intel NUCs) work well.

---

## 🔽 Step 1: Download and Prepare the Proxmox Installer

1. Go to the Proxmox website and download the latest Proxmox VE ISO.
2. Download and install Balena Etcher or Rufus.
3. Plug in your USB stick.
4. Use the software to flash the Proxmox ISO to the USB stick.

Note: This will erase all data on the USB stick.

---

## 💿 Step 2: Install Proxmox on Your Server

1. Plug the bootable USB into your server.
2. Connect a monitor and keyboard to the server.
3. Turn on the server and enter the BIOS or boot menu (usually F2, F12, Del, or Esc).
4. Set the USB as the first boot device and save.
5. The Proxmox installer will load. Choose “Install Proxmox VE.”
6. Accept the license agreement.
7. Select the drive you want to install Proxmox on. This will be erased.
8. Set your region, timezone, and keyboard layout.
9. Create a strong root password and optional email address.
10. Set networking info:
    - Hostname (e.g., proxmox.local)
    - IP address (static recommended)
    - Gateway (usually your router IP, like 192.168.1.1)
    - DNS (router IP or 8.8.8.8)

Click install and wait for it to finish. Remove the USB when prompted and reboot.

---

## 🌐 Step 3: Access the Proxmox Web Interface

After reboot, the server will display a message like:

You can now log in to the web interface: https://192.168.1.100:8006

1. On your second computer, open a browser and go to the address shown.
2. You may see a security warning (because of the self-signed SSL certificate). Click “Advanced” and proceed.
3. Log in with:
    - Username: root
    - Password: the one you set during installation
    - Realm: pam

You're now inside the Proxmox dashboard!

---

## 🧰 Step 4: Update Proxmox

Keeping Proxmox up to date is important for security and stability.

1. Click “Shell” in the web interface or connect via SSH.
2. Run the update command:
   
   apt update && apt full-upgrade -y

3. Reboot if the system tells you a kernel update was installed.

---

## 🚀 Step 5: Your First Homelab Project

You’re ready to start building!

Some beginner-friendly ideas:

- 🏠 Home Assistant: Smart home automation
- 🎬 Plex: Media streaming
- 🚫 Pi-hole: Network-wide ad blocker
- 🐧 Ubuntu Server: Learn Linux and system admin skills

To create a VM or container:

1. In the Proxmox web UI, click “Create VM” or “Create CT.”
2. Follow the wizard and assign CPU, RAM, and disk space.
3. Upload an ISO for VMs (like Ubuntu or Windows).
4. Download LXC templates for containers directly in the interface.

---

## 🛠️ Tips for Beginners

- 🔒 Change the Proxmox port (default is 8006) and use a firewall.
- 💾 Use Proxmox's backup tools regularly.
- 📘 Learn one thing at a time — don’t try to do everything at once.
- 🤝 Join the community:
    - Reddit: r/homelab
    - Proxmox forums

---

## 🎉 Congratulations!

You’ve built your first Proxmox homelab server!

You’re now ready to:

- Host your own apps and services
- Explore virtualization and containers
- Learn IT and DevOps skills
- Build a secure, private, powerful home infrastructure

Have fun homelabbing!
