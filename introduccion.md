Introducción
¿Qué es la Programación Orientada a Objetos (POO)?
La Programación Orientada a Objetos (POO) es un paradigma de programación basado en la organización del código en objetos, que representan entidades del mundo real.
Es importante porque permite crear software modular, reutilizable y fácil de mantener.

Cuatro fundamentos de POO
Abstracción
Es la capacidad de representar elementos del mundo real en el código.
Ejemplo: Un "Auto" puede representarse con atributos (marca, modelo) y métodos (arrancar, frenar).

Encapsulamiento
Protege los datos de un objeto, permitiendo acceso solo a través de métodos específicos.
Ejemplo: Un "Cajero Automático" no permite acceso directo al dinero, solo mediante transacciones.

Herencia
Permite que una clase reutilice características de otra.
Ejemplo: Un "Auto Deportivo" hereda de la clase "Auto", pero añade características como mayor velocidad.

Polimorfismo
Permite que una misma acción tenga diferentes comportamientos según el objeto.
Ejemplo: Un "Animal" puede hacer un sonido, pero cada tipo de animal emite un sonido diferente (perro: ladrido, gato: maullido).

Requisitos iniciales del sistema
Registro de usuarios: El sistema debe permitir la creación y gestión de usuarios.
Gestión de turnos: Los usuarios deben poder solicitar, cancelar y reprogramar turnos.
Notificaciones: El sistema debe enviar recordatorios de turnos vía correo o mensaje.
Historial de turnos: Se debe permitir consultar turnos pasados.
Control de acceso: Solo usuarios registrados pueden acceder a ciertas funciones.

Caso de Uso 1: Iniciar Sesión

Actor(es) involucrado(s): Usuario registrado

Descripción breve: Permite al usuario autenticarse en el sistema mediante sus credenciales.

Flujo principal de eventos:
El usuario ingresa su nombre de usuario y contraseña.

El sistema valida las credenciales.

Si son correctas, el sistema concede acceso al usuario.

Se redirige al usuario a la página de inicio.

Precondiciones:
El usuario debe estar registrado en el sistema.

Postcondiciones:
El usuario ha iniciado sesión y tiene acceso a las funcionalidades del sistema.

Caso de Uso 2: Registrar Usuario

Actor(es) involucrado(s): Usuario nuevo

Descripción breve: Permite a un nuevo usuario registrarse en el sistema.

Flujo principal de eventos:
El usuario ingresa su información (nombre, correo, contraseña).

El sistema valida los datos.

El sistema almacena la información y envía un correo de confirmación.

El usuario confirma el registro a través del correo.

Precondiciones:
El usuario no debe estar registrado previamente.

Postcondiciones:
El usuario queda registrado y puede iniciar sesión en el sistema.

Caso de Uso 3: Realizar Compra

Actor(es) involucrado(s): Cliente

Descripción breve: Permite al cliente comprar productos en la tienda en línea.

Flujo principal de eventos:
El cliente selecciona productos y los agrega al carrito.

El cliente procede al pago.

El sistema solicita los datos de pago y dirección de envío.

Se valida el pago y se confirma la compra.

El sistema genera un número de pedido y envía confirmación al cliente.

Precondiciones:
El cliente debe tener productos en el carrito.

El sistema debe estar disponible.

Postcondiciones:
Se registra el pedido y se inicia el proceso de envío.

Caso de Uso 4: Generar Reporte de Ventas

Actor(es) involucrado(s): Administrador

Descripción breve: Permite al administrador obtener un informe de ventas en un período determinado.

Flujo principal de eventos:
El administrador accede a la sección de reportes.

Ingresa el rango de fechas para el reporte.

El sistema recopila y procesa la información de ventas.

Se genera un documento con el reporte solicitado.

Precondiciones:
El usuario debe ser un administrador autorizado.

Debe haber ventas registradas en el período consultado.

Postcondiciones:
Se genera y se muestra el reporte solicitado.

Caso de Uso 5: Recuperar Contraseña

Actor(es) involucrado(s): Usuario registrado

Descripción breve: Permite a un usuario recuperar su contraseña en caso de olvido.

Flujo principal de eventos:

El usuario solicita la recuperación de contraseña.

El sistema solicita el correo electrónico del usuario.

Se envía un enlace de recuperación al correo proporcionado.

El usuario accede al enlace y establece una nueva contraseña.

Precondiciones:

El usuario debe estar registrado en el sistema.

Postcondiciones:

La contraseña se actualiza y el usuario puede iniciar sesión nuevamente.

BOCETO INICIAL DEL DISEÑO DE CLASES

![Captura de pantalla 2025-03-30 215756](https://github.com/user-attachments/assets/5948340a-80d8-4642-a307-5bd1b3fde944)


