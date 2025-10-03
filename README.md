Create a new Facebook alike social networking web app but it is distributed 
every user has his own account profile data on his PC Or Mac by running XAMPP server on evry user PC
please visit and download
https://vdoc.pub/documents/php-5-social-networking-7p3ojl4clj20

The friend of my friend is my friend
The ennemy of my friend is my ennemy

how to get ip adress of pc on internet running XAMPP

To get the IP address of your PC on the internet while running **XAMPP**, you need to find your **public (external) IP address**. XAMPP itself generally runs on your local machine using its **private (local) IP address** (usually $127.0.0.1$ or a $192.168.x.x$ address).

Here's how to find your public IP address:

## 🌐 Finding Your Public IP Address

Your public IP address is the one assigned to your network by your **Internet Service Provider (ISP)** and is visible to the rest of the internet.

1.  **Use a "What's My IP" Website:** The simplest and most common way is to use a search engine or a dedicated website.
    * Open any web browser on the PC running XAMPP.
    * Search on Google or another search engine for "**what is my ip address**" or "**my ip**".
    * The search engine results page will typically display your public IP address at the top.
    * Alternatively, visit a website like **ipconfig.me**, **whatismyip.com**, or **iplocation.net**. 

This IP address is what external users will need to try and access your XAMPP server, assuming you've configured your router (port forwarding) to allow external traffic to reach the PC running XAMPP.

***

## 💻 Finding Your Private IP Address

While not your *internet* IP, your PC's **private (local) IP address** is necessary for other devices on your *local network* (like a phone connected to the same Wi-Fi) to access XAMPP.

### **On Windows:**
1.  Open the **Command Prompt** (search for `cmd` in the Start menu).
2.  Type the command: `ipconfig`
3.  Look for the entry under **Ethernet adapter** or **Wireless LAN adapter** for your connection, specifically the line labeled **IPv4 Address**. This is your local IP (e.g., $192.168.1.5$).

### **On macOS/Linux:**
1.  Open the **Terminal**.
2.  Type the command: `ifconfig` or `ip a`
3.  Look for the active network interface (e.g., `eth0` for wired, `wlan0` or `en0` for wireless) and find the **inet** address. This is your local IP.

***

## ⚠️ Important Note for Accessing XAMPP Externally

Simply getting your public IP address isn't enough to let others on the internet access your XAMPP server. You will also need to:

1.  **Configure XAMPP/Apache:** Ensure the Apache configuration file ($httpd.conf$ or $httpd-vhosts.conf$) allows connections from external IPs (not just $127.0.0.1$).
2.  **Port Forwarding:** Set up **Port Forwarding** on your **router**. This tells your router to direct incoming traffic on the web server port (usually $80$ or $8080$) from your **Public IP** to the **Private IP** of the specific PC running XAMPP.

If you only want other devices on your **local network** to access it, you only need to use your PC's **Private IP address** (e.g., $192.168.1.5$) in their browser, and **Port Forwarding is NOT needed**.

Security Issue
https://support.microsoft.com/en-us/windows/firewall-and-network-protection-in-the-windows-security-app-ec0844f7-aebd-0583-67fe-601ecf5d774f
