# Principio de Inversión de Dependencias (DIP)
En el sistema de gestión de turnos médicos, algunos módulos importantes estaban conectados directamente a servicios específicos, como una base de datos concreta o un sistema particular de envío de correos. Esto significaba que cualquier cambio en esos servicios afectaba directamente a todo el sistema, generando errores y dificultando la evolución o migración hacia nuevas tecnologías.

Este principio propone invertir las dependencias: en lugar de que la lógica principal del sistema dependa directamente de servicios concretos, se trabaja con abstracciones (por ejemplo, "servicio de notificación" en lugar de "servicio de correo"). Así, se pueden cambiar o reemplazar los servicios reales sin tocar el funcionamiento principal del sistema. Esto hace que el sistema sea mucho más flexible, reutilizable y fácil de adaptar con el tiempo.

## Motivación
En el sistema de gestión de turnos médicos, una problemática significativa radicaba en el acoplamiento directo entre los módulos de alto nivel (responsables de la lógica de negocio central, como la gestión de la programación de citas y la asignación de profesionales de la salud) y las implementaciones concretas de los módulos de bajo nivel (tales como sistemas de persistencia de datos específicos o proveedores de servicios de notificación, como servidores de correo electrónico). Esta dependencia rígida implicaba que cualquier modificación o sustitución en la infraestructura de bajo nivel inducía efectos colaterales de gran magnitud en la totalidad de la aplicación.

La aplicación del Principio de Inversión de Dependencias (DIP) permitió refactorizar la arquitectura del sistema, orientándola hacia la dependencia de abstracciones (definidas mediante interfaces para servicios de notificación, repositorios de datos y otros servicios) en detrimento de las implementaciones particulares. A modo ilustrativo, en lugar de establecer una dependencia directa con un servicio de correo electrónico específico, se definió una interfaz genérica denominada "Servicio de Notificación". El subsistema de gestión de turnos interactúa con esta abstracción, desconociendo la implementación subyacente del servicio de notificación empleado. Esta estrategia posibilitó la sustitución o actualización de los componentes de bajo nivel sin propagar cambios a la lógica de negocio central. En consecuencia, se logró un desacoplamiento efectivo entre los módulos, incrementando la flexibilidad, la testabilidad y la mantenibilidad a largo plazo del sistema.

Ejemplo del mundo real

Imaginemos que una empresa de transporte tiene una aplicación que organiza el envío de productos. La aplicación está directamente conectada a un sistema específico de rastreo de envíos. Si la empresa decide cambiar de proveedor de rastreo, tendría que modificar toda la aplicación para adaptarse a las nuevas herramientas del nuevo proveedor.

Sin embargo, si la aplicación está diseñada para depender de una interfaz común de rastreo (en lugar de depender directamente de un proveedor específico), solo necesitaría cambiar la implementación del proveedor de rastreo sin tocar el resto de la aplicación. Esto permite una gran flexibilidad y agilidad ante cambios, además de reducir los riesgos de errores al modificar solo una pequeña parte del sistema.

### Estructura de clase

![Diagram 2025-04-23 21-06-29](https://github.com/user-attachments/assets/31035188-c1dd-4c53-b39d-6c3862ca0357)

[Estructura de Clase](https://drive.google.com/file/d/1ydUDaQ-p0jeKEhjUnK_mlX3t2s_vSzKJ/view?usp=sharing)

