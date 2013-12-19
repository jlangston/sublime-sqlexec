sublime-sqlexec
===============

A Plugin for running SQL commands in Sublime Text.

Compatibility: MySQL, PostgreSQL. ,MSSQL (on Linux and OSX using SQSH)

Oracle is coming soon.

# Installation

### With Package Control ###

Look for the package named `PhpNamespace`.

### With Git ###

Download the Zip file, extract it to your Sublime Text packages directory, and rename it to SQLExec

Some directories have to be defined in the PATH environment variable, according to the SGBD that you want to use: "mysql" executable for MySQL, "pgsql" executable for PostgreSQL, or "sqlplus" executable for Oracle ( Not tested ), "sqsh" executable for MSSQL (OSX and Linux)

You can also specify full path for these command in settings :

( Preferences > Package Settings > SQLExec > Settings - User )

```json
    "sql_exec.commands": {
        "mysql" : "/usr/bin/mysql"
    },

```

# Sample configuration file
```json
{
    "connections": {
        "Connection 1": {
            "type"    : "mysql",
            "host"    : "127.0.0.1",
            "port"    : 3306,
            "username": "user",
            "password": "password",
            "database": "dbname"
        },
        "Connection 2": {
            "type"    : "mysql2",
            "database": "dbname",
            "loginpath": "loginpath",
        },
        "Connection 3": {
            "type"    : "mssql",
            "host"    : "127.0.0.1",
            "port"    : 1433,
            "username": "user",
            "password": "password",
            "database": "dbname"
        }
        "Connection 4": {
            "type"    : "pgsql",
            "host"    : "psql.server.fr",
            "port"    :  5432,
            "username": "anotheruser",
            "password": "password",
            "database": "dbname"
        }
    }
}
```
# Usage
Default shortcuts are :
- `super+alt+e` : swhitch connection
- `super+e` `super+e` : execute selected query
- `super+e` `super+q` : type a query
- `super+e` `super+s` : show tables records
- `super+e` `super+d` : desc table
