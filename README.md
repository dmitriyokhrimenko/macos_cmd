# MacOS cmd

### Start psql
```bash
pg_ctl -D /usr/local/var/postgres start
```

### Login to psql
```bash
psql -d mydb -U myuser
```

### Get list of users in psql
```bash
psql postgres
```

```bash
\du
```

### Create user in psql throught the OS cmd
```bash
sudo -u postgres createuser <username>
```

### Create user in psql with password (from the psql cmd)
```bash
create user <username> with encrypted password '<password>';
```

### Grant permission to create database
```bash
ALTER USER username CREATEDB;
```

### Grant all privilegies on the target db and user
```bash
grant all privileges on database <dbname> to <username>;
```

### Create db inside a postgres
```bash
create database <dbname>;
```

### Read only user in Postgres
```bash
CREATE ROLE readonly;

GRANT CONNECT ON DATABASE closer_pets_staging_db TO readonly;

GRANT USAGE ON SCHEMA public TO readonly;

GRANT SELECT ON ALL TABLES IN SCHEMA public TO readonly;

CREATE USER readonly_user WITH PASSWORD '4Sh5W#P0rxwOGl0&';

GRANT readonly TO readonly_user;

-- GRANT ALL PRIVILEGES ON TABLE pg_enum TO postgres;

SELECT usename AS role_name FROM pg_catalog.pg_user ORDER BY role_name desc;
```

### Change password to postgres user (OS level - ubuntu, centos, etc)
```bash
sudo -u postgres psql postgres

sudo -u <OS_username> psql <db_role>

ALTER USER postgres WITH PASSWORD 'postgres';
```

### Unblock postgres service
```bash
rm /usr/local/var/postgres/postmaster.pid
brew services restart postgresql
```
