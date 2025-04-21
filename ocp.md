# Principio de Abierto/Cerrado (OCP)
El objetivo principal del Principio de Abierto/Cerrado es permitir que el software sea extensible para nuevas funcionalidades sin necesidad de modificar su código ya existente.
Busca crear sistemas que puedan crecer y adaptarse a nuevos requerimientos sin alterar la base de código que ya funciona.Si cada vez que necesitas agregar una nueva funcionalidad a tu software tienes que cambiar el código existente, introduces riesgos de errores, 
aumentas la complejidad y dificultas el mantenimiento.El Principio de Abierto/Cerrado resuelve esto permitiendo extender la funcionalidad de tu software sin necesidad de modificar el código que ya funciona. Esto se logra creando abstracciones que definen un comportamiento general, y luego implementando nuevas funcionalidades
## Motivacion
Uno de los principales problemas que enfrentaba el sistema de gestión de turnos médicos era su dificultad para adaptarse a nuevos requerimientos sin alterar partes del código que ya estaban funcionando. Un ejemplo claro de esta situación se daba en el módulo de notificaciones. Inicialmente, la lógica de envío de notificaciones
estaba centralizada en una única clase, donde se usaban múltiples estructuras condicionales para determinar si se debía enviar un correo electrónico, un mensaje de texto (SMS) o realizar una llamada automatizada.
Este principio establece que las clases deben estar abiertas para su extensión, pero cerradas para su modificación. Es decir, un sistema bien diseñado debería permitir agregar nuevas funcionalidades sin tener que cambiar el código ya existente.

Al aplicar este principio al módulo de notificaciones, se rediseñó la estructura para trabajar con una interfaz común, que define el comportamiento esperado para cualquier tipo de notificador.
A partir de esta interfaz, se pueden crear múltiples clases concretas —como NotificadorEmail, NotificadorSMS o NotificadorWhatsApp—, cada una con su propia lógica de envío.

Ejemplo del mundo real

Un ejemplo del mundo real sería el de una máquina expendedora diseñada inicialmente para ofrecer solo tres bebidas. Si cada nueva bebida obliga a reprogramar la lógica principal, mantener el sistema se vuelve complejo. Pero si cada bebida funciona como un módulo independiente,
agregar una nueva es tan simple como conectar una nueva unidad, sin tocar las ya existentes.
