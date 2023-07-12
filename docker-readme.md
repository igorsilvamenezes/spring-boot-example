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

# Insert data into table
    *In psql client terminal

    #List all databases
        $> \l

    *Connect to Customer database
        $>\c customer

    *Verify that table is empty
        $>SELECT * FROM customer;

    #Insert first record
        $>INSERT INTO customer (id, name, email, age)
        VALUES (nextval('customer_id_sequence'), 'Alex', 'alex@gmail.com', 22);

    #Insert second record
        $>INSERT INTO customer (id, name, email, age)
        VALUES (nextval('customer_id_sequence'), 'Jamila', 'jamila@gmail.com', 33);

    *Verify the inserted records
        $>SELECT * FROM customer;