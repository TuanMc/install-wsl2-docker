# Install Docker on WSL2 

## 1. Install WSL2:
- Open Windows Store and search `Windows Subsystem for Linux`
- Click on **GET**

## 2. Install WSL2's distribution
- Open `PowerShell` and enter:
  ```
  wsl --install
  ```
  or to choose a specific distribution, you can use:
  ```
  wsl --install -d <Distro>
  ```
  Example: `wsl --install -d Ubuntu-20.04`
  
- Enter **username**, and **password** for the new installed distribution
![image](https://github.com/TuanMc/install-wsl2-docker/assets/30165388/73b1a14e-051d-4a5d-bf38-276c3a028a2a)

Read more:
[Link](https://vvgsrk.medium.com/install-wsl-2-ubuntu-20-04-lts-on-windows-10-and-open-visual-studio-code-from-the-terminal-b85889157c82)

## 3. Install and update the newest packages on Ubuntu
- Open **wls2**'s terminal
- Enter
  ```
  sudo apt-get upgrade
  ```
Read more:
[Link](https://www.cyberciti.biz/faq/upgrade-update-ubuntu-using-terminal/)

## 4. Install Docker
- [Optional] Login to **wsl** as **root** account
- [Optional] Enter command `sudo su -` to allows you to run a command as **root**
- To install **Docker**, enter command:
```
sudo apt install docker.io -y
```
Here, the “-y” option is used to grant the permission to install required packages automatically

![image](https://github.com/TuanMc/install-wsl2-docker/assets/30165388/e1e188de-6592-44a5-b8fd-6cdb15a2093d)

![image](https://github.com/TuanMc/install-wsl2-docker/assets/30165388/6b737f5e-3bee-4fac-ac1c-dce583d729f8)

- Login to **Docker Hub** using command
```
docker login
Username: 
Password:
```
![image](https://github.com/TuanMc/install-wsl2-docker/assets/30165388/4cdac515-bfe3-4c37-ba0e-267917d26e48)

- Make a new user
```
sudo usermod -aG docker $User
```
- Check Docker Version
```
docker --version
```
![image](https://github.com/TuanMc/install-wsl2-docker/assets/30165388/f8f52601-2225-43bd-adcc-f08212abef43)

References:
- [Install docker](https://linuxhint.com/run-docker-in-wsl-without-docker-desktop/)
- [Login Docker via CMD](https://linuxhint.com/how-to-login-into-docker-via-command-prompt/)

## [Optional] Install other dependecies
- Install **git**: `sudo apt install git`

  [Read more](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-22-04)

- Install **nginx**: `sudo apt install nginx`

  [Read more](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04)

- Update **node**:
```
sudo npm cache clean -f
sudo npm install -g n
sudo n stable
```
or using `sudo n latest` to get latest version

Then, enter `hash -r` to clear cache

Check node version: `node -v`

[Read more](https://askubuntu.com/a/480642)

-  Install **npm**: `sudo apt install npm`
