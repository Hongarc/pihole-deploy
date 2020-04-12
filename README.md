# pihole-deploy

## Usage
 - Require `docker` + `docker-compose`
 - Start `pihole` with Docker compose: `docker-compose up -d`
 - Change your dns to `127.0.0.1` (or IP in LAN for another device in LAN)

*__Note:__ my Adlists `https://raw.githubusercontent.com/Hongarc/pihole-deploy/master/custom/data.txt`*

## Dashboard

Go to `http://localhost/admin/index.php`, if your 80 port is used, change to another port in `docker-compose.yaml`

Example 8080 port:

 - Change `- "80:80/tcp"` to `- "8080:80/tcp"`
 - Dashboard is `http://localhost:8080/admin/index.php`

### Password

If you don't set env `WEBPASSWORD`, pihole create a random password and remember it.

To reset, `run docker-compose exec pihole pihole -a -p` (first `pihole` is service's name in `docker-compose.yaml`)

### Export and import

Go to `Dashboard > Settings > Teleporter`

## Get Adlists

 - https://firebog.net/
