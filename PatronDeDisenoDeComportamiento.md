# Anexo - Aplicación de Patrón de Diseño de Comportamiento - Observer

El patrón **Observer** (Observador) es un patrón de diseño **de comportamiento** que define una dependencia de uno a muchos entre objetos, de manera que cuando un objeto (el "Sujeto") cambia de estado, todos sus dependientes (los "Observadores") son notificados y actualizados automáticamente.

En nuestro sistema de gestión de salud, es crucial que cuando el estado de un Turno cambie (por ejemplo, se cancela, se reprograma, se atiende), otras partes del sistema, como el historial del paciente, las notificaciones de SMS/email o la agenda del médico, sean informadas y actualizadas sin que el Turno tenga que conocer explícitamente a todos sus "interesados".

## Motivación

El control manual para actualizar todos los componentes del sistema cuando el estado de un Turno cambia puede ser propenso a errores y muy ineficiente. Por ejemplo, si un turno se cancela, la Recepcionista tendría que recordar manualmente:
1.  Actualizar el estado del turno.
2.  Notificar al paciente.
3.  Actualizar la agenda del médico para liberar el horario.
4.  Posiblemente registrar el evento en un log de auditoría.

Este enfoque crea un fuerte acoplamiento entre la clase Turno y todas las clases que necesitan reaccionar a sus cambios de estado. Si se añade una nueva funcionalidad que debe reaccionar a un cambio de turno (ej. un sistema de facturación), tendríamos que modificar la clase Turno directamente.

El patrón Observer resuelve este problema al:
1.  **Desacoplar Sujeto y Observadores:** El Turno (Sujeto) no necesita saber qué clases específicas están interesadas en sus cambios. Solo mantiene una lista de observadores genéricos.
2.  **Automatizar Notificaciones:** Cuando el estado del Turno cambia, automáticamente notifica a todos los observadores registrados, quienes a su vez reaccionan apropiadamente.
3.  **Facilitar la Expansión:** Añadir nuevas funcionalidades que reaccionen a los cambios de turno es tan simple como crear un nuevo Observador e registrarlo. No se requiere modificar la clase Turno.

Para esto, la clase Turno actuará como el Sujeto, y crearemos interfaces para los Observadores que reaccionarán a los cambios.

## Estructura de Clases

Aquí se muestra cómo el patrón Observer se aplica para manejar las notificaciones de cambios en los turnos.

![Diagram 2025-06-23 22-23-39](https://github.com/user-attachments/assets/ac141503-15ed-4efe-9f4e-0b9868982874)

[Diagrama](https://drive.google.com/file/d/1UgAeb8PMCtuCM-QlO76v2vvdVt-R_3la/view?usp=sharing)

