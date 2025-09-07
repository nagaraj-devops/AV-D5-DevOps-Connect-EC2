# 🔹 Steps to Connect to EC2 (Linux Instance)

## 1. Launch EC2 Instance
- Make sure your instance is **running** in the AWS console.  
- Note its **Public IPv4 address** (example: `3.112.45.89`).  
- Ensure **port 22 (SSH)** is open in the **Security Group**.  

---

## 2. Download Key Pair (.pem)
- When launching, AWS gives you a **key pair file** (e.g., `mykey.pem`).  
- This is your **private key** to authenticate.  
- Move it to a safe location, e.g., `~/keys/mykey.pem`.  

---

## 3. Set Permissions on Key
Run in your terminal:
```bash
chmod 400 ~/keys/mykey.pem
