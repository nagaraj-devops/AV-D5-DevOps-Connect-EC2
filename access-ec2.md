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
```chmod 400 ~/keys/mykey.pem```

## 4. SSH into EC2

Run:
```ssh -i ~/keys/mykey.pem ubuntu@<PUBLIC-IP>```

👉 Replace: ~/keys/mykey.pem → path to your key file.

      ubuntu → the username (depends on AMI):
      
      Amazon Linux → ec2-user
      
      Ubuntu → ubuntu
      
      RHEL → ec2-user or root
      
      CentOS → centos

      <PUBLIC-IP> → your EC2 public IP.

Example:

ssh -i ~/keys/mykey.pem ec2-user@54.201.123.45
