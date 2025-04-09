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


### Tarjeta CRC: Usuario

**Caso de Uso 2**

**Nombre de la Clase:** Usuario

**Superclase:** Persona
**Subclase:** Recepcionista, Médico, Administrador

**Pensamiento del objeto:** Tengo un nombre de usuario y una contraseña. Necesito verificar mis credenciales para acceder al sistema. Si son válidas, quiero usar el sistema según mi rol.

**Responsabilidades:**

Almacenar nombre de usuario y contraseña

Verificar credenciales

Establecer rol (tipo de usuario)

**Colaboradores:** GestordeAutenticacion, Persona

**Propiedad:** nombreUsuario, contraseña, rol
