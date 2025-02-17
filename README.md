# Hito 2 - Desarrollo Frontend 💻 🌻 🌴

El segundo hito consiste en el desarrollo de la aplicación cliente con React.
Se crea proyecto _"Muya, Agricultura Urbana"_ en base a las definiciones del
"Hito 1 - Diseño y Prototipo".

## Integrantes

- Ángela Águila
- Bárbara Estrada
- Cristián Vega

## Repositorio

https://github.com/bestrada05/Muya

## Requerimientos

### 1. Crear un nuevo proyecto usando npm e instalar las dependencias.

Las dependencias utilizadas son:

- react: crear interfaces de usuario.
- react vite: compilar, estructura del proyecto.
- react-dom: renderizar los componentes.
- react-router-dom: enrutamiento dinámico.
- lucide-react: íconos
- sonner: notificaciones

### 2. Utilizar React Router para la navegación entre rutas.

Se utiliza react-router-dom para la navegación entre rutas.

### 3. Reutilizar componentes haciendo uso del paso de props y renderización dinámica.

Se reutiliza los componentes mediante el uso de props y la renderización dinámica (react-dom).

### 4. Hacer uso de los hooks para un desarrollo ágil y reactivo.

Los hooks aplicados son: useContext, useState, useEffect.

### 5. Utilizar Context para el manejo del estado global.

UseContext usado en el carro de compras

---

## Integración Frontend - Backend

1)Autenticación (AuthContext)

Creamos un contexto de autenticación que maneja:

Inicio de sesión
Registro de usuarios
Cierre de sesión
Manejo del estado de autenticación

Funcionalidades principales:

Almacena información del usuario en localStorage
Guarda token, email e ID de usuario
Verifica si el usuario está autenticado
Permite login y registro con manejo de errores

2. Login

Modificamos el componente Login para:

Usar el contexto de autenticación
Validar credenciales
Redirigir después del inicio de sesión
Manejar estados de carga y errores

Cambios clave:

Eliminamos fetch manual
Usamos método login del AuthContext
Agregamos manejo de estados (loading, error)
Redirigimos después de un login exitoso

3. Register

Actualizamos el componente Register para:

Integrar con AuthContext
Añadir rol_id por defecto
Manejar registro de usuarios
Validar contraseñas
Manejar estados de carga y errores

Modificaciones:

Añadimos rol_id: 2 por defecto
Usamos método register del AuthContext
Implementamos validaciones de formulario

4. NavBar

Modificamos la navegación para mostrar:

"Ingresa" cuando no hay sesión
"Cerrar Sesión" cuando hay usuario autenticado
Botón de cierre de sesión que redirige al inicio

5. Carrito (CartContext)

Implementamos un contexto de carrito con:

Gestión de items en el carrito
Persistencia en localStorage
Métodos para agregar, actualizar y eliminar productos
Método de checkout integrado con backend

6. Carrito (Componente Cart)

Actualizamos el carrito para:

Requerir autenticación para realizar compra
Enviar pedido al backend con token de autorización
Manejar errores de procesamiento
Limpiar carrito después de compra exitosa

7. Integración General

Configuramos rutas para proteger acceso
Añadimos validación de autenticación en componentes sensibles
Implementamos flujo completo de usuario:

Registro
Login
Compra
Logout

8. Mejoras de Experiencia de Usuario

Manejo de estados de carga
Mensajes de error descriptivos
Redirecciones automáticas
Deshabilitación de controles durante procesos

Consideraciones de Seguridad

Uso de tokens Bearer
Validación de autenticación en frontend y backend
Protección de rutas sensibles

Esta implementación proporciona un sistema de autenticación y compra completo, con manejo de estados, errores y una experiencia de usuario fluida.
