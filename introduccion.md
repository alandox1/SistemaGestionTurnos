## Anexo - Introducción al Diseño Orientado a Objetos
¿Qué es la Programación Orientada a Objetos (POO)?

La Programación Orientada a Objetos (POO) es un paradigma de programación basado en la organización del código en objetos, que representan entidades del mundo real.
Es importante porque permite crear software modular, reutilizable y fácil de mantener.

## Los cuatro fundamentos de POO
Abstracción
Es la capacidad de representar elementos del mundo real en el código.
Ejemplo: 
 Un control remoto de TV
 
 Control Remoto 
 
- Canal actual
  
- Volumen

+ Cambiar canal
  
+ Subir/bajar volumen
  
+ Encender/apagar


Encapsulamiento
Protege los datos de un objeto, permitiendo acceso solo a través de métodos específicos.
Ejemplo:
Un microondas

Tiene botones para calentar, descongelar, etc.

No ves ni puedes modificar directamente los componentes internos (como los circuitos o el transformador).

- Temporizador (interno)
  
- Voltaje (interno)

+ Iniciar cocción
  
+ Ajustar tiempo
  
+ Parar
  
Herencia
Permite que una clase reutilice características de otra.
Ejemplo: Vehículos

Un automóvil y una moto comparten cosas comunes como:

Tienen ruedas

Pueden moverse

Usan combustible o batería

- Ruedas
  
- Motor
  
- Combustible

[ Auto ] ← hereda de Vehículo

- Aire acondicionado

[ Moto ] ← hereda de Vehículo

- Casco

Polimorfismo
Permite que una misma acción tenga diferentes comportamientos según el objeto.
Ejemplo: Un "Animal" puede hacer un sonido, pero cada tipo de animal emite un sonido diferente (perro: ladrido, gato: maullido).

Requisitos iniciales del sistema
Registro de usuarios: El sistema debe permitir la creación y gestión de usuarios.
Gestión de turnos: Los usuarios deben poder solicitar, cancelar y reprogramar turnos.
Notificaciones: El sistema debe enviar recordatorios de turnos vía correo o mensaje.
Historial de turnos: Se debe permitir consultar turnos pasados.
Control de acceso: Solo usuarios registrados pueden acceder a ciertas funciones.

## Casos de Usos

1. Nombre del caso de uso: Registrar nuevo paciente
   
Actor(es) involucrado(s): Paciente

Descripción breve: Un paciente se registra en el sistema proporcionando sus datos personales.

Flujo principal de eventos:

El paciente accede al formulario de registro.

Completa sus datos personales: nombre, DNI, correo electrónico, teléfono, etc.

El sistema valida los datos.

Si son válidos, el sistema crea un perfil de paciente.

Precondiciones: El paciente no debe estar registrado previamente con el mismo DNI o correo.

Postcondiciones: El paciente queda registrado y puede iniciar sesión para solicitar turnos.

2. Nombre del caso de uso: Iniciar sesión en el sistema

Actor(es) involucrado(s): Paciente, Médico, Administrador

Descripción breve: Un usuario del sistema inicia sesión para acceder a sus funcionalidades.

Flujo principal de eventos:

El usuario accede a la página de inicio de sesión.

Ingresa su usuario (DNI o correo) y contraseña.

El sistema verifica las credenciales.

Si son correctas, el sistema permite el acceso según el perfil (paciente, médico o admin).

Precondiciones: El usuario debe estar registrado.

Postcondiciones: El usuario accede al sistema con los permisos correspondientes.

3. Nombre del caso de uso: Solicitar turno médico
   
Actor(es) involucrado(s): Paciente

Descripción breve: El paciente selecciona un médico, una especialidad y solicita un turno.

Flujo principal de eventos:

El paciente inicia sesión.

Selecciona la especialidad y/o profesional médico.

Consulta los horarios disponibles.

Selecciona un día y hora.

El sistema confirma la reserva del turno.

Precondiciones: El paciente debe estar registrado e iniciar sesión.

Postcondiciones: El turno queda reservado y asociado al paciente y al médico correspondiente.

4. Nombre del caso de uso: Cancelar turno
   
Actor(es) involucrado(s): Paciente

Descripción breve: El paciente cancela un turno previamente reservado.

Flujo principal de eventos:

El paciente accede a su lista de turnos.

Selecciona el turno que desea cancelar.

Confirma la cancelación.

El sistema elimina el turno y lo libera para otros pacientes.

Precondiciones: El paciente debe haber reservado un turno previamente.

Postcondiciones: El turno se libera y queda disponible en el sistema.

5. Nombre del caso de uso: Registrar atención médica
   
Actor(es) involucrado(s): Médico

Descripción breve: El médico registra la atención de un paciente en su turno asignado.

Flujo principal de eventos:

El médico inicia sesión y accede a su agenda.

Selecciona el turno correspondiente al paciente atendido.

Registra el diagnóstico, tratamiento y observaciones.

Guarda la información en la historia clínica del paciente.

Precondiciones: El turno debe estar asignado al médico y marcado como “en atención” o “confirmado”.

Postcondiciones: Los datos de atención quedan registrados y disponibles en el historial clínico del paciente.


## Boceto inicial del Diseño de Clases
![Captura de pantalla 2025-03-30 215756](https://github.com/user-attachments/assets/5948340a-80d8-4642-a307-5bd1b3fde944)

https://drive.google.com/file/d/1jiek8sjVPBmd5IyPmZswwbKYbqTEBVyl/view?usp=sharing


