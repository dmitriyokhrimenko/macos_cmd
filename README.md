# MacOS cmd

### Start psql
```bash
pg_ctl -D /usr/local/var/postgres start
```

### Login to psql
```bash
psql -d mydb -U myuser
```

### Create user in psql
```bash
sudo -u postgres createuser <username>
```
