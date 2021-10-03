# de Bugger backend
### Web site
  All you need is 
  ![](https://imgur.com/ro2N4hy) 
  
  [de Bugger](https://debugger.vercel.app/) 
  
### before deployment 
* \*\*note:\*\* 
  bellows are fake info, you should modify/edit it.
  1. in `env/postgres.env`
  ```bash=
  POSTGRES_USER=postgres
  POSTGRES_PASSWORD=fakepassword
  ```
  you should change `POSTGRES_PASSWORD` to your own content.
  2. in `docker-compose.yaml`
  ```bash=
    pgadmin:
        container_name: pgadmin
        image: dpage/pgadmin4
        environment:
          - PGADMIN_DEFAULT_EMAIL=fakeuser@fake.url
          - PGADMIN_DEFAULT_PASSWORD=fakepassword
  ```
  you should change `PGADMIN_DEFAULT_PASSWORD` to your own content.
  
### deployment
1. `docker build -t api .`
2. `docker-compose -f docker-compose.yaml up`
3. now you can loging pgadmin 
  1. login pgadmin
  2. create connection
  3. `CREATE DATABASE biodb`
  4. copy and peast `db/init.sql` to initiate your database 

