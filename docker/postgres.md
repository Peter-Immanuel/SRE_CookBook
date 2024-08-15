# How to Dump and Restore data in a Postgres Docker Instance

### Dump using 'pg_dump'
- docker exec -i pg_container_name /bin/bash -c "PGPASSWORD=pg_password pg_dump -U pg_username -p pg_port -d database_name" > /desired/path/on/your/machine/dump.sql
- docker exec container_id pg_dump -U pg_user -p pg_port -d pg_db > path/to/store/dump.sql

### Restore using 'psql'
- Copy file into new container
- docker exec -i pg_container_name /bin/bash -c "PGPASSWORD=pg_password psql -U pg_username -p pg_port -d database_name" < /path/on/your/machine/dump.sql
