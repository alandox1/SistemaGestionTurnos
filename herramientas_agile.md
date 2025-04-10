# Herramientas Agile

## Tarjetas CRC
Las Tarjetas CRC (Clase-Responsabilidad-Colaboración) constituyen una
herramienta esencial en el enfoque de la programación orientada a objetos (POO). Se
utilizan para identificar y definir las clases principales de un sistema, así como sus
responsabilidades y colaboraciones dentro del contexto del sistema

### Tarjeta CRC: Paciente

**Nombre de la Clase:** Paciente

**Superclase:** Persona

**Subclase:** -

**Pensamiento del objeto:** Sé qué especialista requiero junto a mis datos personales. Necesito ver cuándo y con quién tengo turno. Avisare cuando no pueda asistir. Mis datos pueden cambiar.
Quiero recordar mis turnos anteriores.

**Responsabilidades:** Solicitar un turno, Consultar sus turnos programados, Cancelar un turno, Actualizar sus datos personales, Ver el historial de sus consultas.

**Colaboradores:** Agenda, Turno, Médico.

**Propiedad:** nombre, apellido, fechaNacimiento, DNI, numeroHistoriaClinica.

![tarjetacrcpaciente drawio](https://github.com/user-attachments/assets/061342c7-b22c-4980-93f9-23fda2a965c7)


### Tarjeta CRC: Médico

**Nombre de la Clase:** Médico

**Superclase:** Persona

**Subclase:** —

**Pensamiento del objeto:** Atiendo pacientes en los horarios asignados. Necesito ver mi agenda, registrar observaciones y diagnósticos. Puedo modificar turnos si es necesario. Quiero acceder al historial de consultas de mis pacientes.

**Responsabilidades:** Visualizar y gestionar su agenda de turnos,Registrar diagnósticos y observaciones médicas,Acceder al historial clínico de sus pacientes,Modificar o cancelar turnos ,Consultar disponibilidad para nuevos turnos,Quiero recordar turnos.

**Colaboradores:** Turno,Paciente,HistoriaClinica,Agenda

**Propiedad a la que se referenciará:**
nombre, apellido, especialidad, matriculaProfesional, horariosAtencion

![tarjetacrcpaciente](https://github.com/user-attachments/assets/572455f4-6e30-4498-be79-5467380a5980)

### Tarjeta CRC: Recepcionista

**Nombre de la Clase:** Recepcionista

**Superclase:** Persona

**Subclase:** —

**Pensamiento del objeto:**
Me encargo de la gestión administrativa. Registro nuevos pacientes.organizo turnos, cancelo citas si es necesario.Me encargo de asignar turnos.Me encargo de consultar o actualizar los datos de los pacientes.

**Responsabilidades:**

Registrar nuevos pacientes en el sistema
.
Asignar turnos a pacientes

Cancelar o reprogramar turnos

Consultar agenda de médicos

Consultar los datos o actualizar de un paciente


**Colaboradores:** Paciente,Turno,Agenda,Médico

**Propiedad**:nombre,apellido,dni,email,telefono,turno.

![Captura de pantalla 2025-04-09 220302](https://github.com/user-attachments/assets/bb9fe3db-8baf-4cd2-84bd-f031c160c639)


### Tarjeta CRC: Turno

**Nombre de la Clase:** Turno

**Superclase:** —

**Subclase:** —

**Pensamiento del objeto:** Soy una cita médica. Tengo una fecha, una hora, un paciente y un médico asignado.Puedo ser reservado, modificado o cancelado.Debo informar si ya fui atendido.Soy un compromiso entre un paciente y un médico en una fecha y hora específica.

**Responsabilidades:** Reservar un espacio en la agenda,Almacenar estado (activo, cancelado, atendido),Asociar paciente y médico,Permitir cancelación o reprogramación

**Colaboradores:** Paciente, Médico, Agenda,Recepcionista.

**Propiedad:** fecha, hora, estado, paciente, médico

![tarjetacrcTurno drawio](https://github.com/user-attachments/assets/c4011285-652f-4932-95cf-101e7d200fcc)


### Tarjeta CRC: Agenda

**Nombre de la Clase:** Agenda

**Superclase:** —

**Subclase:** —

**Pensamiento del objeto:** Organizo los turnos de un médico. Permito visualizar disponibilidad y asignar turnos nuevos.Muestro qué días y horarios están disponibles.Me encargo de mantener actualizada la disponibilidad para nuevos turnos

**Responsabilidades principales:** <Mostrar turnos asignados,Mostrar disponibilidad del médico,Agregar, modificar o eliminar turnos,Filtrar por día o paciente

**Colaboradores:** Médico, Turno, Paciente

**Propiedad:** listaTurnos, medico, rangoFechas

![tarjetacrcAgenda drawio](https://github.com/user-attachments/assets/c81269dc-e3e8-499f-8380-d04893dcc972)



