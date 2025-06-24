# Anexo - Aplicación de Patrón de Diseño estructural - Facade

El patrón **Facade** (Fachada) es un patrón de diseño **estructural** que proporciona una interfaz unificada a un conjunto de interfaces en un subsistema. Una fachada define una interfaz de nivel superior que hace que el subsistema sea más fácil de usar.

En nuestro sistema de gestión de salud, la interacción con el sistema para realizar acciones como solicitar un turno, reprogramarlo o consultarlo, puede involucrar a varias clases (Turno, Medico, Agenda, Paciente). El patrón Facade simplifica estas interacciones complejas.

## Motivación

Inicialmente, para que un Recepcionista o Paciente realice una acción como "solicitar un turno", podría necesitar interactuar directamente con varias clases del subsistema: primero, consultar la Agenda del Medico para disponibilidad, luego quizás crear un Turno, y finalmente actualizar el `Paciente` o `Medico` con la referencia al nuevo turno. Esta interacción directa genera un alto acoplamiento entre los clientes (Recepcionista, Paciente) y las clases internas del subsistema.

El control manual por parte de la Recepcionista al solicitar turnos para los pacientes puede ser propenso a errores si tiene que coordinar manualmente entre la disponibilidad de Medico y la creación de Turno. Un Paciente que quiera consultar sus propios turnos también enfrentaría una complejidad similar si tuviera que buscar en múltiples lugares.

El patrón Facade ayuda a resolver esto al:
1.  **Simplificar la Interfaz:** Proporciona una interfaz única y más sencilla para un conjunto de funcionalidades complejas del subsistema.
2.  **Reducir el Acoplamiento:** Los clientes (ej. Recepcionista, Paciente) solo interactúan con la Facade, y no necesitan conocer los detalles internos o las interacciones de las múltiples clases del subsistema (Turno, Medico, Agenda).
3.  **Encapsular la Complejidad:** La lógica de coordinar las clases del subsistema para realizar una tarea específica se encapsula dentro de la Facade.

Para esto, crearemos una GestionTurnosFacade que centralice las operaciones de turno.

## Estructura de Clases

Aquí se muestra cómo se implementa el patrón Facade para simplificar la gestión de turnos.
![Diagram 2025-06-23 22-00-27](https://github.com/user-attachments/assets/ee7615be-7bc7-466f-989e-d2295a2bb92e)

[Diagrama](https://drive.google.com/file/d/19j9VB4S_ROmsSlvNbEQcxhOpcpJAxAkE/view?usp=sharing)

