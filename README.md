# WordPress Blog (Powered by Docker Compose :) )

This project demonstrates how to deploy a complete, functional WordPress website using Docker Compose. It sets up a multi-container application stack consisting of a web application (WordPress) and a database (MySQL), perfect for local development or a quick cloud deployment.

## Getting Started

Follow these steps to get your WordPress site up and running in minutes!

### Prerequisites

Before you begin, ensure you have the following installed on your system:

* [**Docker Desktop**](https://www.docker.com/products/docker-desktop) (which includes Docker Engine and Docker Compose)

### Setup Instructions

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Ade1damola/wordpress-docker-app.git

    cd wordpress-docker-app
    ```
 

2.  **Create Your Environment File:**
    Copy the example environment file and fill in your actual credentials.
    ```bash
    cp .env.example .env
    ```
    **Now, open the newly created `.env` file and replace the placeholder values with strong, unique passwords for `MYSQL_ROOT_PASSWORD` and `MYSQL_PASSWORD`.**

    The `.env` file contains sensitive information and is ignored by Git, so it will NOT be committed to your public repository.

### Running the Application

Once you've set up your `.env` file, you can start the entire application stack with a single command:

```bash
docker compose up -d
```

### Accessing Your WordPress Site
After the containers have started (this might take a minute or two for the database and WordPress to fully initialize), open your web browser and navigate to:

[http://localhost:8080](http://localhost:8080)

You should see the famous WordPress setup screen! Follow the on-screen instructions to complete your WordPress installation.


### Stopping the Application
When you're done working on your blog and want to stop the services, run:

```bash
docker compose down
```

### Cleaning Up
If you want to remove the named volume (deleting all your database data, including blog posts), you can use:

```bash
docker compose down -v
```