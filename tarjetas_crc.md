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

**Colaboradores:** Agenda, Turno, Médico,recepcionista.

**Propiedad:** nombre, apellido, fechaNacimiento, DNI, direccion,telefono,email.

![Captura de pantalla 2025-04-09 230123](https://github.com/user-attachments/assets/5e61f527-e456-481e-9d38-5e99d1d11460)

### Tarjeta CRC: Médico

**Nombre de la Clase:** Médico

**Superclase:** Persona

**Subclase:** —

**Pensamiento del objeto:** Quiero recordar turnos. Necesito ver mi agenda, registrar observaciones y diagnósticos. Puedo modificar turnos si es necesario. Quiero acceder al historial de consultas de mis pacientes.

**Responsabilidades:** Visualizar y gestionar su agenda de turnos,Registrar diagnósticos y observaciones médicas,Acceder al historial clínico de sus pacientes,Modificar o cancelar turnos.

**Colaboradores:** Turno,Paciente,HistoriaClinica,Agenda

**Propiedad a la que se referenciará:**
nombre, apellido, especialidad, matriculaProfesional, horariosAtencion

![Captura de pantalla 2025-04-09 230223](https://github.com/user-attachments/assets/93de00cf-130c-416d-af0a-e07e3c8eb282)



### Tarjeta CRC: Recepcionista

**Nombre de la Clase:** Recepcionista

**Superclase:** Persona

**Subclase:** —

**Pensamiento del objeto:**
Me encargo de la gestión de la agenda. Registro nuevos pacientes.organizo turnos, cancelo citas si es necesario.Me encargo de asignar turnos.Me encargo de consultar o actualizar los datos de los pacientes.

**Responsabilidades:** Registrar nuevos pacientes en el sistema,Asignar turnos a pacientes,Cancelar o reprogramar turnos,Consultar agenda de médicos,Consultar los datos o actualizar de un paciente.


**Colaboradores:** Paciente,Turno,Agenda,Médico

**Propiedad**:nombre,apellido,dni,email,telefono,turno.

![Captura de pantalla 2025-04-09 230838](https://github.com/user-attachments/assets/5db1f615-5b32-4e0b-9628-459238a7c942)


### Tarjeta CRC: Turno

**Nombre de la Clase:** Turno

**Superclase:** —

**Subclase:** —

**Pensamiento del objeto:** Tengo una fecha y una hora asignada,se quien me atendera,se a quien debo atender,mi estado puede cambiar segun la accion realizada

**Responsabilidades:** Conocer su fecha y hora, Conocer el paciente asignado, Conocer el médico asignado, Cambiar su estado.

**Colaboradores:** Paciente, Médico,Recepcionista.

**Propiedad:** fecha, hora, estado, paciente,motivoCancelacion.


![Captura de pantalla 2025-04-09 231310](https://github.com/user-attachments/assets/3d6c55ed-fe45-4fa3-a718-17ac98fade05)



### Tarjeta CRC: Agenda

**Nombre de la Clase:** Agenda

**Superclase:** —

**Subclase:** —

**Pensamiento del objeto:** Organizo los turnos de un médico. Permito visualizar disponibilidad y asignar turnos nuevos.Muestro qué días y horarios están disponibles.Me encargo de mantener actualizada la disponibilidad para nuevos turnos,Asigno los turnos a los pacientes.

**Responsabilidades principales:** Organizar agenda,Mostrar disponibilidad del médico,modificar o eliminar turnos,Filtrar por día o paciente,Asignar turno

**Colaboradores:** Médico, Turno, Paciente

**Propiedad:** fechaInicio, fechaFin, medicoId, listaTurnos,turno.


![Captura de pantalla 2025-04-09 225817](https://github.com/user-attachments/assets/f49b1418-e2e0-4917-93b5-72d138691247)




