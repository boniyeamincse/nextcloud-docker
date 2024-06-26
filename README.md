# nextcloud-docker
# User Guide: Setting up Nextcloud with Docker on CentOS 7

## Prerequisites:
- CentOS 7 installed on your server.
- Docker installed on CentOS 7.
- Basic knowledge of Docker and Docker Compose.

## Steps:

1. **Prepare your CentOS 7 Environment:**
   - Ensure your CentOS 7 system is up-to-date.
   - Install Docker on CentOS 7 by following the official Docker documentation.

2. **Create Project Directory:**
   - Create a directory for your Nextcloud Docker project. For example:
     ```
     mkdir nextcloud-docker
     cd nextcloud-docker
     ```

3. **Create Docker Compose Configuration:**
   - Create a `docker-compose.yml` file in your project directory.
   - Copy and paste the provided Docker Compose configuration into this file.

4. **Create Nextcloud Docker Configuration:**
   - Create a `nextcloud` directory in your project directory.
   - Inside the `nextcloud` directory, create a `Dockerfile` and a `config` directory.
   - Copy the provided Nextcloud Dockerfile into the `Dockerfile`.
   - Inside the `config` directory, create a `config.php` file.
   - Copy the provided Nextcloud configuration PHP file into `config.php`.
   - Modify the `config.php` file to suit your environment, replacing placeholders with actual values.

5. **Create Apache Docker Configuration:**
   - Create an `apache` directory in your project directory.
   - Inside the `apache` directory, create a `Dockerfile` and a `ssl` directory.
   - Copy the provided Apache Dockerfile into the `Dockerfile`.
   - Inside the `ssl` directory, create a placeholder for your SSL certificates.

6. **Create MariaDB Docker Configuration:**
   - Create a `mariadb` directory in your project directory.
   - Inside the `mariadb` directory, create a `Dockerfile`.
   - Copy the provided MariaDB Dockerfile into the `Dockerfile`.

7. **Initialize MariaDB Database:**
   - Inside the `mariadb` directory, create an `init.sql` file.
   - Copy the provided MariaDB initialization SQL commands into this file.

8. **Configure SSL Certificates:**
   - Obtain SSL certificates for your domain using Let's Encrypt.
   - Place the obtained SSL certificates in the `apache/ssl` directory.

9. **Start Docker Services:**
   - Navigate to your project directory containing `docker-compose.yml`.
   - Run the command `docker-compose up -d` to start the Docker services.

10. **Access Nextcloud:**
    - Once the Docker services are running, you can access Nextcloud via your domain name (e.g., `https://nextcloud.akijgroup.co`).
    - You may need to wait a few moments for the SSL certificates to be provisioned and applied.

11. **Initial Setup:**
    - Follow the Nextcloud setup wizard to complete the initial configuration.
    - Provide necessary details such as admin username, password, database credentials, etc.

12. **Enjoy Nextcloud:**
    - Once the setup is complete, you can start using Nextcloud to store, sync, and share your files securely.

Congratulations! You have successfully set up Nextcloud with Docker on CentOS 7. You can now enjoy the features of Nextcloud while leveraging the power of Docker for easy deployment and management.
