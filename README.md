# Technical Exercise

## Requisitos

- Docker
- Docker Compose
- JDK 17
- Maven

## Instrucciones para Ejecutar

1. Clona el repositorio:
    ```sh
    git clone https://github.com/Camila-Rodriguez/TechnicalTest.git
    ```
2. Navega al directorio del proyecto:
    ```sh
    cd technicalExercise
    ```
3. Empaqueta la aplicación con Maven:
    ```sh
    mvn clean package
    ```
4. Construye la imagen Docker:
    ```sh
    docker build -t technicalexercise:latest .
    ```
5. Levanta los contenedores con Docker Compose:
    ```sh
    docker-compose up
    ```
6. Accede a la aplicación en `http://localhost:8080`.

## Endpoints de la API

AUTORES

--Crear un autor
POST /api/authors
Body: { "name": "Author Name", "birthdate": "YYYY-MM-DD" }

--Actualizar un autor
PUT /api/authors/{id}
Body: { "name": "Author Name", "birthdate": "YYYY-MM-DD" }

--Eliminar un autor
DELETE /api/authors/{id}

--Consultar un autor
GET /api/authors/{id}


LIBROS


--Crear un libro
POST /api/books
Body: { "title": "Book Title", "author": { "id": 1 } }

--Actualizar un libro
PUT /api/books/{id}
Body: { "title": "Book Title", "author": { "id": 1 } }

--Eliminar un libro
DELETE /api/books/{id}

--Consultar un libro
GET /api/books/{id}
