---
title: 'Install Grav'
taxonomy:
    category:
        - docs
menu: 'Install Grav'
---

```markdown
wget https://getgrav.org/download/core/grav-admin/1.5.8
7z x 1.5.8
cd grav-admin
sudo apt-get install php7.0-mbstring
sudo service apache2 restart
sudo chown -R www-data ; www-data .
sudo apt-get install sqlite php-sqlite3

# Update Grave
bin/gpm selfupgrade -f
# Update Plugins 
bin/gpm update -f
# Install theme
bin/gpm install learn2-git-sync

nano /etc/apache2/apache2.conf
	<Directory /var/www/grav-admin>
    	    AllowOverride All
	</Directory>
```

## add Let's Encrypt subdomain
```markdown
certbot --expand -d tsst16.tk,docs.tsst16.tk
```
