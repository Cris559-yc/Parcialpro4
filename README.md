# Parcialpro4
En El Salvador existen muchos talleres y y tecnicos independientesde reparacion de computadoras que realizan los presupuestos de forma manula, ya sea por medio de un cuadreno donde llevan sus apuntes, de calculando a base de su propia memoris e incluso en WhatsApp tomando notas. Estos metodos pueden provocar distintos errores al momento de sumar costos, aplicar recargos o para registrar los servicios solicitados. Al no tener una herramienta sencilla para poder registrar y calcular los precios, el cliente puede llegar a recibir una informacion erronea y el tecnico puede perder tiempo recalculando costos y tambien puede tener perdidas.
Este tipo de situaciones pueden generar: Perdida de tiempo en atencion al cliente. Presupuestos con montos incorrectos. Falta de control sobre los servicios que se proporcionaron y cuel fue el monto total. Una mala experiencia en la atención al cliente.
Por eso como solucion a esto se ha propuesto una pagina web que permita ingresar el nombre del cliente, seleccionar uno y/o varios servicios con precios estandar y elegir el nivel de urgencia para poder generar automaticamente el presupuesto total en pantalla.

¿Qué valor agregado tiene el uso de WebComponents a su proyecto?
El uso de WebComponents agrega modularidad y reutilización. En este proyecto se creó el componente personalizado <resultado-presupuesto>, el cual encapsula la sección donde se muestran los resultados del cálculo. Esto mejora la organización del código, facilita el mantenimiento y permite reutilizar el componente en otras pantallas o futuras versiones sin duplicar lógica de presentación.

¿De qué forma manipularon los datos sin recargar la página?
Se manipularon los datos usando JavaScript del lado del cliente con un evento sobre el formulario:
Se escuchó el evento submit con addEventListener.
Se evitó la recarga de la página usando event.preventDefault().
Se obtuvieron los valores del input, checkboxes y select con el DOM (getElementById, querySelectorAll).
Se actualizó el resultado en pantalla dinámicamente usando innerHTML dentro del WebComponent.

¿De qué forma validaron las entradas de datos? Expliquen brevemente
Se validó de dos formas:
Validación HTML: se usó required en campos obligatorios (como el nombre del cliente y el select de urgencia).
Validación con JavaScript: antes de calcular, el programa verifica:
Que el nombre del cliente no esté vacío (trim()).
Que exista al menos un servicio seleccionado (checkboxes marcados).
Que la urgencia haya sido seleccionada (no valor vacío).
Si alguna validación falla, se muestra una alerta y se detiene el proceso con return.

¿Cómo manejaría la escalabilidad futura en su página?
Para escalar el proyecto en el futuro se podría:
Separar el proyecto en archivos: index.html, styles.css y app.js.
Crear más WebComponents (ej: componente de servicios, componente de historial, componente de formulario).
Guardar presupuestos en localStorage o integrar un backend (Node.js/PHP) con base de datos para historial y usuarios.
Implementar validaciones más robustas (patrones, mensajes inline, manejo de errores).
Usar control de versiones y estructura modular para agregar nuevas funciones sin afectar lo existente.

Cristian Yahir Campos Aparicio.  SMSS109222
Lindys Arely Martinez Herrera.   SMSS170822
