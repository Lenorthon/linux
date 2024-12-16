### Se connecter
```
PS C:\WINDOWS\system32> ssh root@wilfart.fr -p 6213
```

### Installer nginx
```
apt install nginx
```

### Configuration du firewall
```
apt install ufw
ufw enable
ufw allow 6213/tcp
```

### Configurations des permissions
```
chmod 644 /etc/nginx/sites-enabled/*
chmod 644 /etc/nginx/sites-available/*
chmod 644 /etc/nginx/nginx.conf
```
### Outil de sécurité
```
sudo dnf install fail2ban
nano /etc/fail2ban/jail.local
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
```
### Bonnes pratiques 
```
sudo dnf update -y
nano /etc/sudoers
sudo systemctl list-units --type=service
```

