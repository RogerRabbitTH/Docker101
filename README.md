
# ติดตั้ง Docker

## เอามาจาก ChatGPT ทำตามขั้นตอนได้เลย
ขั้นแรกคือการติดตั้ง Docker บน Ubuntu โดยใช้คำสั่งต่อไปนี้ใน Terminal

1. อัปเดตระบบแพคเกจของคุณ

```
sudo apt update
```

2. ติดตั้งพื้นฐานที่จำเป็นสำหรับการติดตั้ง Docker
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

3. เพิ่ม GPG key ของ Docker
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

4. เพิ่ม Docker repository เข้าไปในตัวเลือกการติดตั้งแพคเกจของคุณ
```
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

5. อัปเดตระบบแพคเกจอีกครั้ง
```
sudo apt update
```

6. ติดตั้ง Docker
```
sudo apt install docker-ce docker-ce-cli containerd.io
```

7. ตรวจสอบว่า Docker ติดตั้งเรียบร้อยแล้วโดยใช้คำสั่ง
```
sudo docker run hello-world
```
