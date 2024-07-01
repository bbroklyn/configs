## Step 1: Changing PostgreSQL Configuration Files:

1. Edit `postgresql.conf` to allow connections from any IP address:

   ```bash
   sudo vim /etc/postgresql/*/main/postgresql.conf
   ```

2. Search for listen_addresses using `?` in vim and set it to `'*'`:

   ```bash
   listen_addresses = '*'
   ```

3. Save and close the file using `:wq`

## Step 2: Edit pg_hba.conf to configure access permissions:

1. Edit `pg_hba.conf` to configure access permissions:

   ```bash
   sudo vim /etc/postgresql/*/main/pg_hba.conf
   ```

2. Add the following line at the end to allow connections without a password from any IP address:

   ```bash
   host all all 0.0.0.0/0 md5
   ```

3. Save and close the file using `:wq`

## Step 3: Restart PostgreSQL Service

1. Restart the `PostgreSQL service` to apply the changes:

   ```bash
   sudo service postgresql restart
   ```

   **OR**

   ```bash
   sudo systemctl restart postgresql
   ```
