# Docker Notes — Day 9

## Docker Version

Output of `docker version`:

MCC@DESKTOP-PG2G4R4 MINGW64 ~/engineering-hadeelbanihani22-dotcom (pr-08-docker)
$ MCC@DESKTOP-PG2G4R4 MINGW64 ~/engineering-hadeelbanihani22-dotcom (pr-08-docker)
$ docker logs pg-prework
The files belonging to this database system will be owned by user "postgres".
This user must also own the server process.

The database cluster will be initialized with locale "en_US.utf8".
The default database encoding has accordingly been set to "UTF8".
The default text search configuration will be set to "english".

Data page checksums are disabled.

fixing permissions on existing directory /var/lib/postgresql/data ... ok
creating subdirectories ... ok
selecting dynamic shared memory implementation ... posix
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default time zone ... UTC
creating configuration files ... ok
running bootstrap script ... ok
sh: locale: not found
2026-03-04 10:11:20.953 UTC [35] WARNING:  no usable system locales were found
performing post-bootstrap initialization ... ok
syncing data to disk ... ok

initdb: warning: enabling "trust" authentication for local connections
initdb: hint: You can change this by editing pg_hba.conf or using the option -A, or --auth-local and --

Success. You can now start the database server using:

    pg_ctl -D /var/lib/postgresql/data -l logfile start

waiting for server to start....2026-03-04 10:11:21.623 UTC [41] LOG:  starting PostgreSQL 15.17 on x86_
2026-03-04 10:11:21.625 UTC [41] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-03-04 10:11:21.632 UTC [44] LOG:  database system was shut down at 2026-03-04 10:11:21 UTC
2026-03-04 10:11:21.637 UTC [41] LOG:  database system is ready to accept connections
 done
server started

/usr/local/bin/docker-entrypoint.sh: ignoring /docker-entrypoint-initdb.d/*

waiting for server to shut down....2026-03-04 10:11:21.725 UTC [41] LOG:  received fast shutdown reques
2026-03-04 10:11:21.731 UTC [41] LOG:  aborting any active transactions
2026-03-04 10:11:21.733 UTC [41] LOG:  background worker "logical replication launcher" (PID 47) exited
2026-03-04 10:11:21.733 UTC [42] LOG:  shutting down
2026-03-04 10:11:21.736 UTC [42] LOG:  checkpoint starting: shutdown immediate
2026-03-04 10:11:21.750 UTC [42] LOG:  checkpoint complete: wrote 3 buffers (0.0%); 0 WAL file(s) added=0.001 s; distance=0 kB, estimate=0 kB
2026-03-04 10:11:21.752 UTC [41] LOG:  database system is shut down
 done
server stopped

PostgreSQL init process complete; ready for start up.

2026-03-04 10:11:21.841 UTC [1] LOG:  starting PostgreSQL 15.17 on x86_64-pc-linux-musl, compiled by gc
2026-03-04 10:11:21.841 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-03-04 10:11:21.841 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-03-04 10:11:21.845 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-03-04 10:11:21.850 UTC [55] LOG:  database system was shut down at 2026-03-04 10:11:21 UTC
2026-03-04 10:11:21.854 UTC [1] LOG:  database system is ready to accept connections



## Hello World Test

Output of `docker run hello-world`:

[paste your hello-world output here]

## Stop and Restart

Commands:
```bash
docker stop pg-prework
docker restart pg-prework
docker logs pg-prework

## Postgres Container

Command used:

```bash
docker run -d \
  --name pg-prework \
  -e POSTGRES_PASSWORD=prework \
  -p 5432:5432 \
  postgres:15-alpine

  