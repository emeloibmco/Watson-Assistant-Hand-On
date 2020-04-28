# Watson-Assistant-Hand-On

Watson Assistant es un bot cognitivo que puede ser personalizado para adaptase a sus necesidades empresariales, el asistente direcciona las consultas de sus clientes a un conocimiento, lo que proporciona la respuesta adecuada. Los conocimientos de diálogo devuelven respuestas que son creadas por el usuario para proporcionar información sobre los temas o tareas sobre los que los usuarios realizan preguntas y sobre cómo preguntan sobre las mismas y el producto crea de forma dinámica un modelo de aprendizaje automático que se adapta para comprender las mismas solicitudes de usuario y otras similares.

Watson Assistant es un bot alojado completamente que está gestionado por IBM Cloud, lo que significa que no tiene que preocuparse por configurar o mantener la infraestructura para darle soporte.

## 1. Conceptos Básicos 📋 
### Dialog skill
Una Skill es un contenedor para la inteligencia artificial que le permite a un asistente ayudar a sus clientes.

Un asistente dirige las solicitudes por el camino óptimo para resolver un problema del cliente. Agregue habilidades para que su asistente pueda proporcionar una respuesta directa a una pregunta común o hacer referencia a resultados de búsqueda más generalizados para algo más complejo
Un dialog skill comprende las preguntas o solicitudes típicas de los usuarios y las responde o las cumple siguiendo un diálogo escrito por usted.

### Itens
Una intención representa el propósito de la entrada de un usuario, como una pregunta sobre ubicaciones de negocios o un pago de facturas. Usted define una intención para cada tipo de solicitud de usuario que desea que su aplicación admita. El nombre de una intención siempre tiene el prefijo del caracter ``` #```. Para entrenar la habilidad de diálogo para reconocer sus intenciones, usted proporciona muchos ejemplos de entrada del usuario e indica a qué intenciones se asignan.

Se proporciona un catálogo de contenido que contiene intenciones comunes preconstruidas que puede agregar a su aplicación en lugar de crear la suya propia. Por ejemplo, la mayoría de las aplicaciones requieren una intención de saludo que inicia un diálogo con el usuario. Puede agregar el catálogo de contenido General para agregar una intención que salude al usuario y haga otras cosas útiles, como finalizar la conversación.

### Dialogo
Un diálogo es un flujo de conversación ramificado que define cómo responde su aplicación cuando reconoce las intenciones y entidades definidas. Utiliza el editor de diálogo para crear conversaciones con los usuarios, proporcionando respuestas basadas en las intenciones y entidades que reconoces en su entrada.

Para permitir que su habilidad de diálogo maneje preguntas más matizadas, defina entidades y haga referencia a ellas desde su diálogo.

### Entidades
Una entidad representa un término u objeto que es relevante para sus intentos y que proporciona un contexto específico para un intento. Por ejemplo, una entidad podría representar una ciudad donde el usuario desea encontrar una ubicación comercial o el monto de un pago de facturas. El nombre de una entidad siempre tiene como prefijo el caracter ```@```.

Puede entrenar el dialog skill para reconocer sus entidades proporcionando valores y sinónimos de términos de entidad, patrones de entidad o identificando el contexto en el que una entidad se usa típicamente en una oración. Para ajustar su diálogo, regrese y agregue nodos que verifiquen las menciones de la entidad en la entrada del usuario además de las intenciones.

Mas información en: 
https://cloud.ibm.com/docs/assistant?topic=assistant-skills
https://cloud.ibm.com/docs/services/assistant-icp?topic=assistant-private-getting-started

## 2. Desarrollo de un Watson Assistant por medio de IBM CLOUD 🚀

### Caso de uso 

Actualmente a nivel internacional se está presentando una pandemia ocasionada por el COVID-19, lo cual ha generado que las personas tengan muchas inquietudes las cuales no pueden aclarar tan fácilmente o de fuentes oficiales. Por esa razón se desarrolló un ChatBot con el fin de aclarar dichas dudas brindando información oficial con el fin de evitar que se cree pánico y desinformación. 

### Paso a paso del desarrollo 

### Paso 1:

Iniciar sesión en IBM Cloud, en caso de que no se cuente con una cuenta, crearla en este enlace https://cloud.ibm.com/registration

### Paso 2:

En la sección de catálogo buscamos Watson Assistant y se selecciona dicho servicio 

![1](https://user-images.githubusercontent.com/44415995/77944254-3d6ca000-7284-11ea-8760-ffb4c6dc5682.jpg)

### Paso 3:

Para crear el servicio de Watson Assistant, primero se debe seleccionar la región, en este caso se seleccionó Dallas y posteriormente selecciona el tipo de plan que más se acomode a sus necesidades. Una vez realizado esto se le asigna un nombre al servicio y se le da clic a la opción de “Create” o “Crear”.

![2](https://user-images.githubusercontent.com/44415995/77944449-a05e3700-7284-11ea-86d0-e6d81c49dc90.jpg)

### Paso 4:

En la ventana que se cargó se le da clic a “Launch Watson Assistant” o “Iniciar Launch Watson Assistant” y se abrirá una nueva ventana.

![3](https://user-images.githubusercontent.com/44415995/77944487-b1a74380-7284-11ea-867e-8de6afa46216.jpg)

### Paso 5:

Ahora se selecciona la opción de “Skill” la cual tiene este icono ![Icono1](https://user-images.githubusercontent.com/44415995/77944907-5c1f6680-7285-11ea-9ec6-8ebc41320025.jpg) y se selecciona “Create Skill” o “Crear skill”, luego se selecciona “Dialog Skill” y “Next” o “Siguiente”.

![4](https://user-images.githubusercontent.com/44415995/77944530-be2b9c00-7284-11ea-9ce7-145f3eb13d55.jpg)

### Paso 6:

Ahora se procede a configurar el modelo donde es importante asignarle un nombre y el idioma en el que se va a implementar el chatbot en este caso español.

![5](https://user-images.githubusercontent.com/44415995/77944551-c5eb4080-7284-11ea-9333-79afde5f6fb7.jpg)
