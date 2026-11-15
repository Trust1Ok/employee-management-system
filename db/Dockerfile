
# Use MySQL 8.0
FROM mysql:8.0

# Set the working directory
WORKDIR /tmp

# Copy SQL scripts and data files
COPY test_db/*.sql /tmp/
COPY test_db/*.dump /tmp/

# Run the employee database setup script
# when the database is first initialised
COPY test_db/employees.sql /docker-entrypoint-initdb.d/

# Set the MySQL root password (lab use only)
ENV MYSQL_ROOT_PASSWORD=example
