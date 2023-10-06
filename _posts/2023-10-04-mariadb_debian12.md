---
title: "mariadb_debian12"
layout: post
subtitle: Install Mysql Server debian 12
author: m4rv4x
categories: bash
banner:
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: bash mysql
top: 1
sidebar: []
---
To connect to MariaDB on Debian 12 and create a table, you can follow these steps:

1. Install MariaDB:
   ```
   sudo apt update
   sudo apt install mariadb-server
   ```

2. Start the MariaDB service:
   ```
   sudo systemctl start mariadb
   ```

3. Secure the MariaDB installation:
   ```
   sudo mysql_secure_installation
   ```

   This command will prompt you to set a root password and perform other security-related configurations.

4. Connect to the MariaDB server:
   ```
   sudo mysql -u root -p
   ```

   Enter the root password you set during the secure installation.

5. Create a new database:
   ```
   CREATE DATABASE your_database_name;
   ```

   Replace `your_database_name` with the desired name for your database.

6. Use the newly created database:
   ```
   USE your_database_name;
   ```

7. Create a table:
   ```
   CREATE TABLE your_table_name (
       column1 datatype constraint,
       column2 datatype constraint,
       ...
   );
   ```

   Replace `your_table_name` with the desired name for your table. Specify the columns and their datatypes as needed.

8. Insert data into the table:
   ```
   INSERT INTO your_table_name (column1, column2, ...)
   VALUES (value1, value2, ...);
   ```

   Replace `your_table_name` with the name of your table. Specify the values to be inserted into the respective columns.

That's it! You have now connected to MariaDB on Debian 12 and created a table.
