# Escenarios de Casos de Uso

## Caso de uso 1 - Registrar nuevo paciente

### Descripcion general
Permite que un nuevo usuario se registre en el sistema proporcionando sus datos personales y de contacto. Una vez registrado, el paciente obtiene acceso a todas las funcionalidades del sistema, como solicitar turnos, consultar historial, y recibir notificaciones. Este proceso puede incluir validaciones como verificación de correo y control de duplicidad de datos (correo o documento).

## Flujo de eventos
### Pasos Desempeñados(ruta principal)

1.El usuario accede a la opcion "Crear Cuenta" 

 * Desde la página de inicio, el usuario selecciona esta opción.

2.Ingresa sus datos personales y de contacto

 * Completa un formulario con nombre, DNI, correo, dirección, teléfono, etc.

3.El sistema valida los datos

 * El sistema revisa que los campos estén completos y con formato correcto.

4.El sistema comprueba que no exista un usuario con el mismo correo o dni

 * El sistema revisa que los campos estén completos y con formato correcto.

5.El sistema registra al nuevo paciente

 * Si todo está correcto, se guarda la nueva cuenta.

### Condiciones

* **Precondiciones:** No debe existir una cuenta previo con el mismo correo/DNI
* **Poscondiciones:** Usuario registrado y habilitado para iniciar sesion
* **Suposiciones:** El formulario esta correctamente validado.

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

Precondiciones: El paciente tiene acceso a internet y está registrado en el sistema.

Postcondiciones: El paciente recibe un mensaje de error y no se reserva el turno.

Suposiciones: El turno seleccionado no está disponible.

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
1.El paciente inicia sesion

 * El paciente accede a su cuenta personal.

2.Ingresa a "Mis Turnos"

 * Desde el menú principal, elige la sección donde visualiza sus turnos agendados.

3.Selecciona un turno vigente

 * El paciente identifica el turno que desea cancelar y lo selecciona.

4.Confirma la cancelacion

 * El sistema solicita una confirmación para evitar errores.

5.El sistema elimina el turno y actualiza la agenda

 * El sistema elimina el turno y libera el horario en la agenda del médico.
### Condiciones
* **Precondiciones:** El turno debe existir y ser cancelable (no vencido)
* **Poscondiciones:** Turno eliminado del sistema,Agenda liberada
* **Suposiciones:** El turno no esta dentro del periodo de cancelacion restringida

* [Enlace del Escenario](https://drive.google.com/file/d/1FIO6ylXUcQnJ19nbvHQzxxEdevsmMKcl/view?usp=sharing)


## Caso de uso 5 - Notificar Recordatorio de Turno
### Descripcion General:
Funcionalidad automatizada del sistema que se encarga de enviar notificaciones recordatorias a los pacientes con turnos programados en las siguientes 24 o 48 horas. Este recordatorio puede enviarse vía correo electrónico o mensaje SMS, ayudando a reducir el ausentismo y mejorando la eficiencia operativa del centro de salud.
## Pasos desempeñados(Ruta Principal)
1.El sistema ejecuta una tarea programada

 * El sistema ejecuta automáticamente una función diaria

2.Consulta la base de datos de turnos

 * accede a los turnos del dia siguiente

3.Identifica turnos programados dentro de las proximas 24-48 horas.

 * Revisa los turnos programados para las próximas 24 a 48 horas.

4.Verifica que el paciente tenga datos de contactos validos

 * Se asegura de que el paciente tenga un correo o número válido.

5.Genera el contenido del mensaje recordatorio

 * El sistema arma el contenido con nombre del médico, especialidad, fecha y hora.

6.Envia la notificacion por el medio configurado(correo/sms)

 * Se envía por los canales configurados (correo electrónico,SMS).
### Condiciones
* **Precondiciones:** Turno registrado y datos de contacto disponible
* **Poscondiciones:** Notificacion enviada
* **Suposiciones:** El servicio de mensajeria funciona correctamente

* [Enlace del Escenario](https://drive.google.com/file/d/1e-lRHBjN39gbGlCuGKJeTsT5sLoyy8Nx/view?usp=sharing)
