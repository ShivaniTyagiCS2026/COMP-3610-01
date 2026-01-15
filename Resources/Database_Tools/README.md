# Database Tools & Configuration

## Tools Included in GitHub Codespaces

### PostgreSQL
- **Version:** Latest (configured in devcontainer)
- **Default User:** postgres
- **Default Password:** postgres
- **Port:** 5432
- **Initial Database:** postgres

### VS Code Extensions
1. **PostgreSQL Client** (cweijan.vscode-postgresql-client2)
   - Browse database objects
   - Execute queries
   - Manage connections

2. **SQLTools** (mtxr.sqltools)
   - Query builder
   - Connection management
   - Syntax highlighting

3. **SQLTools PostgreSQL Driver** (mtxr.sqltools-driver-pg)
   - PostgreSQL-specific support
   - Advanced features

### Command Line Tools
- `psql` - PostgreSQL command-line interface
- `createdb` - Create new databases
- `dropdb` - Delete databases
- `pg_dump` - Backup databases
- `pg_restore` - Restore databases

## Connection Configuration

### Using PostgreSQL Client Extension
1. Click the PostgreSQL icon in VS Code sidebar
2. Create new connection with:
   - **Host:** localhost
   - **Port:** 5432
   - **Database:** postgres
   - **Username:** postgres
   - **Password:** postgres

### Using psql Command Line
```bash
psql -U postgres -h localhost -d postgres
```

### Connection String
```
postgresql://postgres:postgres@localhost:5432/postgres
```

## Common Tasks

### Creating a Database
```sql
CREATE DATABASE course_db;
```

### Creating a Table
```sql
CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE
);
```

### Backing Up a Database
```bash
pg_dump -U postgres course_db > backup.sql
```

### Restoring a Database
```bash
psql -U postgres course_db < backup.sql
```

## Additional Resources
- PostgreSQL documentation available in VS Code Help
- SQL tutorials within each week's lecture materials
- Practice exercises in worksheet directories

---

*For questions about specific tools or configurations, see the course discussion forum.*
