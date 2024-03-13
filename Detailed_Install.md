Install ubuntu server 22.04.3 LTS
Created and valid as of 23 Nov 2023
Joel Templeman

Create with a non-root user (This sample uses <isocmb> as the user, so replace with your own username)

sudo apt-get update

apt list --upgradable

sudo apt upgrade -y (restart services if needed)

sudo apt-get install nginx -y

##sudo ufw allow 'Nginx HTTP'

##sudo ufw allow 'OpenSSH'

##sudo ufw enable

systemctl status nginx (Should report: "Active: active (running)")

Ctrl C to break

##sudo apt install certbot python3-certbot-nginx -y

##sudo nano /etc/nginx/sites-available/default     clearwaterroad.ddns.net

sudo nginx -t (Should report: nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful)

##sudo systemctl reload nginx

##sudo ufw allow 'Nginx Full'

##sudo ufw delete allow 'Nginx HTTP'

##sudo certbot --nginx -d <mydomain> -d www.<mydomain>

cd ~/

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

source ~/.bashrc

nvm install v16.20.2

sudo apt-get update

sudo apt-get install -y ca-certificates curl gnupg

sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg

##NODE_MAJOR=16
##NODE_MAJOR=18
##NODE_MAJOR=20
##NODE_MAJOR=21

echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_16.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

sudo apt-get update

sudo apt-get install nodejs -y
	
node -v

nodejs -v

##nvm install stable

curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt install yarn -y

yarn --version

sudo curl --compressed -o- -L https://yarnpkg.com/install.sh | bash

**Open a 2nd terminal**

git clone https://github.com/JoelTempleman/retro-env-can-weather-chan.git

cd retro-env-can-weather-chan

yarn install

##npm install npm

##npm start

npm install -g pm2

pm2 start backend.js

pm2 startup systemd

sudo env PATH=$PATH:/home/isocmb/.nvm/versions/node/v16.20.2/bin /home/isocmb/.nvm/versions/node/v16.20.2/lib/node_modules/pm2/bin/pm2 startup systemd -u isocmb --hp /home/isocmb

##sudo ufw allow 8600

##sudo ufw allow 8080

npx update-browserslist-db@latest -y

yarn build

##npm install caniuse-lite

##npm audit fix

