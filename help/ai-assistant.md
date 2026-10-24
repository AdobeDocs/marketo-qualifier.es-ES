---
title: Uso del chat de IA
description: Aprenda a utilizar el chat de IA en [!DNL Adobe Marketo Qualifier] para buscar cuentas, elaborar proyectos de alcance y obtener respuestas basadas en los datos de CRM, participación y Centro de conocimiento.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/LHCHAk0rsNwLsKFhKMlHaLL7xkkCEAKFNDMEonb2TdQ'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Adobe Marketo Qualifier
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 1%
---

# Chat de IA

AI Chat responde a preguntas en lenguaje natural en función de su contexto de ventas. Utilícelo para buscar una cuenta, prepararse para una llamada, elaborar un borrador de alcance y priorizar su trabajo sin salir de [!DNL Adobe Marketo Qualifier].

![Botón de chat de IA](assets/ai-chat.png){width="800" zoomable="yes"}

## Abrir chat de IA

Para abrir el panel de chat, selecciona el botón **[!UICONTROL AI Chat]** flotante. El panel se abre junto a la página actual para que pueda tener a la vista un posible cliente, una cuenta o un flujo de trabajo saliente. Para cambiar el tamaño del panel, arrastre su borde. Para cerrar el panel, vuelve a seleccionar **[!UICONTROL Charla de IA]**.

>[!NOTE]
>
>La disponibilidad del chat de IA depende de la configuración de su organización y de sus permisos. Si no aparece el botón **[!UICONTROL Charla de IA]**, la característica no está habilitada para su cuenta.

## Fuentes de datos

AI Chat puede utilizar estas fuentes:

* El manual de su organización en [Centro de conocimientos](admin-settings.md#knowledge-center).
* Su CRM conectado, incluidos posibles clientes, contactos, cuentas, oportunidades y actividades.
* [!DNL Marketo] datos de actividad y participación.
* Investigación de cuentas y noticias recientes recopiladas por Account Qualification Agent.
* Investigación web pública.

## Uso del chat de IA

Utilice el chat de IA para estos tipos de tareas:

* **Investigue y resuma**: pida un resumen de una cuenta, un grupo comprador o la participación reciente de un posible cliente.
* **Posicionamiento de compilación**: pídale al asistente que coloque la solución para una cuenta específica antes de una reunión.
* **Borrador y alcance refinado**: pídale que escriba o vuelva a escribir un correo electrónico. Especifique el tono, la longitud, el idioma y si desea incluir los emojis.
* **Obtener recomendaciones**: Pregunte a qué clientes potenciales o cuentas priorizar o solicite un objetivo o cadencia para un nuevo flujo de trabajo saliente.
* **Buscar detalles de contacto**: pídale al asistente que enriquezca a un posible cliente con más información de contacto y antecedentes.

## Consulte AI Chat en sus datos conectados

El chat de IA puede responder a preguntas sobre los datos de inteligencia de su empresa, [!DNL Marketo Qualifier], CRM, [!DNL Marketo], [!DNL Marketo Optimizer] y. Haga una pregunta en lenguaje sencillo para buscar información o recuperar contexto. Estas búsquedas de datos conectados leen los datos e informan sobre ellos; no crean, editan ni inician programas o campañas.

A continuación se muestran algunos ejemplos de indicadores. Cuanto más específico sea en el mensaje, más centrados estarán los resultados.

Perspectivas y cuentas:

* &quot;Encuentre clientes potenciales con estado de participación Nuevo&quot;.
* &quot;Investigue la empresa Adobe&quot;.
* &quot;Dame el perfil completo para un cliente potencial&quot;.
* &quot;Mostrar rendimiento saliente durante los últimos 30 días&quot;.
* &quot;Enumerar las reuniones reservadas de los últimos 30 días.&quot;

Centro de conocimientos:

* &quot;¿Qué garantía hay disponible para gestionar las objeciones de precios?&quot;
* &quot;¿Cuáles son los diferenciadores clave frente a los competidores?&quot;
* &quot;Enumerar documentos en el Centro de conocimientos&quot;.
* &quot;Resumir un documento&quot;.

CRM:

* &quot;Enumerar las oportunidades abiertas&quot;.
* &quot;Enumerar los cinco primeros posibles clientes con nombre y correo electrónico&quot;.
* &quot;Mostrar las actividades de ventas de un posible cliente o una cuenta&quot;.

[!DNL Marketo]:

* &quot;Examinar mis campañas inteligentes&quot;.
* &quot;Obtener la lista inteligente denominada &#39;Adquirido&#39;&quot;.
* &quot;Examine mis programas o consiga un programa por su nombre&quot;.
* &quot;Enumerar [!DNL Marketo] tipos de actividades.&quot;

[!DNL Adobe Journey Optimizer B2B Edition]:

* &quot;¿Cuántos recorridos tengo?&quot;
* &quot;¿Cómo segmenta el usuario mi audiencia?&quot;
* &quot;¿Qué páginas de aterrizaje existen en mi cuenta?&quot;
* &quot;¿Qué campos de plomo alimentan la puntuación?&quot;

Inteligencia de la empresa:

* &quot;¿Qué tecnologías utiliza una empresa?&quot;
* &quot;Mostrar noticias recientes para una empresa&quot;.
* &quot;Buscar compañías similares a una compañía determinada.&quot;
* &quot;Enumerar las ofertas de empleo abiertas para una empresa&quot;.

### Alcance y límites actuales

* Las búsquedas de datos conectadas leen sus datos e informan sobre ellos. No crean un programa, inician una campaña ni editan un registro CRM.
* En [Audiencia inteligente (Beta)](smart-audience.md), el chat admite acciones en la lista de audiencias, como guardar una lista, agregar columnas de información, filtrar y priorizar cuentas y posibles clientes, y agregar posibles clientes seleccionados a un flujo de trabajo saliente existente. Esto no escribe en CRM ni reemplaza la revisión y aprobación por correo electrónico.
* AI Chat busca información; no es una herramienta de creación de informes. No genera análisis ni tendencias del estilo [!DNL Marketo] a lo largo del tiempo, como el estado del correo electrónico del trimestre o una lista de posibles clientes creados en los últimos 10 días. Use los informes [!DNL Marketo] nativos para estas tareas.

## Respuestas básicas en su guía de estrategias

Para usar tu manual de [Centro de conocimientos](admin-settings.md#knowledge-center), consulta el Centro de conocimientos en tu pregunta. Por ejemplo:

`From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

La respuesta refleja los mensajes del manual de implementación.

## Proporcionar comentarios sobre las respuestas

Valore el contenido generado con los controles de miniaturas hacia arriba o hacia abajo. Sus comentarios ayudan a mejorar las respuestas futuras.

## Revisar respuestas de IA

Las respuestas generadas por IA pueden ser inexactas. Revise todo el contenido antes de utilizarlo.

* Compruebe los hechos, los nombres y las cifras antes de confiar en ellos.
* Lea cuidadosamente los correos electrónicos redactados y personalícelos antes de enviarlos.
* Utilice la salida del asistente como punto de partida, no como resultado final.

Los términos de IA generativa de Adobe rigen el uso de AI Chat por parte de su organización.

>[!MORELIKETHIS]
>
>* [Centro de conocimientos](admin-settings.md#knowledge-center)
>* [Cuentas](accounts.md)
>* [Flujos de trabajo salientes](outbound-workflows.md)
