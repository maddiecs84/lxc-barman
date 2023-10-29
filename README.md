# lxc-barman

A Debian LXC image containing [Barman](https://pgbarman.org/) for performing backups of PostgreSQL.

## Configuration

Once running run login to your instance and run `/etc/barman/add-server.sh` to add a PostgreSQL server to backup.

Alternatively provide your configuration as file to the script, containing the following

```bash
DB_HOST=
DB_PORT=5432
DB_USER=
DB_USER_PASSWORD=
DB_USER_DATABASE=
DB_REPLICATION_USER=
DB_REPLICATION_PASSWORD=
DB_BACKUP_METHOD=postgres
DB_SLOT_NAME=barman
DB_POSTGRES_PUBLIC_KEY=
DB_SERVER_POSTGRES_PASSWORD=
```

```bash
/etc/barman/add-server.sh "my-server-x.env"
```

## Why?

I run a Home Lab on Proxmox and my preference is to manage CTs rather than a VM or CT running Docker images (with something like Portainer).