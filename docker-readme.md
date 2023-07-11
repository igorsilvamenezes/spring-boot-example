# Create docker container

    *Create Docker container Postgres by docker compose file
        $> docker compose up -d

    *List all docker containers
        $> docker compose ps

# Create Database

    *List all docker containers
        $> docker ps

    *Execute shell commands within the container
        $> docker exec -it postgres bash

    #Execute psql client for connecting to postgres database
        $> psql -U menezes

    #List all databases
        $> \l

    #Create the new database
        $> CREATE DATABASE customer;

# Show Table
    *Execute shell commands within the container
        $> docker exec -it postgres bash

    #Execute psql client for connecting to postgres database
        $> psql -U menezes

    #List all databases
        $> \l

    *Connect to Customer database
        $>\c customer

    *List of table relations
        $>\dt

    *List of all relations
        $>\d

    *List all data of the table
        $>select * from customer;