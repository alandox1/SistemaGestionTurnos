# Principio de Segregación de Interfaces (ISP)
En el sistema de gestión de turnos médicos, había componentes que estaban conectados a estructuras muy grandes que incluían muchas funciones innecesarias. Por ejemplo, ciertos módulos encargados de gestionar los turnos también estaban obligados a incluir funciones relacionadas con reportes estadísticos o configuraciones administrativas, aunque no las necesitaran. Esto hacía que los cambios en funciones no relacionadas afectaran a todo el sistema y aumentaban el riesgo de errores.

El principio ISP propone dividir esas interfaces grandes en partes más pequeñas y específicas, de modo que cada componente del sistema dependa únicamente de lo que realmente necesita. Aplicando este principio, se crearon interfaces más simples y enfocadas, como una para manejo de turnos, otra para notificaciones y otra para reportes.

## Motivacion
En el desarrollo del sistema para la administración de citas médicas, se hizo evidente que ciertos elementos internos del software se encontraban atados a capacidades que no eran parte de su función principal. Por ejemplo, un componente dedicado exclusivamente a la visualización de las citas en la pantalla del usuario se veía en la necesidad de incorporar lógica relacionada con la creación de informes estadísticos, la configuración general del sistema o la gestión de las cuentas de usuario. Este inconveniente surgía directamente de la inobservancia del principio de segregación de interfaces (ISP). Esta directriz establece que ningún componente debería verse obligado a depender de herramientas o funciones que no utiliza en su operación cotidiana. En esencia, cada pieza del sistema debería funcionar con el mínimo conjunto de dependencias necesario.

Para remediar esta situación, las estructuras de software complejas se descompusieron en interfaces más pequeñas y especializadas, cada una enfocada en un propósito específico. De esta manera, el módulo encargado de mostrar las citas solo interactúa con una interfaz que le provee las herramientas de visualización; el módulo de informes utiliza una interfaz diseñada exclusivamente para la manipulación de datos de reportes; y así sucesivamente. Este enfoque simplifica cada parte del sistema, incrementa su estabilidad y facilita las tareas de mantenimiento y modificación sin la introducción de riesgos innecesarios.

Ejemplo del mundo real

Imaginá que un médico solo necesita una hoja con el nombre del paciente y la hora del turno. Pero en lugar de eso, le dan un formulario de diez páginas con información financiera, datos de otros pacientes y estadísticas de la clínica. No solo pierde tiempo, sino que corre el riesgo de confundirse. En cambio, si cada profesional recibe solo la información que necesita, puede trabajar mejor y con menos errores. Eso es exactamente lo que propone este principio: darle a cada parte del sistema solo lo que realmente va a usar.

## Estructura de Clases

![SolidISP](https://github.com/user-attachments/assets/c69ac19e-eb84-49e3-b9b4-4f1de05eaac8)

[Estructura de Clases](https://drive.google.com/file/d/10YVFEO_VDqeF7pl-suyfbp-3p_uWsVUx/view?usp=sharing)

