# MacOS cmd

### Start psql
```bash
pg_ctl -D /usr/local/var/postgres start
```

### Change password to postgres user
```bash
sudo -u postgres psql postgres

ALTER USER postgres WITH PASSWORD 'postgres';
```

### Login to psql
```bash
psql -d mydb -U myuser
```

### Create user in psql
```bash
sudo -u postgres createuser <username>
```

### Unblock postgres service
```bash
rm /usr/local/var/postgres/postmaster.pid
brew services restart postgresql
```
