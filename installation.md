Once you've installed PostgreSQL on Ubuntu using `apt install postgresql`, you can access it from the command line (CLI) as follows:

### 1️⃣ **Switch to the PostgreSQL User**
PostgreSQL creates a default system user named `postgres`. To use the PostgreSQL CLI tools, you need to switch to this user:

```bash
sudo -i -u postgres
```

### 2️⃣ **Access PostgreSQL Shell (`psql`)**
Once you're switched to the `postgres` user, you can enter the PostgreSQL interactive shell (`psql`) by running:

```bash
psql
```

This should log you into the PostgreSQL shell, showing something like:

```
postgres=#
```

### 3️⃣ **Connect to a Specific Database**
By default, `psql` connects to a database named `postgres`. If you want to connect to a different database, use:

```bash
psql -d your_database_name
```

### 4️⃣ **Exit `psql`**
To exit the PostgreSQL shell, type:

```sql
\q
```

### 5️⃣ **Running SQL Commands**
You can run SQL commands inside `psql`, such as:

```sql
SELECT version();
```

To list all databases:

```sql
\l
```

To list all tables in the current database:

```sql
\dt
```

To switch databases:

```sql
\c database_name
```

---

### 🚀 **Bonus: Enable Direct Access Without Switching Users**
If you want to run `psql` directly from your normal user:

1. Install the `postgresql-client` if not already installed:

   ```bash
   sudo apt install postgresql-client
   ```

2. Use `psql` with your username:

   ```bash
   psql -U postgres
   ```

   If you get an authentication error, try:

   ```bash
   psql -U postgres -h localhost
   ```

3. If you want to avoid typing `-U postgres` each time, create a PostgreSQL user matching your Ubuntu username and grant it access:

   ```bash
   sudo -i -u postgres
   createuser --interactive
   ```

   Follow the prompts to create a user with the same name as your Ubuntu user.

Now, you can run `psql` directly without switching users.

