# Laboratorio-1- Martes jueves 2:00pm-4:00pm

Integrantes: Daniel Salgado Mazo, Duvan Pinilla, Juan David Castro

contraseñas (1234) (secret/secreto)

1. Ventajas de Ajax frente a la recarga tradicional
Ajax (Asynchronous JavaScript and XML) permite que la página web se comunique con el servidor en segundo plano, ofreciendo varias ventajas clave sobre el modelo tradicional (donde cada clic recarga la página entera):

Actualización parcial: Solo se actualiza la parte de la interfaz que necesita cambiar (como una tabla de resultados), en lugar de volver a cargar toda la cabecera, menús y estilos.

Mejor experiencia de usuario (UX): La navegación se siente fluida y similar a una aplicación de escritorio. Se eliminan los "pantallazos en blanco" y las interrupciones mientras el servidor responde.

Ahorro de ancho de banda: Al enviar y recibir únicamente los datos necesarios (por ejemplo, un fragmento de HTML o un objeto JSON) y no todo el código de la página, el consumo de red disminuye.

Interacción continua: El usuario puede seguir interactuando con otras partes de la página mientras espera que una consulta pesada se resuelva en el servidor.

2. Diferencia entre execute y render (en el contexto de JSF/Ajax)
Estos atributos definen qué entra al servidor y qué sale del servidor durante una petición Ajax:

execute (Entrada/Procesamiento): Define qué componentes de la vista deben enviar sus datos al servidor para ser procesados en el ciclo de vida (conversión, validación y actualización del modelo). Si tienes un formulario con varios campos, pero en el execute solo indicas el ID de un campo de texto, el servidor solo procesará y validará ese texto específico.

render (Salida/Actualización visual): Define qué componentes de la vista deben redibujarse en el navegador una vez que el servidor termina de procesar la petición. Es el equivalente a decir: "Cuando termines, actualiza únicamente esta tabla y este mensaje de error".

3. Por qué CriteriaBuilder es útil en consultas dinámicas
En JPA (Java Persistence API), CriteriaBuilder permite construir consultas a la base de datos utilizando objetos de Java en lugar de concatenar cadenas de texto (como se haría con SQL o JPQL puro). Es ideal para consultas dinámicas por lo siguiente:

Estructura programática: Cuando un usuario puede elegir entre múltiples filtros opcionales (por ejemplo, buscar por nombre, por fecha, o por ambos), concatenar cadenas de texto con if/else se vuelve propenso a errores de sintaxis y espacios faltantes. CriteriaBuilder permite ir añadiendo predicados (condiciones WHERE) a una lista de forma limpia y segura.

Seguridad de tipos en tiempo de compilación: Si te equivocas en el nombre de una propiedad o en el tipo de dato, el compilador de Java te avisará antes de ejecutar el programa (especialmente si usas el Metamodelo de JPA). Con JPQL en texto, el error solo "estalla" cuando la aplicación ya está corriendo.

Prevención de Inyección: Al manejar los parámetros internamente como objetos, elimina el riesgo de inyección de código SQL/JPQL.
