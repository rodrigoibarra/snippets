# Certbot Renewal

Here's how to manually renew ssl certificate using certbot.

- Loginto server.
- Stop Nginx, it trys to use the same ports as Nginx so if you dont stop it, it fails. `sudo systemctl stop nginx`
- Run Certbot to renew `sudo ./certbot-auto renew`
- Restart Nginx `sudo systemctl restart nginx`

And that's about it, I should set up a cron job but since it starts and stops Nginx I *basically don't trust it to do it on it's own.* 