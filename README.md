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
Se desea agilizar el proceso de compras online por medio de un watsonAssistant, a continuación se muestra el flujo que ayudará con la venta de productos.

![WhatsApp Image 2020-04-28 at 12 35 27 PM](https://user-images.githubusercontent.com/44415995/80523327-8121fa80-8953-11ea-9478-966fc70828ac.jpeg)



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

<img width="408" alt="1" src="https://user-images.githubusercontent.com/44415995/80521457-aa8d5700-8950-11ea-8cdb-9a1d14e2ee69.PNG">

### Paso 7:
El siguiente paso a seguir es entrenar el modelo, primero se comienza con los “intent” o “intenciones”, este entrena al asistente para comprender la variedad de formas en que los usuarios expresan una idea o inquietud. Para ello se selecciona “Create intent” y se le asigna un nombre a la intención y los ejemplos para entrenar el modelo.

- Creamos la intención #comprar, #Estado_Pedido, #Quejas_Reclamos y #saludos.

- La intención comprar es creada para entender cuando el usuario quiere comprar, trate de realizar varios ejemplos para que el assistant se entrene mejor.

<img width="400" alt="2" src="https://user-images.githubusercontent.com/44415995/80522661-8d598800-8952-11ea-83fa-1b4c6cd98a1d.PNG">

- Estado de pedido es una intención creada para entender a un usario cuando desee saber el estado de su pedido.

<img width="400" alt="3" src="https://user-images.githubusercontent.com/44415995/80523381-a0208c80-8953-11ea-90c2-04d22a98e54c.PNG">

La intención quejas y reclamos ayudará al assistant a identificar cuando una personas tenga algúna queja o reclamo.

<img width="400" alt="4" src="https://user-images.githubusercontent.com/44415995/80523395-a6166d80-8953-11ea-8b7e-41abe40b6f8b.PNG">

Y la intención saludo se creo para que el assistant tenga la capacidad de entender un saludo.

<img width="400" alt="5" src="https://user-images.githubusercontent.com/44415995/80523398-a6af0400-8953-11ea-9d25-59f29e23e873.PNG">

### Paso 8:
Una vez ingresados los “Entity”, se ingresan las entidades los cuales son sustantivos, palabras clave o entidades regulares, para ello se selecciona “Create entity” donde se le asigna un nombre y los sustantivos. Para este modelo se añadieron @Afirmativo, @Negativo, @Id, @Numero_Celular, @Tipo_Computadora, @Salir.

- Afirmativo, es creada para aquellos nodos que tienen una respuesta positiva.

<img width="520" alt="6" src="https://user-images.githubusercontent.com/44415995/80525003-30f86780-8956-11ea-9ab8-2d53ec516fb4.PNG">

- Negativo, es creada para aquellos nodos que tienen una respuesta negativa.

<img width="520" alt="7" src="https://user-images.githubusercontent.com/44415995/80525004-3190fe00-8956-11ea-97a1-675aa0b535fc.PNG">

- Para el caso de Id, seleccionamos el tipo patterns y se escoge una entidad regular que sea para número del 1 al 5                                                                                                                                                         
<img width="520" alt="8" src="https://user-images.githubusercontent.com/44415995/80525006-3190fe00-8956-11ea-8976-958d1a724f39.PNG">

- El número de celultar, también es una entidad regular que valida que el dato ingresado sea un número de 10 dígitos.

<img width="520" alt="cel" src="https://user-images.githubusercontent.com/44415995/80546964-a4ad6b00-897c-11ea-979f-72c9f5b20e22.PNG">

- En la entidad tipo computadora, agregamos todos las clases de coputadora que se van a vender. 

<img width="520" alt="10" src="https://user-images.githubusercontent.com/44415995/80525010-32299480-8956-11ea-9ff7-e9ddf1a3b054.PNG">

- Por ultima la entidad salir es usada en caso de que el usuario no quiera seguir usando el assistant.

<img width="520" alt="11" src="https://user-images.githubusercontent.com/44415995/80525011-32299480-8956-11ea-8ec7-cf05d3d3e55c.PNG">


### Paso 9:

Ahora vamos a añadir los diálogos, para ello seleccionamos en el costado izquierdo la opción que dice "Dialog" o "Dialogo" y seguimos los siguientes pasos: 

9.1 Primero vamos a añadir los diálogos, para ello se debe seleccionar “Add node” o “Añadir nodo”.

![](https://github.com/emeloibmco/Watson-Assistant-Hands-On/issues/2#issue-609428841)

Una vez añadido se proporciona un nombre a el nuevo nodo y selecciona ya sea un “Intent” o un “Entity”, (creado anteriormente) según convenga.

9.2 Aqui se crea el nodo saludo, que responde a las entradas clasificadas por el asistente en la entidad “saludo”

<img width="591" alt="nombre saludo" src="https://user-images.githubusercontent.com/46906169/80656246-54024480-8a46-11ea-979e-8290f008b25b.PNG">

9.3 Vamos a crear el nodo Volver_Inicio_Salir, dejando el condicional inicial del asistente como vacio.

<img width="499" alt="Volver inicio" src="https://user-images.githubusercontent.com/46906169/80658702-74cd9880-8a4c-11ea-8d2c-414299e0bf70.PNG">

9.4 Luego creamos el nodo salir 

<img width="511" alt="salir" src="https://user-images.githubusercontent.com/46906169/80658834-d8f05c80-8a4c-11ea-8c97-382db14bfa57.PNG">

9.5 Ahora vamos a añadir el nodo correspondiente a comprar, haciendo uso de la entidad “comprar” en el condicional inicial y seleccionando en la lista desplegable del “assistant respond” el tipo “option”. 

En el title escribimos "¿Que artículo deseas comprar?" y añadimos una opción dando clic a "Add option" para determinar la visualizacion del texto escribimos en "list lable" para añadir un valor, que debe corresponder a una entidad o intención, escribimos en "value"

<img width="487" alt="nodo comprar config" src="https://user-images.githubusercontent.com/46906169/80656427-cb37d880-8a46-11ea-9191-e3e3404027d2.PNG">

9.6 Añadimos un nodo hijo por cada producto que exista en el menú de compras

<img width="367" alt="nodo hijo comprar" src="https://user-images.githubusercontent.com/46906169/80657319-e7d51000-8a48-11ea-820a-47fe80c5512c.PNG">

9.7 Llenamos los campos como se muestra a continuación, para mostrar una imagen en el dialogo basta con buscar la imagen en internet y copiar su enlace.

<img width="524" alt="nodo mac book" src="https://user-images.githubusercontent.com/46906169/80657452-3bdff480-8a49-11ea-8aa7-7bae5c8b6b17.PNG">

Dentro del mismo nodo creamos un submenú que pregunta si quiere o no comprar el producto de ese nodo, se crea añadiendo un tipo de respuesta dando clic en "Add response type" ubicado en la parte inferior del nodo. Como se muestra acontinuación:

<img width="499" alt="submenu mac" src="https://user-images.githubusercontent.com/46906169/80657718-fa9c1480-8a49-11ea-995d-62320b824e63.PNG">

9.8 Creamos las respuestas de para cada opcion del submenú anterior, estas respuestas se añadiran al dialogo en forma de nodos hijos del nodo del producto, siendo si y no cada opción tiene un nodo asociado.

<img width="499" alt="submenu mac" src="https://user-images.githubusercontent.com/46906169/80657718-fa9c1480-8a49-11ea-995d-62320b824e63.PNG">
>

En caso de haber elegido si, el mensaje que se va a mostrar en ese nodo será el siguiente.
<img width="508" alt="afirmativo" src="https://user-images.githubusercontent.com/46906169/80658215-2966ba80-8a4b-11ea-9161-589d2c11be69.PNG">

Vamos al final del nodo y selecionamos en la lista desplegable jump to, y elegimos el nodo Volver_Inicio_Salir

<img width="442" alt="salto volver al inicio" src="https://user-images.githubusercontent.com/46906169/80658419-b27df180-8a4b-11ea-91f8-b0e07ddb1f80.PNG">

En caso de haber elegido no, el mensaje que se va a mostrar en ese nodo será el siguiente.
<img width="513" alt="negativo" src="https://user-images.githubusercontent.com/46906169/80658255-4602f280-8a4b-11ea-888e-7397bab2e1f0.PNG">

Vamos al final del nodo y selecionamos en la lista desplegable jump to, y elegimos el nodo Volver_Inicio_Salir

<img width="442" alt="salto volver al inicio" src="https://user-images.githubusercontent.com/46906169/80658419-b27df180-8a4b-11ea-91f8-b0e07ddb1f80.PNG">

9.9 Vamos a crear el nodo destinado para quejas y reclamos, hace uso de la intencion #Quejas_Reclamos en el condicional inicial. Damos clic en la parte superior derecha del nodo en el boton ![iconocuztomize](https://user-images.githubusercontent.com/46906169/80659107-97ac7c80-8a4d-11ea-805f-850bfbf1bd41.PNG) para habilitar el slot y llenar los campos como se muestra a continuación:

<img width="494" alt="quejas y reclamos" src="https://user-images.githubusercontent.com/46906169/80659431-9465c080-8a4e-11ea-9bd9-99f830f3e5ea.PNG">

#### Este nodo debe saltar al nodo Volver_Inicio_Salir



### Vista Preliminar

![Watson-Assistant-Preview-Link-Google-Chrome-2020-04-29-17-51-13](https://user-images.githubusercontent.com/56199403/80654959-2667cc00-8a43-11ea-9b56-c5d91461ccf2.gif)


## 3. Conservar el Watson Assistant 🔧

Para que tu Watson Assistant se mantenga siendo funcional es recomendable:

### 2.1 Actualiza los intentes:
Siempre que sea posible crear nuevas entidades o elimina las que los usuarios realmente no estén utilizando.
### 2.2 Escribe diferentes formas de un mismo mensaje:
Los usuarios pueden preguntar de diferentes formas es por eso que es necesario que una sola pregunta tenga varias versiones.
### 2.3 Guía a los usuarios a través de la conversación:
Para que los usuarios tengan una buena experiencia y deseen seguir usando en Assistant es necesario que se guíen desde el principio hasta el final de la conversación.
### 2.4 Cuida el flujo de la conversación:
Cada interacción debe conducir a la siguiente que ya fue definida. Es conveniente que la conversación este guionizada para que los usuarios solo tengan que seguir el guion creado.
### 2.5 Asegúrese que su interfaz conversación este siempre actualizada:
Watson Assistant está diseñado para simular una conversación, pero se recomienda no solo usar textos, sino que por medio de IBM también se puede enriquecer con imágenes, botones, etc.


## Construido con 🛠️
_Se uso IBM Cloud para utilizar los servicios de Watson Assistant que nos proporcionó las herramientas necesarias para crear el chat-bot_
* [IBM](https://www.ibm.com/cloud/watson-assistant/) - El servicio



## Autores ✒️
* **IBM** - *Equipo IBM Cloud*


