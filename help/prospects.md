---
title: Clientes potenciales en [!DNL Adobe Marketo Qualifier]
description: Obtenga información sobre cómo crear su lista de clientes potenciales desde CRM, fuentes importadas y agregadas manualmente, filtrar clientes potenciales y revisar los detalles del cliente potencial en [!DNL Adobe Marketo Qualifier].
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Sales Qualifier
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 1%
---

# Clientes potenciales

Para ver los posibles clientes y contactos a los que puede acceder, seleccione **[!UICONTROL Clientes potenciales]** en el panel de navegación izquierdo. Utilice la lista para revisar el estado y la actividad más reciente de cada posible cliente.

![Tabla de clientes potenciales que muestra el estado del posible cliente y la última actividad para la administración de clientes potenciales](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Posibles clientes]** posibles clientes asignados a usted en el CRM conectado.
* **[!UICONTROL Contactos]** Contactos asignados a usted en el CRM conectado, con su cuenta asociada. Los datos de contacto también incluyen el nombre del propietario. Estos detalles están disponibles para Salesforce y Microsoft Dynamics 365.
* **[!UICONTROL Aspectos destacados del marketing]**: clientes potenciales con actividad de Marketo en directo, como aperturas de correos electrónicos o clics.
* **[!UICONTROL Lista de personas]** clientes potenciales que se importan o agregan manualmente.

## Revisar el contexto del cliente potencial y exportar la lista

La lista de clientes potenciales resume si hay un contexto adicional disponible para una divulgación personalizada. Un resumen encima de la lista muestra el número de clientes potenciales en cada estado y la columna de contexto muestra el estado de cada cliente potencial:

* **[!UICONTROL Aplicado]** El contexto disponible se aplicó al cliente potencial.
* **[!UICONTROL Parcial]**: solo se aplicó parte del contexto disponible.
* **[!UICONTROL Falta]** No hay contexto adicional disponible.

Para descargar la lista de clientes potenciales actual como archivo CSV, seleccione **[!UICONTROL Exportar CSV]**.

## Crear su lista de clientes potenciales

La lista de clientes potenciales combina personas de más de una fuente:

* **clientes potenciales de CRM**—[!DNL Adobe Marketo Qualifier] importan automáticamente los posibles clientes y contactos asignados al usuario conectado. Consulte [Integraciones](integrations.md).
* **Clientes potenciales importados**: clientes potenciales importados desde un archivo CSV.
* **Perspectivas agregadas manualmente**: Perspectivas individuales agregadas en Marketo Qualifier.

Para agregar clientes potenciales que no provienen de su CRM:

1. En la página **[!UICONTROL Posibles clientes]**, seleccione **[!UICONTROL Lista de personas]**.

   ![Lista de personas](assets/prospects-people-list.png){width="800" zoomable="yes"}

1. Seleccione **[!UICONTROL + Agregar personas]**, luego seleccione **[!UICONTROL Importar CSV]** o **[!UICONTROL Agregar persona]**.

   * Para una importación de CSV, cargue un CSV en formato `firstname,email`.
     El nombre y el correo electrónico son obligatorios. El apellido es opcional. La plantilla CSV no incluye la columna ID de posible cliente de CRM, pero puede agregar la columna y sus valores al archivo antes de la importación. Si la importación falla, revise el mensaje de error de los campos o valores para corregirlos y, a continuación, cargue el archivo de nuevo.
     Asigne cualquier campo CSV personalizado o adicional, no solo los estándar. Marketo Qualifier guarda estos valores en cada posible cliente y los pone a disposición más adelante, incluso para la [generación de correo electrónico](outbound-workflows.md#step-5-add-prospects-and-start-email-generation).
   * Para añadir a una persona manualmente, introduzca sus detalles en el formulario.

1. Seleccione **[!UICONTROL Guardar]**.

## Filtrado y búsqueda de clientes potenciales

Para reducir la lista, seleccione **[!UICONTROL Filtro]**. Puede filtrar por:

* Estado de flujo de trabajo saliente
* Creado por
* Cargo
* Cuenta
* Origen
* Última actualización

Los administradores también pueden hacer que los campos CRM asignados estén disponibles como filtros. En **[!UICONTROL Configuración de administración]**, active **[!UICONTROL Filtrable]** para cada campo que los usuarios usen para encontrar clientes potenciales. Ver [Asignar campos CRM](integrations.md#map-crm-fields-inbound-mapping).

En **[!UICONTROL Mis contactos de oportunidad]**, también puede filtrar contactos por campos de sus oportunidades asociadas, como escenario, tipo y fecha de cierre. Los campos de oportunidad tienen etiquetas como **[!UICONTROL Stage (Opportunity)]**, que los distingue de los campos de contacto. El administrador controla qué campos de oportunidad están disponibles como filtros.

También puede filtrar contactos por campos desde su cuenta asociada, como sector, región o tipo de cuenta. El administrador elige qué campos de cuenta se pueden filtrar. Combine filtros de cuenta, contacto y oportunidad para buscar, por ejemplo, contactos con una función específica en cuentas de un sector específico. El filtrado de campos de cuenta está disponible para Salesforce y Microsoft Dynamics 365, y se pueden usar los mismos campos en [Segmentación de flujos de trabajo salientes](outbound-workflows.md#step-2-configure-targeting-filters).

### Filtrar por aspectos destacados de marketing

Revise y dé prioridad a los posibles clientes por su participación de [!DNL Marketo] activa, como la actividad de correo electrónico, las visitas web y los rellenos de formulario. El compromiso aparece en tiempo casi real, a medida que sucede.

Para filtrar posibles clientes por Aspectos destacados de marketing:

1. Seleccione **[!UICONTROL Filtro]**.
1. Agregue un filtro de Elementos destacados de marketing y establezca el tipo de actividad, la campaña u otros atributos para que se centren en la participación que importa.

Cada posible cliente muestra su última actividad [!DNL Marketo] junto con el historial reciente.

Marketing Highlights está disponible en todas las regiones de producción. Un administrador completa una configuración única que conecta a [!DNL Marketo] con Marketo Qualifier. Ver [Configurar aspectos destacados de marketing](integrations.md#turn-on-marketo-engagement-filtering).

## Revisar detalles del cliente potencial

Para abrir el perfil de un cliente potencial, seleccione el cliente potencial. Revise las señales que importan antes de ponerse en contacto con:

* **Resumen de persona de IA**: instantánea escrita por IA del posible cliente o contacto y su participación reciente. Utilice el resumen para comprender a la persona rápidamente antes de revisar las actividades individuales. Los resúmenes personales de IA están disponibles en las instancias que ejecutan [!DNL Marketo Optimizer] Prime o Ultimate.
* **Lista de actividades**: una lista cronológica que muestra los últimos 90 días de actividad de marketing.
* **Vista de escala de tiempo**: una escala de tiempo visual que muestra los últimos 90 días de participación de marketing en todos los canales.
* **Contenido visto**: páginas web y recursos que el cliente potencial vio. Para abrir un elemento, selecciónelo.

### Generar preparación de reunión

Además del resumen de la persona de IA permanente, puede generar una preparación de reunión adaptada a una llamada específica desde la pestaña **[!UICONTROL Investigación de la reunión]**, junto a **[!UICONTROL Investigación de la cuenta]**.

La preparación para la reunión combina la investigación web sobre el cliente potencial y su compañía con la evidencia de estudios de casos sobre clientes de igual a igual que utilizan el producto que está vendiendo. Los puntos de conversación del caso práctico pueden incluir resultados medibles para los clientes. Las fuentes se combinan en un solo resumen, con puntos de conversación clasificados por relevancia. Cada tema de conversación identifica si proviene de estudios de casos, investigación web o ambos. Si no hay evidencia relevante de estudio de caso disponible, la preparación de la reunión utiliza la investigación web.

* **Basado en objetivos**: si el cliente potencial está inscrito en un flujo de trabajo saliente en ejecución, selecciónelo. La preparación se alinea con el objetivo de ese flujo de trabajo saliente, como reservar una reunión o volver a atraer al posible cliente.
* **Mensaje personalizado**: escriba para qué desea prepararse, por ejemplo `Focus on renewal risk` o `Prepare for a technical deep dive with their IT lead`. La preparación coincide con el mensaje. La opción de mensaje personalizado está disponible siempre que el cliente potencial no esté en un flujo de trabajo saliente en ejecución.

La información sigue la meta del flujo de trabajo saliente o la petición de datos personalizada que elija. La forma de generar la preparación de la reunión no cambia.

>[!MORELIKETHIS]
>
>* [Cuentas](accounts.md)
>* [Flujos de trabajo salientes](outbound-workflows.md)
>* [Chat de IA](ai-assistant.md)
