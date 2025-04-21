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

* [Enlace del Escenario](https://drive.google.com/file/d/1j0doeWnuMsGsl4PqhQ7tWTcx_9a1vFtB/view?usp=sharing)

## Caso de uso 2 - Iniciar sesion
### Descripcion General:
Permite a los usuarios del sistema (pacientes, médicos o administradores) acceder a su cuenta mediante un proceso de autenticación. El usuario debe ingresar su nombre de usuario y contraseña válidos para ingresar a su panel correspondiente. Este caso de uso es esencial para asegurar que solo usuarios autorizados accedan a las funcionalidades del sistema.

## Pasos desempeñados(Ruta Principal)
1.El usuario abre la pagina de login

 * El usuario accede a la plataforma.

2.Ingresa usuario y contraseña

 * Introduce su nombre de usuario y contraseña.

3.El sistema verifica credenciales

 * El sistema compara los datos ingresados con los registrados.

4.Redirige al panel correspondiente

 * El sistema redirige al usuario al menu dependiendo su rol
### Condiciones
* **Precondiciones:** Usuario debe estar registrado
* **Poscondiciones:** acceso permitido o denegado segun resultado
* **Suposiciones:** Los datos estan correctamente almacenados.

* [Enlace del Escenario](https://drive.google.com/file/d/1v-gOTcCT2iERNwYh5sB2k9Jy7grlCW9s/view?usp=sharing)

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
* **Precondiciones:** Usuario registrado e identificado,Agenda del medico disponible
* **Poscondiciones:** Turno asignado y confirmado
* **Suposiciones:** El sistema tiene conexion estable con la base de datos de turno

* [Enlace del Escenario](https://drive.google.com/file/d/1zacd-2sNYMeJ1r95mwzLyhNp1tMmyg5k/view?usp=sharing)

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
