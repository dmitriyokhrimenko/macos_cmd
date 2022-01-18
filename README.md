# MacOS cmd

### Start psql
```bash
pg_ctl -D /usr/local/var/postgres start
```

### Login to psql
```bash
psql -d mydb -U myuser
```

### Change password to postgres user (OS level - ubuntu, centos, etc)
```bash
sudo -u postgres psql postgres

sudo -u <OS_username> psql <db_role>

ALTER USER postgres WITH PASSWORD 'postgres';
```

### Create db inside a postgres
```bash
create database <dbname>;
```

### Grant all privilegies on the target db and user
```bash
grant all privileges on database <dbname> to <username>;
```

### Create user in psql throught the OS cmd
```bash
sudo -u postgres createuser <username>
```

### Create user in psql with password (from the psql cmd)
```bash
create user <username> with encrypted password '<password>';
```

### Unblock postgres service
```bash
rm /usr/local/var/postgres/postmaster.pid
brew services restart postgresql
```
