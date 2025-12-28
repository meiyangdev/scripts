1. use session manager to connect to db instance, 
then enter `sudo su` and `docker exec -it imageID /bin/bash`,
and input `ENV`, `ENV["DATABASE_PASSWORD”]`know what database is and what password is 
start db console `bundle exec rails dbconsole`,
enter `\l` to list db,
enter `\du` to list users,
enter `\c`to list database name `\c postgres` to go inside of db console,
`\dn+ public`  to see schema privilege

```
PGPASSWORD=$DATABASE_PASSWORD bin/rails db
\x ON
```