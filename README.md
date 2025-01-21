# Foro Hub API

**Foro Hub API** es un proyecto de backend que replica el funcionamiento básico de un foro. Este proyecto está desarrollado con **Spring Boot** y permite a los usuarios realizar las siguientes acciones:

1. **Crear un nuevo tópico.**
2. **Mostrar todos los tópicos creados.**
3. **Mostrar un tópico específico.**
4. **Actualizar un tópico.**
5. **Eliminar un tópico.**

---

## 🛠️ Tecnologías utilizadas

- **Java 17**
- **Spring Boot 3.1.5**
- **H2 Database** (base de datos en memoria).
- **Maven** (gestión de dependencias).
- **Postman** (para realizar pruebas).

---

## 🚀 Funcionalidades principales

### Rutas disponibles (CRUD de Tópicos)

| Método | Ruta            | Descripción                           |
|--------|-----------------|---------------------------------------|
| POST   | `/topicos`      | Crear un nuevo tópico.                |
| GET    | `/topicos`      | Listar todos los tópicos.             |
| GET    | `/topicos/{id}` | Obtener un tópico específico por ID.  |
| PUT    | `/topicos/{id}` | Actualizar un tópico existente.       |
| DELETE | `/topicos/{id}` | Eliminar un tópico por su ID.         |

---

## 📂 Cómo ejecutar el proyecto

### **1. Clonar el repositorio**


```bash
git clone https://github.com/tu-usuario/foro-hub-api.git
cd foro-hub-api
2. Configurar la base de datos H2
El proyecto utiliza una base de datos en memoria llamada H2. Esta base de datos no requiere instalación ni configuración adicional.

Puedes acceder a la consola H2 en:
http ://localhost :8080 /h2 -console

Credenciales para conectarse:

Dirección URL JDBC: jdbc:h2:mem:testdb
Usuario: sa
Contraseña: password
3. Ejecutar el proyecto
Asegúrese de tener Java 17 instalado en su computadora.
Asegúrese de tener Maven instalado.
Ejecuta el siguiente comando en la terminal, dentro del directorio del proyecto:
intento

Copiar

Editar
mvn spring-boot:run
Esto iniciará el servidor en http ://localhost :8080 .

4. Probar la API
Usa Postman , Insomnia , o cualquier cliente HTTP para probar las rutas de la API. Aquí tienes ejemplos:

Crear un tema (POST /topicos)
Cuerpo de la solicitud (JSON):
json

Copiar

Editar
{
    "titulo": "Mi primer tópico",
    "mensaje": "Este es el contenido del tópico."
}
Obtener todos los temas (GET /topicos)
No necesitas enviar datos en esta solicitud.

Actualizar un tema (PUT /topicos/{id})
Cuerpo de la solicitud (JSON):
json

Copiar

Editar
{
    "titulo": "Tópico actualizado",
    "mensaje": "Contenido del tópico actualizado."
}
Eliminar un tema (DELETE /topicos/{id})
No necesitas enviar datos en esta solicitud, solo el ID del tema en la URL.

📝 Estructura del proyecto
El proyecto sigue la arquitectura estándar de Spring Boot:

intento

Copiar

Editar
src/main/java/com/alura/foro/
├── config/              # Configuración de seguridad
├── controller/          # Controladores REST
├── exception/           # Manejo de excepciones
├── model/               # Clases de modelo (entidades)
├── repository/          # Acceso a la base de datos (JPA)
├── service/             # Lógica de negocio
└── ForoApplication.java # Punto de entrada del proyecto
📝 Licencia
Este proyecto fue desarrollado como parte de un desafío educativo en Alura Cursos y está diseñado para fines de aprendizaje.
