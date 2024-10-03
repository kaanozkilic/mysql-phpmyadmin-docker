# mysql-phpmyadmin-docker
A MySQL development environment with Docker and phpMyAdmin for learning MySQL 

# Setting Up a Codespace in GitHub

1. Navigate to your repository on GitHub.
2. Click the **Code** button and select **Create codespace on main**.
3. Wait a few moments for your codespace environment to be set up.

Once the setup is complete, you can perform all your tasks directly within the browser-based codespace.

## Troubleshooting:
If you encounter the error message **Workspace does not exist**, follow these steps:

1. Click **Open Workspace**.
2. Choose the path: `/workspaces/mysql-phpmyadmin-docker/workspace/`.

This should resolve the issue and allow you to continue working in your codespace.


## Connecting to MySQL Database

After the codespace starts, you can log in to the MySQL database server using the following command:

```bash
mysql -u <username> -p
```

> Replace <username> with your MySQL username. Enter your password when prompted. Once logged in, you can execute SQL queries, such as creating databases, tables, and more.

![Example connection](https://raw.githubusercontent.com/dipaish/dipaish/refs/heads/main/images/courseRelatedImages/dataBase.png)

## Using phpMyAdmin
1. Open the **Ports** view in your codespace.
2. Click **Add Port** and enter **88** as the port number.
3. Once the port is added, a forwarded address for port 88 will appear. Click on the forwarded address to open phpMyAdmin.
5. Use your MySQL credentials to log in and start working with your databases.

***Additionally, you will need to open port 6033 using the same steps as above to ensure full connectivity.***

![Example Ports](https://raw.githubusercontent.com/dipaish/dipaish/refs/heads/main/images/courseRelatedImages/ports.png)