# Desafio-46--Proyecto-Final--ECommerce-32240
## Aplicación web de Ecommerce de productos.

Antes de ejecutar el comando, deben detallarse: PORT CONNECTION BCRYPTGENSALT JWTKEY PERSISTENCE MAILPASSWORD LOGGER, en el .env que esta oculto pero deje un archivo.txt con los detalles.

### Informacion del proyecto

El proyecto esta formado con varias APIs: son session, carts, products, tickets y messages, para acceder a cada una de ellas, la URL es /api/nombreApi/metodo

El proyecto puede trabajar tanto con Mongo como con persistencia en archivos, esto se define en el PERSISTENCE del .env y utiliza el patrón Factory para alternar entre estos

La aplicación cuenta con varias secciones, incluyendo un chat para usuarios, un sistema de roles para la creación y modificación de archivos, usuarios con carritos autogenerados para cada usuario, sistema de compras con control y verificación de stock y motor de plantillas con handlebars Los productos pueden ser agregados tanto por administradores como por usuarios premium; estos últimos pueden modificar y eliminar sus productos, pero no pueden añadirlos a sus carritos

### Tests
Para ejecutar los tests del servidor que conforman las rutas principales de las APIs session, products y carts, ejecute npx mocha test/supertest.test.js

### Usuario administrador

El usuario administrador tiene como email adminCoder@coder.com y como contraseña adminCod3r123.

### Rutas de utilidad

La ruta /api/products/mockProducts arroja 100 productos como si fuese una petición a MongoDB, no tiene ninguna modificacion

La ruta /loggerTest arroja un logger de cada tipo

La ruta /apidocs brinda información adicional sobre las rutas de las APIs carts y products

### Detalles

El programa arroja demasiados errores fatales por favicon y lectura de demás archivos

Para que los usuarios puedan pasar a ser premium, es necesario que suban sus documentos

Para que el servidor esté en producción y no muestre los loggers, el LOGGER del archivo .env debe ser "PRODUCTION"
