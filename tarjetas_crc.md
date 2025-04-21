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

![Captura de pantalla 2025-04-21 143537](https://github.com/user-attachments/assets/c451b238-8081-4d05-96f9-27afa8450291)


### Tarjeta CRC: Médico

**Nombre de la Clase:** Médico

**Superclase:** Persona

**Subclase:** —

**Pensamiento del objeto:** Quiero recordar turnos. Necesito ver mi agenda, registrar observaciones y diagnósticos. Puedo modificar turnos si es necesario. Quiero acceder al historial de consultas de mis pacientes.

**Responsabilidades:** Visualizar y gestionar su agenda de turnos,Registrar diagnósticos y observaciones médicas,Acceder al historial clínico de sus pacientes,Modificar o cancelar turnos.

**Colaboradores:** Turno,Paciente,HistoriaClinica,Agenda

**Propiedad a la que se referenciará:**
nombre, apellido, especialidad, matricula, horariosAtencion


![Captura de pantalla 2025-04-21 143544](https://github.com/user-attachments/assets/90bddab9-6c66-4cc4-bced-d8de16c1cf31)



### Tarjeta CRC: Recepcionista

**Nombre de la Clase:** Recepcionista

**Superclase:** Persona

**Subclase:** —

**Pensamiento del objeto:**
Me encargo de la gestión de la agenda. Registro nuevos pacientes.organizo turnos, cancelo citas si es necesario.Me encargo de asignar turnos.Me encargo de consultar o actualizar los datos de los pacientes.

**Responsabilidades:** Registrar nuevos pacientes en el sistema,Asignar turnos a pacientes,Cancelar o reprogramar turnos,Consultar agenda de médicos,Consultar los datos o actualizar de un paciente.


**Colaboradores:** Paciente,Turno,Agenda,Médico,recepcionista

**Propiedad**:nombre,apellido,dni,email,telefono,direccion

![Captura de pantalla 2025-04-21 143551](https://github.com/user-attachments/assets/eda178b8-63a0-4bbf-a609-8c4d89f2b973)



### Tarjeta CRC: Turno

**Nombre de la Clase:** Turno

**Superclase:** —

**Subclase:** —

**Pensamiento del objeto:** Tengo una fecha y una hora asignada,se quien me atendera,se a quien debo atender,mi estado puede cambiar segun la accion realizada

**Responsabilidades:** Conocer su fecha y hora, Conocer el paciente asignado, Conocer el médico asignado, Cambiar su estado.

**Colaboradores:** Paciente, Médico,Recepcionista.

**Propiedad:** fecha, hora, estado, paciente,motivoCancelacion.


![Captura de pantalla 2025-04-09 225917](https://github.com/user-attachments/assets/47206eef-9b7f-41b0-b03b-3728cd20f0ec)

### Tarjeta CRC: Agenda

**Nombre de la Clase:** Agenda

**Superclase:** —

**Subclase:** —

**Pensamiento del objeto:** Organizo los turnos de un médico. Permito visualizar disponibilidad y asignar turnos nuevos.Muestro qué días y horarios están disponibles.Me encargo de mantener actualizada la disponibilidad para nuevos turnos,Asigno los turnos a los pacientes.

**Responsabilidades principales:** Organizar agenda,Mostrar disponibilidad del médico,modificar o eliminar turnos,Filtrar por día o paciente,Asignar turno

**Colaboradores:** Médico, Turno, Paciente

**Propiedad:** fechaInicio, fechaFin, medicoId, listaTurnos,turno.


![Captura de pantalla 2025-04-09 225817](https://github.com/user-attachments/assets/f49b1418-e2e0-4917-93b5-72d138691247)


* [Tarjetas CRC](https://drive.google.com/file/d/1u_hI6YER85QZzXQFLu4y4vB0H0hHy3-j/view?usp=sharing)



