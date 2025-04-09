# Herramientas Agile

## Tarjetas CRC
Las Tarjetas CRC (Clase-Responsabilidad-Colaboración) constituyen una
herramienta esencial en el enfoque de la programación orientada a objetos (POO). Se
utilizan para identificar y definir las clases principales de un sistema, así como sus
responsabilidades y colaboraciones dentro del contexto del sistema

### Tarjeta CRC: Paciente
**Caso de Uso 1**

**Nombre de la Clase:** Paciente

**Superclase:** Persona

**Subclase:**

**Pensamiento del objeto:** Sé qué especialista requiero junto a mis datos personales. Necesito ver cuándo y con quién tengo turno. Avisare cuando no pueda asistir. Mis datos pueden cambiar.
Quiero recordar mis turnos anteriores.

**Responsabilidades:** Solicitar un turno, Consultar sus turnos programados, Cancelar un turno, Actualizar sus datos personales, Ver el historial de sus consultas.

**Colaboradores:** Agenda, Turno, Médico.

**Propiedad:** nombre, apellido, fechaNacimiento, DNI, numeroHistoriaClinica.

![tarjetacrcpaciente drawio](https://github.com/user-attachments/assets/531d57fb-924a-449e-97e5-4184cfcdc287)
