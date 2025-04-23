# Principio de Sustitución de Liskov (LSP)
Es un tipo de principio de herencia y sustitución de objetos en programación orientada a objetos,cual su proposito es garantizar que las subclases puedan reemplazar a sus clases
padre sin alterar el comportamiento esperado del sistema.En el sistema de gestión de turnos médicos, se creó una clase base Usuario y varias subclases como Paciente, Médico y Administrador. 
Sin embargo, algunas subclases sobrescribían métodos heredados de forma que rompían la lógica general del sistema. Por ejemplo, si un método esperaba un objeto Usuario y se le pasaba un Administrador,
podía fallar porque este no tenía implementado correctamente un comportamiento esperado, como agendar turnos.
## Motivacion
Uno de los problemas más importantes que enfrentaba el sistema de gestión de turnos médicos era la forma en que se habían clasificado y organizado los diferentes tipos de usuarios del sistema. Existía una categoría general para todos los usuarios, de la cual se derivaban otros perfiles, como pacientes, médicos y administradores. El problema surgía cuando se asumía que todos estos usuarios podían hacer las mismas acciones, lo cual no era cierto. Por ejemplo, el sistema intentaba permitir que cualquier usuario pudiera pedir turnos médicos, cuando en realidad solo los pacientes deberían tener esa capacidad.

Esta suposición incorrecta provocaba que el sistema se volviera inconsistente. Se necesitaban hacer excepciones dentro del mismo funcionamiento para que los administradores, por ejemplo, no pudieran pedir turnos, a pesar de estar dentro del grupo general de “usuarios”. Esto complicaba el mantenimiento, introducía errores y hacía que el sistema fuese menos confiable con el tiempo.

Aquí es donde entra en juego el principio de sustitución de Liskov, uno de los principios SOLID. Este principio plantea que si algo pertenece a un grupo, debe comportarse como se espera dentro de ese grupo, sin generar problemas. Es decir, si alguien es tratado como un usuario, entonces debería poder realizar las acciones esperadas para un usuario, sin tener que hacer excepciones o ajustes especiales.

Para resolver el problema, se reorganizó la forma en que se definían los perfiles. En lugar de asumir que todos los usuarios pueden hacer lo mismo, se definieron claramente qué tipo de acciones puede realizar cada uno. Así, los pacientes pueden pedir turnos, los médicos pueden atenderlos y los administradores pueden gestionar el sistema. De esta manera, se evitan errores y se asegura que cada tipo de usuario actúe únicamente dentro de sus responsabilidades.

Un ejemplo del mundo real

Imaginemos que en una empresa todos los empleados tienen una tarjeta de acceso. Pero solo los ingenieros pueden entrar al laboratorio. Si se permite que todos los empleados usen la misma tarjeta para cualquier zona, entonces habrá que hacer excepciones cada vez que un empleado sin autorización quiera entrar al laboratorio. En cambio, si desde el principio se asignan accesos específicos según el rol de cada persona, no hace falta estar revisando constantemente quién puede hacer qué. El sistema funciona de forma más ordenada, segura y clara.

## Estructura de Clases

![SolidLSP](https://github.com/user-attachments/assets/a53cca7c-d3b4-427a-8bb5-3cf5c3dd4947)

[Estructura de clases](https://drive.google.com/file/d/1-hWIs_TFMcYxppuK0fVU2TL8FWhhg7C0/view?usp=sharing)

