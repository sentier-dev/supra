The file `vocab.sentier.dev` should be added to `/etc/nginx/sites-available/`, with the usual symlink to `/etc/nginx/sites-enabled/` and certs managed by certbot:

```console
sudo certbot --nginx -d vocab.sentier.dev --agree-tos --email someone@example.com
```

This config uses nginx as a caching reverse proxy:

```console
sudo mkdir -p /var/cache/nginx/vocab.sentier.dev
sudo chown www-data:www-data /var/cache/nginx/vocab.sentier.dev
```
