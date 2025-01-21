# Hallange literalura

# Desafío Literalura

Este proyecto, realizado como parte del programa Oracle Next Education (Oracle ONE), es una aplicación de consola en Java que permite interactuar con datos de libros y autores mediante una API externa y una base de datos local.

## Funcionalidades
La aplicación ofrece las siguientes opciones a través de un menú interactivo:
- Buscar libros por título.
- Listar libros y autores registrados.
- Listar autores vivos en un año específico.
- Listar libros por idioma.
- Ver el top 10 de libros más descargados.
- Obtener estadísticas.

## Tecnologías utilizadas
- **Java SE 17**
- **Spring Boot v3.3.0**
- **Maven** para gestión de dependencias.
- **PostgreSQL** para almacenamiento de datos.
- **IntelliJ** como IDE de desarrollo.

## Arquitectura del proyecto
El proyecto sigue la estructura estándar de Maven, organizado en los siguientes paquetes:

### Paquetes principales
1. **models**: Contiene las clases de modelo y mapeo a base de datos.
   - `Libros.java`: Define atributos y relaciones de los libros.
   - `Autores.java`: Define atributos y relaciones de los autores.
   - Clases de apoyo para manejar datos de la API (`Datos`, `DatosLibros`, `DatosAutores`).
2. **repositorio**: Interfaces para la interacción con la base de datos.
   - `IAutoresRepository.java`
   - `ILibrosRepository.java`
3. **service**: Clases de servicio para consumir y convertir datos de la API.
   - `ConsumoApi.java`: Obtiene datos de la API Gutendex.
   - `ConvierteDatos.java`: Convierte datos JSON a objetos de modelo.
4. **principal**: Contiene la clase principal (`Principal.java`), que gestiona la lógica de interacción con el usuario.

### Dependencias clave
- **Jackson Dataformat** y **Jackson Core** para manejo de JSON.
- **Spring Data JPA** para integración con la base de datos.
- **PostgreSQL Driver**.

### Configuración de la base de datos
La conexión a la base de datos se realiza a través del archivo `application.properties`. Deberás configurar los valores de:
- `DB_HOST`: Host de la base de datos (e.g., `localhost`).
- `DB_NAME_LITERALURA`: Nombre de la base de datos.
- `DB_USER` y `DB_PASSWORD`: Credenciales del usuario.

Configurar la base de datos Crea una base de datos en PostgreSQL y configura las credenciales en application.properties.

Compilar y ejecutar Usa Maven para compilar y ejecutar la aplicación:

bash
Copy
Edit
cd desafio-literalura
mvn clean install
mvn spring-boot:run





