     # Checking on the firewall

sudo ufw status verbose

# checking...

sudo nano /etc/default/ufw (check that IPV6=yes)

# re-establishing defaults

sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw allow 'Nginx Full' (allow Nginx traffic)

# enable

sudo ufw enable

# see if it’s working

sudo ufw status

> Status: active
>
> To Action From
>
> ---
>
> Nginx HTTP ALLOW Anywhere
> 22/tcp ALLOW Anywhere
> Nginx HTTP (v6) ALLOW Anywhere (v6)
> 22/tcp (v6) ALLOW Anywhere (v6)

Useful article: https://www.agwa.name/blog/post/fixing_the_addtrust_root_expiration
