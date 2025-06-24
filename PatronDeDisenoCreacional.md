# Patrón de Diseño: Singleton

## Propósito y Tipo del Patrón

El patrón **Singleton** (Instancia Única) es un patrón de diseño **creacional** que garantiza que una clase tenga solo una instancia y proporciona un punto de acceso global a ella.

En nuestro sistema de gestión de salud, el `Sistema` central es una entidad única que coordina todas las operaciones (gestión de turnos, pacientes, médicos, etc.). Asegurar que solo exista una instancia de `Sistema` previene inconsistencias de datos, problemas de sincronización y asegura un control centralizado de los recursos y la lógica de negocio, lo cual es crucial en un entorno multiusuario.

## Motivación

El control manual de muchas operaciones o la existencia de múltiples "puntos de entrada" o "instancias" de la lógica central de nuestro sistema podría generar inconsistencias de datos y conflictos, especialmente en un centro de salud donde varios recepcionistas o usuarios interactúan simultáneamente.

Por ejemplo, si hubiera múltiples instancias de la clase `Sistema` gestionando turnos, una instancia podría pensar que un horario está disponible mientras otra ya lo ha asignado, llevando a sobrecitas o errores en la agenda.

El patrón Singleton resuelve este problema al:
1.  **Garantizar una única instancia:** Solo se crea una y solo una instancia de la clase `Sistema`.
2.  **Proporcionar un punto de acceso global:** Todas las partes del sistema que necesiten interactuar con la lógica central pueden acceder a esta única instancia de manera consistente y controlada. Esto asegura la integridad y sincronización en los datos de los pacientes, médicos y turnos.

Para eso, la clase `Sistema` ahora tendrá una estructura que incorpora el patrón Singleton.

## Estructura de Clases

Aquí se muestra cómo la clase `Sistema` se modifica para implementar el patrón Singleton.

![Diagram 2025-06-23 21-31-36](https://github.com/user-attachments/assets/0c565787-244e-4c82-a376-f676bc342c4d)


[Diagrama](https://drive.google.com/file/d/16rg6yg0_UNVQZsQRb3u6oFmVb0iIPsxE/view?usp=sharing)
