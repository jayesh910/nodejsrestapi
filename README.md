# Node.js Rest APIs with Express & MySQL example

For more detail, please visit:
> [Build Node.js Rest APIs with Express & MySQL](https://bezkoder.com/node-js-rest-api-express-mysql/)

> [Deploying/Hosting Node.js app on Heroku with MySQL database](https://bezkoder.com/deploy-node-js-app-heroku-cleardb-mysql/)

## Project setup
```
npm install
```

### Run
```
node server.js
```

MAKE SURE TO RUN THESE STEPS for dockerizing app:
docker network create app_network

docker run -d -it --network app_network -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=testdb --name mysqlname mysql

CREATE TABLE IF NOT EXISTS `customers` (id int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT, email varchar(255) NOT NULL, name varchar(255) NOT NULL,active BOOLEAN DEFAULT false) ENGINE=InnoDB DEFAULT CHARSET=utf8;
INSERT INTO customers(id, email, name, active) VALUES (25, "nehakum@cybage.com" , "Neha" , 1);

docker run -d -it -p 3000:3000 --network app_network --name nodejsapp __

ALTER USER 'root' IDENTIFIED WITH mysql_native_password BY 'root';
