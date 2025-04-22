# Principio de Segregación de Interfaces (ISP)
En el sistema de gestión de turnos médicos, había componentes que estaban conectados a estructuras muy grandes que incluían muchas funciones innecesarias. Por ejemplo, ciertos módulos encargados de gestionar los turnos también estaban obligados a incluir funciones relacionadas con reportes estadísticos o configuraciones administrativas, aunque no las necesitaran. Esto hacía que los cambios en funciones no relacionadas afectaran a todo el sistema y aumentaban el riesgo de errores.

El principio ISP propone dividir esas interfaces grandes en partes más pequeñas y específicas, de modo que cada componente del sistema dependa únicamente de lo que realmente necesita. Aplicando este principio, se crearon interfaces más simples y enfocadas, como una para manejo de turnos, otra para notificaciones y otra para reportes.

## Motivacion
En el sistema de gestión de turnos médicos, uno de los problemas que se detectó fue que ciertos módulos del sistema estaban obligados a depender de funcionalidades que no utilizaban. Por ejemplo, un componente que solo se encargaba de mostrar turnos también tenía que incluir funciones relacionadas con reportes estadísticos, configuración del sistema o administración de usuarios.Este problema se debe a una violación del principio de segregación de interfaces (ISP), que propone que ningún módulo debe estar obligado a depender de métodos que no necesita. Es decir, cada parte del sistema debe contar solo con lo justo y necesario para funcionar.

Para aplicar este principio, se dividieron las grandes estructuras en interfaces más pequeñas y especializadas, enfocadas en tareas concretas. Así, por ejemplo, el módulo de visualización de turnos depende únicamente de una interfaz que contiene funciones de visualización; el módulo de reportes depende de una interfaz que solo maneja reportes, y así sucesivamente. Esto hace que cada parte del sistema sea más sencilla, más estable y más fácil de mantener o modificar sin riesgos innecesarios.

Ejemplo del mundo real

Imaginá que un médico solo necesita una hoja con el nombre del paciente y la hora del turno. Pero en lugar de eso, le dan un formulario de diez páginas con información financiera, datos de otros pacientes y estadísticas de la clínica. No solo pierde tiempo, sino que corre el riesgo de confundirse. En cambio, si cada profesional recibe solo la información que necesita, puede trabajar mejor y con menos errores. Eso es exactamente lo que propone este principio: darle a cada parte del sistema solo lo que realmente va a usar.

## Estructura de Clases

![SolidISP](https://github.com/user-attachments/assets/c69ac19e-eb84-49e3-b9b4-4f1de05eaac8)

[Estructura de Clases](https://drive.google.com/file/d/10YVFEO_VDqeF7pl-suyfbp-3p_uWsVUx/view?usp=sharing)

