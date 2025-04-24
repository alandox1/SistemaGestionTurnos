# Principio de Inversión de Dependencias (DIP)
En el sistema de gestión de turnos médicos, algunos módulos importantes estaban conectados directamente a servicios específicos, como una base de datos concreta o un sistema particular de envío de correos. Esto significaba que cualquier cambio en esos servicios afectaba directamente a todo el sistema, generando errores y dificultando la evolución o migración hacia nuevas tecnologías.

Este principio propone invertir las dependencias: en lugar de que la lógica principal del sistema dependa directamente de servicios concretos, se trabaja con abstracciones (por ejemplo, "servicio de notificación" en lugar de "servicio de correo"). Así, se pueden cambiar o reemplazar los servicios reales sin tocar el funcionamiento principal del sistema. Esto hace que el sistema sea mucho más flexible, reutilizable y fácil de adaptar con el tiempo.

## Motivación
En el sistema de gestión de turnos médicos, uno de los mayores problemas era que los módulos de alto nivel (como la lógica principal del sistema, que gestiona la programación de citas y la asignación de médicos) dependían directamente de implementaciones de bajo nivel (como bases de datos específicas o sistemas de notificación como el correo electrónico). Este enfoque hacía que cualquier cambio en estos componentes de bajo nivel tuviera un gran impacto en toda la aplicación.

Al aplicar DIP, el sistema fue reestructurado para que la lógica principal del sistema dependiera de abstracciones (como interfaces de notificación, bases de datos y servicios) en lugar de implementaciones concretas. Por ejemplo, en lugar de que el sistema de gestión de turnos dependa directamente de un servicio de correo electrónico específico, se creó una interfaz general de "Servicio de Notificación", y el sistema interactúa con esta interfaz, sin saber qué servicio de notificación está siendo utilizado realmente. Esto permitió cambiar o reemplazar el sistema de notificación sin afectar el resto del sistema.El código de alto nivel se desacopló de los detalles de implementación, haciendo que el sistema fuera más flexible, fácil de probar, y más sencillo de mantener a largo plazo.

Ejemplo del mundo real

Imaginemos que una empresa de transporte tiene una aplicación que organiza el envío de productos. La aplicación está directamente conectada a un sistema específico de rastreo de envíos. Si la empresa decide cambiar de proveedor de rastreo, tendría que modificar toda la aplicación para adaptarse a las nuevas herramientas del nuevo proveedor.

Sin embargo, si la aplicación está diseñada para depender de una interfaz común de rastreo (en lugar de depender directamente de un proveedor específico), solo necesitaría cambiar la implementación del proveedor de rastreo sin tocar el resto de la aplicación. Esto permite una gran flexibilidad y agilidad ante cambios, además de reducir los riesgos de errores al modificar solo una pequeña parte del sistema.


![Diagram 2025-04-23 21-06-29](https://github.com/user-attachments/assets/31035188-c1dd-4c53-b39d-6c3862ca0357)

[Diagrama](https://drive.google.com/file/d/1ydUDaQ-p0jeKEhjUnK_mlX3t2s_vSzKJ/view?usp=sharing)

