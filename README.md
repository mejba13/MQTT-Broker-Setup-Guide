# MQTT-Broker-Setup-Guide

Step-by-step guide to setting up and testing an MQTT broker on an AWS EC2 instance. Includes installation, configuration, local and remote testing, and troubleshooting tips. Ideal for IoT and real-time applications.

---

## 🚀 Setup Steps

### 1️⃣ Launch an EC2 Instance
- Start with an AWS EC2 instance (Ubuntu 22.04 LTS).
- Ensure the Security Group allows port `1883` for MQTT traffic.

### 2️⃣ Install Mosquitto MQTT Broker
Run the following commands to install and start Mosquitto:
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install mosquitto mosquitto-clients -y
sudo systemctl start mosquitto
```

### 3️⃣ Configure Mosquitto
Edit the configuration file:
```bash
sudo nano /etc/mosquitto/mosquitto.conf
```
Adjust settings (e.g., `allow_anonymous true`) and restart the service:
```bash
sudo systemctl restart mosquitto
```

### 4️⃣ Test Locally
Use Mosquitto clients to test publish/subscribe:
```bash
mosquitto_sub -h localhost -t test -v
mosquitto_pub -h localhost -t test -m "Hello from server"
```

### 5️⃣ Test Remote Connectivity
Ensure the Security Group allows external traffic on port `1883`. Test using an external MQTT client:
```bash
mosquitto_pub -h <Public_IP> -t test -m "Hello from external client"
```

---

## 📸 Screenshots

### MQTT Server Setup
![MQTT Server Setup](https://s3.us-east-1.amazonaws.com/mejba.me/aws/mqtt-server-setup.png)

### MQTT Server Running
![MQTT Server Running](https://s3.us-east-1.amazonaws.com/mejba.me/aws/mqtt-server-running.png)

---

## 🔗 Let's Connect  

- **GitHub**: [mejba13](https://github.com/mejba13)  
- **GitLab**: [Engr Mejba Ahmed](https://gitlab.com/engr-mejba-ahmed)  
- **LinkedIn**: [Engr Mejba Ahmed](https://www.linkedin.com/in/engr-mejba-ahmed-795ab3165/)  
- **YouTube**: [Engr Mejba Ahmed](https://www.youtube.com/channel/UCfLIuNxRfXT7HmvvB9Ld0SA)  
- **Instagram**: [engr_mejba_ahmed](https://www.instagram.com/engr_mejba_ahmed/)  
- **Twitter (X)**: [@mejba_92](https://x.com/mejba_92)  
- **Facebook**: [Engr Mejba Ahmed](https://www.facebook.com/engrmejbaahmed/)  
- **Medium**: [Engr Mejba Ahmed](https://medium.com/@engr-mejba-ahmed)  
- **Reddit**: [engrmejbaahmed](https://www.reddit.com/user/engrmejbaahmed/)  
- **LeetCode**: [engrmejbaahmed](https://leetcode.com/u/engrmejbaahmed/)  
- **TryHackMe**: [EngrMejbaAhmed](https://tryhackme.com/r/p/EngrMejbaAhmed)  
- **Codewars**: [mejba13](https://www.codewars.com/users/mejba13)  
- **HackerOne**: [Engr Mejba Ahmed](https://hackerone.com/engrmejbaahmed?type=user)  
- **HackerRank**: [Dashboard](https://www.hackerrank.com/dashboard)  
- **Bugcrowd**: [EngrMejbaAhmed](https://bugcrowd.com/EngrMejbaAhmed)  
- **PentesterLab**: [lucid_hacker_721](https://pentesterlab.com/profile/lucid_hacker_721)  
- **DEV.to**: [Engr Mejba Ahmed](https://dev.to/engrmejbaahmed)  
- **Pinterest**: [engrmejbaahmed](https://www.pinterest.com/engrmejbaahmed/)  
- **Quora**: [Engr Mejba Ahmed](https://www.quora.com/profile/Engr-Mejba-Ahmed)  

---

Let me know if you'd like to make any further adjustments! 🚀
