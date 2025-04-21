# Principio de Responsabilidad Única (SRP)

El Principio de Responsabilidad Única (Single Responsibility Principle, SRP) tiene como propósito asegurar que una clase tenga una sola razón para cambiar. 
Esto significa que una clase debe tener una única responsabilidad y que todas sus funciones deben estar relacionadas con esa responsabilidad.

El problema que aborda el SRP es el acoplamiento excesivo y la falta de cohesión 
en las clases. Cuando una clase tiene múltiples responsabilidades, cualquier cambio en una de esas responsabilidades puede afectar a otras partes del sistema.
Esto hace que el código sea más difícil de mantener, entender y modificar.

El SRP soluciona este problema al asegurar que cada clase tenga una sola responsabilidad. Al separar las responsabilidades en clases diferentes, 
se reduce el acoplamiento entre las clases y se facilita la reutilización del código. Esto hace que el código sea más modular y fácil de mantener.

## Motivacion
El problema que aborda el SRP es el acoplamiento excesivo y la falta de cohesión en las clases. Cuando una clase tiene múltiples responsabilidades, cualquier cambio en una de esas responsabilidades puede afectar a otras partes del sistema.
Esto hace que el código sea más difícil de mantener, entender y modificar. Además, el acoplamiento excesivo puede llevar a la propagación de errores y a una mayor complejidad en el sistema.

El SRP soluciona este problema al asegurar que cada clase tenga una sola responsabilidad. Al separar las responsabilidades en clases diferentes,
se reduce el acoplamiento entre las clases y se facilita la reutilización del código. Esto hace que el código sea más modular y fácil de mantener.Además, al tener clases con una única responsabilidad,
los cambios en una clase no afectan a otras partes del sistema, lo que reduce el riesgo de introducir errores

### Ejemplo del mundo real

maginemos una aplicación de gestión de empleados en una empresa. Inicialmente, tenemos una clase Empleado que maneja tanto los datos personales del empleado como la lógica de cálculo de salarios y 
la generación de informes de desempeño. Esta clase tiene múltiples responsabilidades, lo que hace que sea difícil de mantener y entender.

Para aplicar el SRP, podemos separar las responsabilidades en tres clases diferentes: Empleado, CalculadoraDeSalarios y GeneradorDeInformes. La clase Empleado manejará solo los atributos y comportamientos relacionados con los datos personales del empleado.
La clase CalculadoraDeSalarios gestionará la lógica de cálculo de salarios, y la clase GeneradorDeInformes manejará la generación de informes de desempeño. 









