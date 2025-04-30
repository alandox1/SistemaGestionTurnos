# Escenarios de Casos de Uso

## Caso de uso 1 - Registrar nuevo paciente

### Descripcion general
Este caso de uso describe el proceso mediante el cual un nuevo individuo es incorporado al sistema como paciente. El objetivo principal es permitir que una persona cree una cuenta en el sistema, proporcionando la información personal y de contacto.

## Flujo de eventos
### Pasos Desempeñados(ruta principal)

1.El usuario accede a la opcion "Crear Cuenta" 

 * El usuario, a través de la interfaz del sistema, localiza y selecciona la opción

2.Ingresa sus datos personales y de contacto

 * Completa un formulario con nombre, DNI, correo, dirección, teléfono, etc.

3.El sistema valida los datos

 * Una vez que el usuario envía el formulario, el sistema realiza una serie de comprobaciones automáticas

4.El sistema comprueba que no exista un usuario con el mismo correo o dni

 * Después de la validación inicial de los datos, el sistema realiza una consulta a la base de datos de pacientes existente.

5.El sistema registra al nuevo paciente

 * Si todas las validaciones son exitosas, el sistema procede a crear una nueva entrada en la base de datos de pacientes.

### Condiciones

* **Precondiciones:** No debe existir una cuenta previo con el mismo correo/DNI
* **Poscondiciones:** Usuario registrado y habilitado para iniciar sesion
* **Suposiciones:** El formulario esta correctamente validado.

[Enlace del Escenario](https://drive.google.com/file/d/1WayhlAgg-4emzrAt6pgjwnbDxd40ZHv4/view?usp=sharing)

## Escenario 1:Registrar Paciente - Registro exitoso de nuevo paciente

Nombre del escenario: Registrar Paciente - Registro exitoso de nuevo paciente

Descripción: El recepcionista registra a un nuevo paciente sin errores.

### Pasos desempeñado
1.El usuario accede a la opción "Crear cuenta".
 * El usuario entra al sistema y accede a la opcion "Crear cuenta"

2.El usuario ingresa sus datos personales y de contacto.
 * Completa un formulario con nombre, DNI, correo, dirección, teléfono, etc.

3.El sistema valida los datos.
* El sistema revisa que los campos estén completos y con formato correcto.
  
4.El sistema comprueba que no exista un usuario con el mismo correo o DNI.
* El sistema revisa que los campos estén completos y con formato correcto.

5.El sistema registra al nuevo paciente.
* El sistema registra al paciente y guarda sus datos

6.El sistema muestra un mensaje de confirmación de registro exitoso.
* El sistema informa al paciente que se confirmo su registro

7.El usuario puede iniciar sesión con las credenciales registradas.
* El usuario es capaz de iniciar sesion

### Condiciones

* Precondiciones: El usuario no tiene una cuenta registrada con el mismo correo o DNI.

* Postcondiciones: El paciente está registrado en el sistema y puede iniciar sesión.

* Suposiciones: Todos los campos del formulario son válidos y cumplen con los requisitos.

Prioridad: Alta

Riesgo: Bajo.

## Escenario 2:Registrar Paciente - Error en validación de datos del paciente
Nombre del escenario: Registrar Paciente - Error en validación de datos del paciente

Descripción: El recepcionista intenta registrar a un paciente con datos inválidos.

### Pasos desempeñados
1.El usuario accede a la opción "Crear cuenta".
* El usuario accede al sistema y oprime la opcion "crear cuenta"

2.El usuario ingresa datos inválidos (por ejemplo, formato de correo incorrecto).
* El usuario ingresa datos invalidos

3.El sistema muestra un mensaje de error indicando qué datos son inválidos.
* El sistema informa un error en los datos del usuario
  
4.El usuario corrige los datos y vuelve a intentar el registro.
* El usuario corrige los datos puestos y reintenta el registro

### Condiciones

* Precondiciones: El usuario está intentando registrar una cuenta nueva.

* Postcondiciones: El usuario recibe un mensaje de error y no se registra la cuenta.

* Suposiciones: Al menos uno de los campos del formulario es inválido.

Prioridad: Media.

Riesgo: Medio.

## Escenario 3:Registrar Paciente - Registro de paciente con DNI ya existente
Nombre del escenario: Registrar Paciente - Registro de paciente con DNI ya existente

Descripción: El recepcionista intenta registrar a un paciente con un DNI que ya está en el sistema.

### Pasos desempeñados
1.El usuario accede a la opción "Crear cuenta".
* El usuario accede al sistema y oprime la opcion "crear cuenta"
  
2.El usuario ingresa un DNI que ya está registrado en el sistema.
* El usuario ingresa un Dni

3.El sistema muestra un mensaje de error indicando que el DNI ya está registrado.
* El sistema informa un error con el dato dato,indicando que ya esta registrado

4.El usuario puede buscar al paciente existente o corregir el DNI.
* El usuario podria buscar a la sesion existente o corregir el dato.

### Condiciones

Precondiciones: El usuario está intentando registrar una cuenta nueva con un DNI que ya está registrado.

Postcondiciones: El usuario recibe un mensaje de error y no se registra la cuenta.

Suposiciones: El DNI ingresado ya está asociado a una cuenta existente.

Prioridad: Alta.

Riesgo: Alto.


* [Enlace del Escenario](https://drive.google.com/file/d/1Qq64--rHLb-W6_p2i3J7p43ZAuGBfYon/view?usp=sharing)

## Caso de uso 2 - Iniciar sesion
### Descripcion General:
Permite a los usuarios del sistema (pacientes, médicos o administradores) acceder a su cuenta mediante un proceso de autenticación. El usuario debe ingresar su nombre de usuario y contraseña válidos para ingresar a su panel correspondiente. Este caso de uso es esencial para asegurar que solo usuarios autorizados accedan a las funcionalidades del sistema.

## Pasos desempeñados(Ruta Principal)
1.El usuario accede a la opción "Iniciar Sesión".

 * El usuario accede al sistema y accede a la opcion iniciar sesion

2.El usuario ingresa sus credenciales (correo y contraseña).

 * El usuario ingresa sus datos

3.El sistema valida las credenciales.

 * El sistema compara los datos ingresados con los registrados.

4.El sistema verifica si la cuenta está activa.

 * El sistema redirige al usuario al menu dependiendo su rol

5.El sistema otorga acceso al usuario.

 * El sistema otro acceso al usuario a la pagina

### Condiciones

* Precondiciones: El usuario debe tener una cuenta registrada y activa en el sistema.
* Poscondiciones: El usuario ha iniciado sesión y tiene acceso a las funcionalidades del sistema.
* Suposiciones: Las credenciales ingresadas son correctas y la cuenta está activa.

Prioridad:Alto

Riesgo:Medio

## Escenario 1:Iniciar Sesión - Inicio de sesión exitoso
Nombre del escenario: Iniciar Sesión - Inicio de sesión exitoso

Descripción: El usuario ingresa sus credenciales correctamente y accede al sistema.

### Pasos desempeñados

1.El usuario accede a la opción "Iniciar Sesión".
* El usuario navega hasta la página de inicio de sesión del sistema.

2.El usuario ingresa sus credenciales (correo y contraseña).
* El usuario debe ingresar su dirección de correo electrónico y contraseña en los campos correspondientes.

3.El sistema valida las credenciales.
* El sistema verifica que el correo y la contraseña ingresados coincidan con los almacenados en la base de datos.

4.El sistema verifica si la cuenta está activa.
* El sistema comprueba el estado de la cuenta para asegurarse de que no esté desactivada o bloqueada.

5.El sistema otorga acceso al usuario.
* Si las credenciales son válidas y la cuenta está activa, el sistema permite el acceso al usuario.

6.El sistema redirige al usuario a la página principal.
* El usuario es llevado a la página principal del sistema, donde puede acceder a todas las funcionalidades disponibles.

### Condiciones

* Precondiciones: El usuario tiene una cuenta registrada y activa en el sistema.

* Postcondiciones: El usuario ha iniciado sesión y tiene acceso a las funcionalidades del sistema.

* Suposiciones: Las credenciales ingresadas son correctas y la cuenta está activa.

Prioridad: Alta

Riesgo:Bajo

## Escenario 2:Iniciar Sesión - Error en validación de credenciales
Nombre del escenario: Iniciar Sesión - Error en validación de credenciales

Descripción: El usuario ingresa credenciales incorrectas y no puede acceder al sistema.

### Pasos desempeñados
1.El usuario accede a la opción "Iniciar Sesión".

* El usuario navega hasta la página de inicio de sesión del sistema.
 
2.El usuario ingresa credenciales incorrectas.

* El usuario ingresa un correo y/o contraseña que no coinciden con los registros almacenados.

3.El sistema muestra un mensaje de error indicando que las credenciales son incorrectas.

* El sistema detecta que las credenciales no coinciden y notifica al usuario del error.

4.El usuario puede intentar nuevamente ingresar sus credenciales.

* El usuario tiene la opción de corregir sus datos y volver a intentar el inicio de sesión.

### Condiciones

* Precondiciones: El usuario intenta iniciar sesión con credenciales incorrectas.

* Postcondiciones: El usuario recibe un mensaje de error y no se otorga acceso al sistema.

* Suposiciones: Al menos una de las credenciales ingresadas es incorrecta.

Prioridad:Media

Riesgo:Medio

## Escenario 3:  Iniciar Sesión - Cuenta inactiva

Nombre del escenario: Iniciar Sesión - Cuenta inactiva

Descripción: El usuario intenta iniciar sesión con una cuenta que está inactiva.

### Pasos desempeñados
El usuario accede a la opción "Iniciar Sesión".
 * Información del paso: El usuario navega hasta la página de inicio de sesión del sistema.

1.El usuario ingresa sus credenciales (correo y contraseña).
 * El usuario ingresa su dirección de correo electrónico y contraseña en los campos correspondientes.

2.El sistema valida las credenciales.

 * El sistema verifica que el correo y la contraseña ingresados coincidan con los almacenados en la base de datos.

3.El sistema verifica que la cuenta está inactiva.

 * El sistema comprueba el estado de la cuenta y detecta que está inactiva.

4.El sistema muestra un mensaje indicando que la cuenta está inactiva.

 * El sistema notifica al usuario que su cuenta está inactiva y no puede acceder al sistema.

5.El usuario puede intentar reactivar su cuenta o contactar al soporte.

 * El usuario tiene la opción de seguir las instrucciones para reactivar su cuenta o contactar al soporte técnico.

### Condiciones

* Precondiciones: El usuario tiene una cuenta registrada pero inactiva en el sistema.

* Postcondiciones: El usuario recibe un mensaje indicando que la cuenta está inactiva y no se otorga acceso al sistema.

* Suposiciones: La cuenta del usuario está marcada como inactiva en el sistema.

Prioridad: Alta.

Riesgo: Alto.


* [Enlace del Escenario](https://drive.google.com/file/d/1grTwZ1yFfQ_mwM2GZ8DCtCSmkONccC5Y/view?usp=sharing)

## Caso de uso 3 - Solicitar Turno Medico

### Descripcion General:
Permite a los pacientes registrados en el sistema seleccionar una especialidad médica, un profesional de salud y un horario disponible para agendar un turno. El proceso es completamente en línea, y la asignación del turno es inmediata si existe disponibilidad. Esta funcionalidad busca facilitar el acceso a consultas médicas sin necesidad de asistencia presencial o llamadas telefónicas.
## Pasos desempeñados(Ruta Principal)
1.El paciente inicia sesion

 * El paciente accede al sistema e ingresa su usuario y contraseña.

2.Selecciona "Solicitar Turno"

 * Desde el menú principal, selecciona la opción correspondiente.

3.Elige la especialidad del medico requerido

 * El sistema despliega un listado actualizado de especialidades médicas disponibles.

4.Selecciona Medico

 * El sistema filtra y muestra los profesionales que atienden esa especialidad.

5.Selecciona fecha y horario

 * El paciente elige cuándo desea ser atendido.

6.El sistema confirma y registra el turno

 * Si todo es correcto, el sistema guarda el turno y lo asigna al paciente.
### Condiciones
* Precondiciones: Usuario registrado e identificado,Agenda del medico disponible
* Poscondiciones: Turno asignado y confirmado
* Suposiciones: El sistema tiene conexion estable con la base de datos de turno


## Escenario 1 : Solicitar Turno Médico - Solicitud de turno exitoso

Nombre del escenario: Solicitar Turno Médico - Solicitud de turno exitoso

Descripción: El paciente solicita un turno médico y recibe la confirmación.

### Pasos desempeñados

1.El paciente accede a la plataforma de turnos médicos.
 * El paciente puede acceder a la plataforma a través de una computadora o teléfono móvil 

2.El paciente selecciona la opción "Solicitar Turno Médico".
 * El paciente debe seleccionar la opción correspondiente para solicitar un turno.

3.El paciente ingresa sus datos personales.
 * El paciente debe ingresar datos como nombre, apellido, fecha de nacimiento, y DNI.

4.El paciente selecciona el tipo de consulta (médico de cabecera, especialista, etc.).
 *  El paciente debe elegir el tipo de consulta que desea realizar.

5.El paciente selecciona la fecha y hora preferida para la consulta.
* El paciente debe elegir una fecha y hora disponible para la consulta.

6.El sistema verifica la disponibilidad del turno seleccionado.
 * El sistema verifica si el turno seleccionado está disponible.

7.El sistema confirma la solicitud de turno.
 * Si el turno está disponible, el sistema confirma la solicitud.

8.El sistema envía una notificación de confirmación al paciente.
 * El sistema envía una notificación por correo electrónico o SMS confirmando el turno.

9.El paciente puede imprimir o guardar la confirmación del turno.
 * El paciente tiene la opción de imprimir o guardar la confirmación del turno.

### Condiciones
* Precondiciones: El paciente tiene acceso a internet y está registrado en el sistema.

* Postcondiciones: El turno médico ha sido reservado y confirmado para el paciente.

* Suposiciones: El paciente ingresa datos válidos y elige una fecha y hora disponibles.

Prioridad:Alta

Riego:bajo

## Escenario 2:Solicitar Turno Médico - Error en la disponibilidad del turno

Nombre del escenario: Solicitar Turno Médico - Error en la disponibilidad del turno

Descripción: El paciente intenta solicitar un turno médico, pero el turno seleccionado no está disponible.

### Pasos desempeñados
1.El paciente accede a la plataforma de turnos médicos.
 *El paciente puede acceder a la plataforma a través de una computadora o telefono.

2.El paciente selecciona la opción "Solicitar Turno Médico".
 *El paciente debe seleccionar la opción correspondiente para solicitar un turno.

3.El paciente ingresa sus datos personales.
 * El paciente debe ingresar datos como nombre, apellido, fecha de nacimiento, y DNI.

4.El paciente selecciona el tipo de consulta (médico de cabecera, especialista, etc.).
 * El paciente debe elegir el tipo de consulta que desea realizar.

5.El paciente selecciona la fecha y hora preferida para la consulta.
 * El paciente debe elegir una fecha y hora disponible para la consulta.

6.El sistema verifica la disponibilidad del turno seleccionado.
 * El sistema verifica si el turno seleccionado está disponible.

7.El sistema muestra un mensaje de error indicando que el turno no está disponible.
 * El sistema detecta que el turno no está disponible y notifica al paciente del error

8.El paciente puede seleccionar otra fecha y hora disponible.
 *  El paciente tiene la opción de seleccionar otra fecha y hora disponible.

### Condiciones

* Precondiciones: El paciente tiene acceso a internet y está registrado en el sistema.

* Postcondiciones: El paciente recibe un mensaje de error y no se reserva el turno.

* Suposiciones: El turno seleccionado no está disponible.

Prioridad:Media

Riesgo:Medio

## Escenario 3:Solicitar Turno Médico - Datos personales inválidos
Nombre del escenario: Solicitar Turno Médico - Datos personales inválidos

Descripción: El paciente intenta solicitar un turno médico con datos personales inválidos.

### Pasos desempeñados
1.El paciente accede a la plataforma de turnos médicos.
 * El paciente puede acceder a la plataforma a través de una computadora o teléfono.

2.El paciente selecciona la opción "Solicitar Turno Médico".
 * El paciente debe seleccionar la opción correspondiente para solicitar un turno.

3.El paciente ingresa datos personales inválidos.
 * El paciente omite algún campo obligatorio o ingresa datos incorrectos.

4.El sistema muestra un mensaje de error indicando qué datos son inválidos.
 * El sistema detecta los datos inválidos y notifica al paciente del error.

5.El paciente corrige los datos y vuelve a intentar la solicitud.
 * El paciente tiene la opción de corregir los datos y volver a intentar la solicitud.

### Condiciones
* Precondiciones: El paciente tiene acceso a internet y está registrado en el sistema.

* Postcondiciones: El paciente recibe un mensaje de error y no se reserva el turno.

* Suposiciones: Al menos uno de los datos personales ingresados es inválido.

* [Enlace del Escenario](https://drive.google.com/file/d/18PoPxXxTTHDWOZpAjg6gGu3XCZCY8Dy7/view?usp=sharing)

## Caso de uso 4 - Cancelar Turno Medico

### Descripcion General:
Brinda al paciente la posibilidad de cancelar un turno que ya ha sido reservado, siempre que esté dentro del plazo permitido por la institución médica. Esta opción permite liberar espacios en la agenda médica, favoreciendo la reprogramación de otros pacientes y optimizando el uso del tiempo profesional.
## Pasos desempeñados(Ruta Principal)
1.El paciente accede a la plataforma de turnos médicos.

 * El paciente puede acceder desde una computadora o teléfono

2.El paciente selecciona la opción "Cancelar Turno Médico".

 * La opción debe estar visible en el menú de gestión de turnos.

3.El paciente visualiza la lista de turnos activos.

 * El sistema muestra los turnos futuros del paciente.

4.El paciente selecciona el turno que desea cancelar

 * Cada turno incluye detalles como fecha, hora y médico.

5.El sistema solicita confirmación de cancelación.

 * Se muestra un mensaje de advertencia y confirmación.

6.El paciente confirma la cancelación del turno.
 *  El paciente acepta la cancelación.

7.El sistema actualiza el estado del turno a "Cancelado".
 * El sistema registra que el turno ha sido cancelado por el paciente.

8.El sistema libera el horario del turno cancelado.
 * El horario queda disponible para otros pacientes.

### Condiciones
* Precondiciones: El paciente debe tener al menos un turno activo en el sistema.
* Poscondiciones:El turno queda cancelado y el horario disponible para otros usuarios.
* Suposiciones: El paciente realiza la cancelación con la antelación requerida por la política del sistema (por ejemplo, 24h).

Prioridad:Alta

Riesgo:Bajo

## Escenario 1:Cancelar Turno Médico - Cancelación exitosa
Descripcion:El paciente accede al sistema y selecciona "Cancelar Turno Medico"

### Pasos desempeñados
1.El paciente accede a la plataforma de turnos médicos.
 * El paciente accede desde su dispositivo a la plataforma.

2.El paciente selecciona la opción "Cancelar Turno Médico".
 * La opción debe estar disponible junto a cada turno.

3.El sistema solicita confirmación.
 * El sistema previene cancelaciones accidentales.

4.El paciente confirma la cancelación.
 * El paciente confirma que desea cancelar el turno.

5.El sistema actualiza el estado del turno.
 * El sistema registra el turno como "cancelado".

6.El sistema libera el horario.
 * El turno queda disponible para otros pacientes.

7.El médico es notificado.
 * El sistema avisa al profesional médico.

8.El paciente recibe una confirmación.
 * El sistema notifica al paciente.

### Condiciones
* Precondiciones:El paciente tiene al menos un turno activo y acceso a internet.
* Postcondiciones:El turno se cancela, queda libre para nuevos pacientes y el médico es notificado.
* Suposiciones: El turno está dentro del plazo permitido para cancelar (por ejemplo, más de 24 horas antes).

Prioridad:Alto
Riesgo:Bajo

## Escenario 2:Cancelar Turno Médico - Cancelación fuera de plazo
Descripción: El paciente intenta cancelar un turno dentro del período no permitido (por ejemplo, menos de 24 horas antes).

### Pasos desempeñados
1.El paciente accede a la plataforma y selecciona un turno para cancelar.
 * Navega al listado de turnos.

2.El sistema verifica la hora del turno.
 * El sistema detecta si faltan menos de 24 horas.

3.El sistema bloquea la cancelación.
 * Muestra mensaje indicando que ya no se puede cancelar online

4.El sistema sugiere contactar con el centro médico
 * Ofrece un número de teléfono



### Condiciones
* Precondiciones:El paciente tiene un turno activo.
* Postcondiciones:El turno no se cancela automáticamente desde la plataforma.
* Suposiciones: El sistema impide cancelaciones fuera de plazo.

Prioridad:Media

Riesgo:Medio


 [Enlace del Escenario](https://drive.google.com/file/d/1pF1hLiTKPdGpvR7S2GwcTbqhClgDaMka/view?usp=sharing)


## Caso de uso 5 - Notificar Recordatorio de Turno
### Descripcion General:
Permite al sistema enviar recordatorios automáticos de turnos médicos previamente agendados, utilizando medios como correo electrónico, SMS o notificaciones móviles.
## Pasos desempeñados(Ruta Principal)
1.El sistema escanea la base de datos en busca de turnos próximos.

 * El sistema identifica todos los turnos con fechas dentro del umbral configurado.

2.El sistema valida los datos de contacto del paciente.

 * Verifica que el paciente tenga correo electrónico, teléfono u otra vía disponible.

3.El sistema genera el contenido del mensaje de recordatorio.

 * El mensaje incluye fecha, hora, tipo de consulta y médico asignado.

4.El sistema selecciona el canal de envío configurado por el paciente.

 * Según preferencia del paciente (email, SMS, app).

5.El sistema envía el recordatorio.

 * Se realiza el envío por el canal correspondiente.

6.El sistema registra el envío en el historial del paciente.

 * Guarda la hora, canal y estado del envío.
### Condiciones
* Precondiciones: El paciente tiene al menos un turno programado en el sistema.
* Poscondiciones: El paciente recibe un recordatorio con los detalles del turno.
* Suposiciones: El sistema está funcionando correctamente y el servicio de mensajería está activo.

Prioridad:Alta
Riesgo:Baja

## Escenario 1:Notificación enviada con éxito
Descripción: El sistema detecta un turno próximo y envía el recordatorio sin inconvenientes.

### Pasos desempeñados
1.El sistema detecta un turno próximo.
 * Se ejecuta una búsqueda automatizada de turnos dentro del período configurado (ej. 24-48h).

2.El sistema valida los datos del paciente.
 * Verifica que el paciente tenga medios válidos de contacto.

3.El sistema genera el mensaje.
 * Se utiliza una plantilla con los detalles del turno.

4.El sistema envía el mensaje.
 * El mensaje se envía por el canal preferido del paciente.

5.El sistema registra el envío.
 * Se guarda la operación con sello de tiempo y estado del envío.

### Condiciones
* Precondiciones:El paciente tiene un turno confirmado dentro del plazo de aviso configurado.
* Postcondiciones:El paciente recibe la notificación del turno
* Suposiciones:El servicio de notificaciones funciona correctamente.

Prioridad:Alta

Riesgo:Baja

## Escenario 2:Falla en el envío del recordatorio
Descripción: El sistema detecta un turno próximo y genera el mensaje correctamente, pero ocurre un error técnico durante el intento de envío del recordatorio.

### Pasos desempeñados
1.El sistema detecta un turno próximo.
 * Se activa el proceso programado para buscar turnos cercanos.


2.El sistema valida los datos del paciente.
 * Verifica si el paciente tiene medios válidos de contacto.


3.El sistema genera el mensaje.
 * Se compone el texto del recordatorio con los datos del turno.


4.El sistema intenta enviar el mensaje.
 * El mensaje se canaliza al proveedor (email, SMS, push).



5.El envío falla.
 * El sistema detecta que no pudo completar el envío (error de red, error del servidor, tiempo de espera agotado).


6.El sistema registra el fallo en el historial.
 * Se guarda el evento como fallido, con el motivo del error.

### Condiciones
* Precondiciones:El paciente tiene un turno y un canal de notificación válido.
* Postcondiciones:No se entrega el mensaje. El sistema puede intentar un reenvío o dejarlo registrado.
* Suposiciones:Falla momentánea del servidor de envíos.

Prioridad:Media

Riesgo:Medio


[Enlace del Escenario](https://drive.google.com/file/d/1pIKxRgHVAE6OwdnHBCwb27edqs4g69u2/view?usp=sharing)
