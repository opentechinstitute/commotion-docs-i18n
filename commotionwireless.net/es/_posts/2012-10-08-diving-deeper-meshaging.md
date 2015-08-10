---
layout: blog
title: Profundizando en el "meshaging"
categories: [messaging,chat,UX,applications]
created: 2012-10-08
changed: 2012-10-29
post_author: The Work Department
lang: es
---
  En nuestra reciente <a href="https://commotionwireless.net/blog/exploring-meshaging" target="_blank">publicaci�n del blog sobre mensajes</a>, introdujimos nuestra aplicaci�n &ldquo;meshaging&rdquo; (chat b�sico) y explicamos algunos de los planes para nuestro futuro trabajo con �l. Todav�a estamos trabajando en este proyecto y hemos diagramado c�mo sucede exactamente la comunicaci�n en la aplicaci�n. Esto ha mejorado nuestro proceso interno y creemos que es beneficioso compartirlo.
En comparaci�n con los sistemas centralizados, basados en servidor, las aplicaciones de redes descentralizadas son un poco desordenadas: con el beneficio de la descentralizaci�n viene el costo de una mayor complejidad. Mantener la consistencia de los datos a trav�s de una red mesh es un problema dif�cil de resolver, y hay muchos enfoques interesantes para abordar este problema. Como dise�adores, nos interesamos en acoger la inconsistencia: �qu� sistemas podr�an existir, o incluso prosperar, en una red de conexiones inconsistentes o dispositivos transitorios? Esto es importante tener en cuenta debido a que una red mesh podr�a estar cambiando constantemente.
Para explorar el tema de la comunicaci�n descentralizada, decidimos trabajar a trav�s del dise�o de una aplicaci�n de chat de una red mesh en la que los nodos servir�an como hubs de chat. Consideramos como una aplicaci�n de chat descentralizada se ver�a con niveles variados de replicaci�n o mensajes compartidos entre nodos vecinos
Usamos la analog�a de la aplicaci�n del chat por su simplicidad y generalidad, pero puedes reemplazar los &ldquo;chats&rdquo; con cualquier tipo de mensajes de uno a varios. Actualmente, como un ejercicio, �realmente <em>deber�as</em> intentar y pensar en otro tipo de mensajes que podr�an ser transportados sobre una red mesh! Imagina una red de term�metros en un invernadero, o una red de sensores de movimiento que encienda luces, o muchas otras posibilidades.
<img alt="" class="decoded" src="/files/basic_chat_diagrams_for_blog_Artboard_1_0.png" style="width: 540px; height: 485px;" />
**Diagrama 1** (arriba) ilustra una aplicaci�n de chat en la que los nodos env�an mensajes s�lo a los clientes conectados localmente (cero saltos). Los n�meros 1, 2, y 3 representan los nodos conectados a la red mesh, y los peque�os �conos de personas designadas con letras representan las personas conectadas a cada uno de los nodos. En este escenario, los usuarios pueden chatear con otros usuarios en el mismo nodo. Por ejemplo, la persona H puede chatear con la persona J porque ambos est�n conectados al Nodo 2. No pueden, sin embargo, chatear con la Persona K o la Persona D, porque esos usuarios, aunque est�n conectados con la red de mesh, est�n en diferentes nodos.
<img id="internal-source-marker_0.5773324861970599" src="/files/basic_chat_diagrams_for_blog_Artboard_2_0.png" />
**Diagrama 2 **(arriba) ilustra a los usuarios en el Nodo 1 comunic�ndose (hop-cero/sistema de chat sin transmisi�n).
<img id="internal-source-marker_0.5773324861970599" src="/files/basic_chat_diagrams_for_blog_Artboard_3_0.png" />
**Diagrama 3** (arriba) ilustra a un vecino de al lado difundir un sistema de chat, en el que los nodos difundir�an todos los mensajes a nodos dentro de la distancia de un salto. Este sistema permitir�a a una persona chatear con las personas conectadas dentro de su propio nodo, o con sus vecinos de al lado, pero no con nodos a dos o m�s saltos. En el Diagrama 3, la Persona G puede chatear con la Persona C porque ambos est�n conectados al Nodo 1. Pero en esta etapa la Persona G tambi�n puede chatear con la Persona J porque J est� conectada con G del nodo 2 del vecino de al lado. Aunque, la Persona G no podr�a chatear con la Persona L, porque el Nodo 3, al que la Persona L est� conectado, est� a dos saltos de distancia.
<img id="internal-source-marker_0.5773324861970599" src="/files/basic_chat_diagrams_for_blog_Artboard_4.png" />
**Diagrama 4** (arriba) muestra como el vecino de al lado difunde el sistema de chat, ilustrando a los usuarios en el Nodo 1 comunic�ndose uno con el otro y a los usuarios en el Nodo 2.
Esperamos que estos diagramas puedan ayudar a incentivar conversaciones acerca del desarrollo de aplicaciones descentralizadas. Mantente atento para m�s mensajes.

