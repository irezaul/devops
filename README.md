# 

### Run New VM-Machine 
##### * first install 
```bash
sudo apt-get update
```
##### 2nd Process- on Serverpc
```bash
sudo apt install sshd 
sudo apt install openssh-server
```
##### 3rd check sshd status
```bash
systemctl status sshd
```
##### 4th Enable ssh connection
```bash
systemctl enable ssh
```
##### now configure sshd_config

##### go to 
```bash
nano /etc/ssh/sshd_config
```
#### Uncomment the port 22 & PermitRootLogin yes
```bash
uncomment port 22
PermitRootLogin yes
```
![Port22](https://user-images.githubusercontent.com/77927449/126047292-137b0096-4773-4dee-a77c-58b99887e298.png)

#### change the hostname
```bash
sudo hostnamectl set-hostname master-node
```
#### if not change hostname follow the step
```bash
nano /etc/gdm3/custom.conf
```
> type `AllowRoot=true`
> then 
```bash
nano /etc/pam.d/gdm-password
```
> uncomment the `Auth Required`

![Auth](https://user-images.githubusercontent.com/77927449/126047796-e2379dd2-cd36-4ef6-bb71-b8e068b777c5.gif)

> save & reboot
#### Now use again the change the hostname
```bash
sudo hostnamectl set-hostname master-node
```

