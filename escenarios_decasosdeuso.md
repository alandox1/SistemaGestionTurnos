# Escenarios de Casos de Uso

## Caso de uso 1 - Reprogramar turno

### Descripcion general
Permitir a la Recepcionista modificar la fecha y/o hora de un turno médico previamente agendado para un paciente, a solicitud de este, asegurando la actualización de la agenda del médico y la notificación correspondiente al paciente.

## Flujo de eventos
### Pasos Desempeñados(ruta principal)

1.La Recepcionista accede al módulo de "Gestión de Turnos" en el sistema. 

 * Acceso a la interfaz de gestión.

2.La Recepcionista busca el turno original del Paciente.

 * Completa un formulario con nombre, DNI, correo, dirección, teléfono, etc.

3.El Sistema muestra los detalles del turno encontrado.

 * Presenta información del turno

4.La Recepcionista confirma el turno con el Paciente y selecciona "Reprogramar Turno".

 * Valida que sea el turno correcto.

5.El Sistema presenta un calendario con la disponibilidad de nuevos horarios.

 * Muestra slots libres para el mismo médico/especialidad.

6.La Recepcionista consulta con el Paciente y selecciona el nuevo horario deseado.

 * Interacción verbal para elección del paciente.

7.La Recepcionista confirma la reprogramación en el sistema.

 * Acción de confirmación explícita.

8.El Sistema libera el horario del turno original.

 * Marca el turno original como cancelado/reprogramado.

9.La Recepcionista informa verbalmente al Paciente sobre el nuevo horario

 * Comunicación directa de la confirmación.

### Condiciones

* **Precondiciones:** La Recepcionista ha iniciado sesión en el sistema de gestión de turnos médicos y
posee los permisos necesarios para modificar citas.

* **Poscondiciones:** El turno original del Paciente ha sido liberado (marcado como "reprogramado" o
"cancelado por reprogramación") en el sistema.

* **Suposiciones:** El formulario de búsqueda de turnos y reprogramación funciona correctamente

Prioridad: Alta

Riesgo: Media

[Enlace del Escenario](https://drive.google.com/file/d/1ImFNVPk5NlMwteKoioJqPe1z_GwNJf9e/view?usp=sharing)

## Escenario 1:Reprogramar turno- Reprogramacion exitosa

Nombre del escenario: Reprogramar turno- Reprogramacion exitosa

Descripción: la Recepcionista debe iniciar la reprogramación de múltiples turnos debido a un cambio en la disponibilidad de un médico, y el paciente acepta sin problemas.

### Pasos desempeñado
1.La Recepcionista accede al módulo de "Gestión de Turnos" en el sistema. 

 * Acceso a la interfaz de gestión.

2.La Recepcionista busca el turno original del Paciente.

 * Completa un formulario con nombre, DNI, correo, dirección, teléfono, etc.

3.El Sistema muestra los detalles del turno encontrado.

 * Presenta información del turno

4.La Recepcionista confirma el turno con el Paciente y selecciona "Reprogramar Turno".

 * Valida que sea el turno correcto.

5.El Sistema presenta un calendario con la disponibilidad de nuevos horarios.

 * Muestra slots libres para el mismo médico/especialidad.

6.La Recepcionista consulta con el Paciente y selecciona el nuevo horario deseado.

 * Interacción verbal para elección del paciente.

7.La Recepcionista confirma la reprogramación en el sistema.

 * Acción de confirmación explícita.

8.El Sistema libera el horario del turno original.

 * Marca el turno original como cancelado/reprogramado.

9.La Recepcionista informa verbalmente al Paciente sobre el nuevo horario

 * Comunicación directa de la confirmación.

### Condiciones

* Precondiciones: La Recepcionista tiene acceso al sistema y permisos para modificar agendas.

* Postcondiciones: El turno original del Paciente ha sido marcado como "Reprogramado" o "Cancelado por Ausencia del Médico".

* Suposiciones:  El formulario de búsqueda de turnos y reprogramación funciona correctamente

Prioridad: Alta

Riesgo: Media

 [Enlace del Escenario](https://drive.google.com/file/d/1rEjVAtPLHxXDsPqsM78jggARf29QBHSx/view?usp=sharing)

## Escenario 2:Reprogramar turno -  Reprogramación Fallida
Nombre del escenario: Reprogramar turno -  Reprogramación Fallida

Descripción: La Recepcionista intenta reprogramar un turno, pero el sistema rechaza la operación porque el turno original no cumple con las reglas de negocio (ej., tiempo mínimo de antelación), lo que lleva a la Recepcionista a proponer una alternativa.

### Pasos desempeñados
1.El Paciente contacta a la Recepcionista solicitando reprogramar un turno para hoy mismo (ej., en 1 hora).

* Solicitud de reprogramación urgente.

2.La Recepcionista accede al módulo de "Gestión de Turnos" y busca el turno del Paciente.

* Búsqueda y acceso al turno.

3.El Sistema muestra los detalles del turno encontrado.

* Visualización de la información del turno.
  
4.La Recepcionista selecciona la opción "Reprogramar Turno".

* Intención de iniciar el proceso de reprogramación. 

5.El Sistema realiza una validación automática de las políticas de reprogramación (ej., tiempo mínimo de antelación).

* Verificación de reglas de negocio (ej., el turno es dentro de 1 hora y la política es 2 horas).

6.El Sistema muestra un mensaje de error a la Recepcionista: "No se puede reprogramar un turno con menos de 2 horas de antelación."

* Mensaje claro de rechazo y motivo.

7.La Recepcionista comunica la situación al paciente explicando la política de la clínica.

* Explicación transparente de la política.

8.La Recepcionista registra la decisión final del Paciente en el sistema.

* Se documenta la resolución.

### Condiciones

* Precondiciones: El Paciente solicita reprogramar un turno con una antelación menor a la permitida por las reglas de negocio.

* Postcondiciones: El turno original del Paciente permanece inalterado o es cancelado (si el Paciente decide)

* Suposiciones:  El sistema tiene implementadas y configuradas las reglas de negocio de tiempo mínimo para reprogramación.

Prioridad: Alta.

Riesgo: Medio.

[Enlace del Escenario](https://drive.google.com/file/d/19625u_NJNJ6zfiF_h74w14XCisji7vbK/view?usp=sharing)


## Caso de uso 2 - Acceder historial clinico
### Descripcion General:
La Recepcionista consulta la información administrativa y un resumen limitado del historial clínico de un paciente para confirmar datos de contacto, obra social o historial de atenciones previas, antes de una consulta o para agendar un nuevo turno.

## Pasos desempeñados(Ruta Principal)
1. La Recepcionista selecciona al Paciente desde su agenda de turnos o lo busca en el sistema.

 * Identificación del paciente.

2. La Recepcionista selecciona la opción "Acceder al Historial Clínico" (o "Ver Ficha de Paciente").        

 * Inicio de la acción de acceso.

3. El Sistema verifica las credenciales de la Recepcionista y sus permisos de acceso al historial del Paciente.        

 * Validación de usuario y autorización del rol.

4. El Sistema verifica la disponibilidad y existencia del historial clínico del Paciente.        

 * Comprobación de integridad de datos.

5. El Sistema carga y presenta la vista del historial clínico, limitada a las secciones permitidas para la Recepcionista (ej., datos de contacto, obra social, lista de atenciones).       
 * Visualización de la información según permisos.

6. La Recepcionista navega a través de las secciones accesibles para verificar la información requerida.

* Revisión de datos administrativos.

7. La Recepcionista utiliza la información del historial para confirmar los datos del Paciente o para completar una tarea administrativa.

* Utilización de datos para procesos de recepción.

### Condiciones

* Precondiciones:  Existe un historial clínico registrado para el Paciente
* Poscondiciones:  La Recepcionista ha consultado la información administrativa necesaria del historial clínico
* Suposiciones:  El sistema de gestión de turnos tiene un módulo integrado o acceso al historial clínico con diferenciación de roles.

Prioridad:Alto

Riesgo:Medio

[Enlace Del Escenario](https://drive.google.com/file/d/1s8Xyrvil-fhIU45gaWZGSa5WFTWNwFkm/view?usp=sharing)

## Escenario 1:Acceder historial clinico - Acceso fallido
### Descripcion General:
Una Recepcionista intenta acceder al historial clínico de un paciente, pero el sistema informa que no se encontró ningún historial asociado a ese paciente, indicando un posible error en el registro o una falta de historial previo.

## Pasos desempeñados(Ruta Secundaria)
1. La Recepcionista selecciona al Paciente (ej., un paciente nuevo o con un registro antiguo sin historial cargado) desde el sistema.

  * Identificación del paciente.

2. La Recepcionista selecciona la opción "Acceder al Historial Clínico".

  * Inicio de la acción de acceso.

3. El Sistema verifica las credenciales de la Recepcionista y sus permisos de acceso.

  * Validación de usuario y autorización.
  
4. El Sistema intenta localizar el historial clínico asociado al Paciente seleccionado.                
  
  * Búsqueda del historial en la base de datos.


5. El Sistema determina que no existe un historial clínico registrado para el Paciente, o no lo puede cargar.

  * El historial no se encuentra o hay un error de acceso a datos.        
  
7. El Sistema muestra un mensaje de error a la Recepcionista: "Historial Clínico no encontrado para este Paciente." o "Error al cargar el historial."

  * Notificación clara de la ausencia o fallo.

8. La Recepcionista informa al Paciente (si aplica) sobre la ausencia de historial o contacta al personal de TI si es un error técnico.

  * Gestión de la excepción.

* Precondiciones:   Se selecciona un Paciente para el cual no existe un historial clínico en el sistema o no es accesible.
* Poscondiciones:   El acceso al historial clínico es denegado o no se logra cargar.
* Suposiciones:   El sistema tiene una base de datos de historiales clínicos

Prioridad: Media

Riesgo: Bajo




* [Enlace del Escenario](https://drive.google.com/file/d/1MMEcBkL7AByZBlNoc0a1xQIfvYvThOti/view?usp=sharing)

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
