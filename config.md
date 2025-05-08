# 1 / Generate pem files
sudo certbot certonly --standalone -d yourdomain.com or sudo certbot certonly --nginx -d yourdomain.com

# 2/  Give right to pem files
sudo chmod 644 /etc/letsencrypt/live/yourdomain.com/fullchain.pem
sudo chmod 640 /etc/letsencrypt/live/yourdomain.com/privkey.pem
sudo chown root:root /etc/letsencrypt/live/yourdomain.com/privkey.pem 

# 3/ Look at the docker-compose.yml file for all configs