# PruebaSolati
** Chexter app
Es una aplicación para consultar la información de un producto
** Tecnologiás
-Base de datos: PostgreSQL
-Lenguaje: PHP 7.4
-Patron de diseño: MVC, DAO y Singleton
-front: HTML, javascripts
** Estructura
   *DAO
    --ProductsDAO
    --ProductModel
    --UserDAO
    --UserModel
  *Modeles
    -login
    --Controller
    -product
     -controller
     -views
   *db(Configuracion de la Base de datos)
   *index
   *server(rutas y render de las vistas)
** Crear tablas
CREATE DATABASE chexter;
-- Crear la tabla --
  CREATE TABLE products (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  description TEXT,
  price NUMERIC(10, 2) NOT NULL,
  quantity INT NOT NULL,
  created_at TIMESTAMPTZ DEFAULT CURRENT_TIMESTAMP
);
 CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  username VARCHAR(50) NOT NULL,
  description VARCHAR(250) NOT NULL
);
** Endpoints 
1. Login: http://localhost/chexter/login POST
   Ejemplo:
   {
    "username":"prueba",
    "password":"prueba123"
   }
2. Product: http://localhost/chexter/getProducts GET
 
