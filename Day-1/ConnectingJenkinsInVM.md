### Steps to Deploy Jenkins in Azure VM
1. Connect to Your Ubuntu VM
```bash
ssh -i your-key.pem azureuser@YOUR_VM_PUBLIC_IP
```

2. Update the System
```bash
sudo apt update
sudo apt update -y
```

3. Install Java (Jenkins Requires It)
```bash
sudo apt install fontconfig openjdk-17-jre -y
#check java version for 17
java -version
```

4. Add Jenkins Key
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo gpg --dearmor -o /usr/share/keyrings/jenkins-keyring.gpg
```

5. Add Jenkins Repository
```bash
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.gpg] https://pkg.jenkins.io/debian-stable binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list
```

6. Install Jenkins
```bash
sudo apt update
sudo apt install jenkins -y
```
7. Start Jenkins
```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins
```

8. Open Port 8080 in Azure Portal
- Azure Portal → Your VM → Networking
- Click Add inbound port rule
- Set destination port to 8080 → Protocol TCP → Click Add

9. Get Unlock Password
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
10. Access Jenkins in Browser
http://YOUR_VM_PUBLIC_IP:8080