---
title: Configurar aspectos destacados de marketing
description: Aprenda a enviar posibles clientes desde Marketo Engage a Marketo Qualifier mediante un paso de flujo de campaña inteligente y obtenga recomendaciones de aspectos destacados de marketing para su revisión.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
subfeature_v2:
  - id: 7b0925d9-0dc0-5c75-a54d-2bcc31c6ebe4
    internal-label: Marketing highlights
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: adcfe279f38ca319589612820351c48af750bad9
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 2%
---

# Configurar aspectos destacados de marketing

Envíe posibles clientes de [!DNL Adobe Marketo Engage] a [!DNL Adobe Marketo Qualifier] agregando el paso de flujo **[!UICONTROL Enviar a Marketo Qualifier]** a una campaña inteligente. Los representantes verán los posibles clientes y la actividad que los envió en **[!UICONTROL Posibles clientes]** > **[!UICONTROL Aspectos destacados del marketing]**.

El paso de flujo funciona con ambos tipos de campañas inteligentes:

* **Las campañas de Déclencheur** envían participación a medida que se producen, como aperturas y clics en correos electrónicos, clics en vínculos, rellenos de formularios y visitas a páginas web.
* **Campañas por lotes** envían los posibles clientes aptos cada vez que se ejecuta la campaña.

Cuando un posible cliente coincide con los criterios de segmentación de un flujo de trabajo saliente, Marketo Qualifier recomienda el posible cliente a su propietario en el CRM conectado. El representante propietario revisa y aprueba el posible cliente antes de la inscripción y el contacto. Los posibles clientes no se inscriben automáticamente.

Marketing Highlights está disponible en todas las regiones de producción: Norteamérica, EMEA y Australia.

## Antes de empezar {#before-you-begin}

Confirme estos requisitos previos antes de agregar el paso de flujo:

* Un administrador de Marketo ha activado **[!UICONTROL Enviar a Marketo Qualifier]** para su instancia de Marketo Engage en **[!UICONTROL Administrador]**.
* Marketo Qualifier está [conectado a Salesforce o Microsoft Dynamics 365](getting-started.md#connect-your-crm), por lo que cada posible cliente puede coincidir con su propietario de CRM.

>[!IMPORTANT]
>
>El paso de flujo **[!UICONTROL Enviar a Marketo Qualifier]** no requiere credenciales de webhook, extremo de URL o API. No necesita acceder a Adobe Developer Console para utilizarlo. Si el paso de flujo no está disponible, póngase en contacto con el administrador de Marketo.

## Envío de posibles clientes con una campaña inteligente {#send-leads-with-a-smart-campaign}

Utilice una campaña inteligente existente o cree una para los posibles clientes y las actividades que desee enviar.

1. En Marketo Engage, abra una campaña inteligente o seleccione **[!UICONTROL Actividades de marketing]** > **[!UICONTROL Nueva]** > **[!UICONTROL Campaña inteligente]** para crear una.
1. En la ficha **[!UICONTROL Lista inteligente]**, defina qué posibles clientes cumplen los requisitos.

   * Para una campaña de déclencheur, agregue déclencheur para las actividades que desee enviar, como **[!UICONTROL Visitas la página web]**, **[!UICONTROL Clics en el vínculo de la página web]** o **[!UICONTROL Clics en el vínculo del correo electrónico]**.
   * Para una campaña por lotes, añada filtros para los posibles clientes que desee enviar.

1. En la ficha **[!UICONTROL Flujo]**, agregue el paso de flujo **[!UICONTROL Enviar a Marketo Qualifier]**.
1. Active la campaña de déclencheur o ejecute o programe la campaña por lotes.
1. En Marketo Qualifier, abra **[!UICONTROL Posibles clientes]** > **[!UICONTROL Aspectos destacados del marketing]** para revisar los posibles clientes y su actividad.

   La actividad muestra cómo llegó un posible cliente, por ejemplo **[!UICONTROL Se agregó desde la campaña por lotes]**.

Los posibles clientes que coinciden con los criterios de segmentación de un flujo de trabajo saliente solo se recomiendan a su propietario de CRM. Para revisar las recomendaciones, abra **[!UICONTROL Tareas]** > **[!UICONTROL Sugerencias del agente]**. Ver [Obtener recomendaciones de aspectos destacados del marketing](outbound-workflows.md#automatically-enroll-prospects-from-marketing-highlights) y [sugerencias de agentes](tasks.md#agent-suggestions).

## Configuraciones de webhook existentes {#existing-webhook-setups}

Las siguientes instrucciones describen la configuración anterior del webhook. No son necesarios para el paso de flujo **[!UICONTROL Enviar a Marketo Qualifier]**. Si su organización ya utiliza un gancho web, trabaje con el administrador de Marketo y con el contacto de Adobe antes de cambiar esa configuración.

+++Instrucciones de configuración de Webhook

Estas instrucciones requieren acceso a Adobe Developer Console y a **[!UICONTROL Admin]** en Marketo Engage.

### Parte A: Creación de credenciales de API {#part-a-create-api-credentials}

Estas credenciales permiten que [!DNL Marketo] se autentique de forma segura en Marketo Qualifier.

Para crear las credenciales:

1. Vaya a la [consola de desarrollador de Adobe](https://developer.adobe.com/console/) e inicie sesión con su Adobe ID.
1. Seleccione **[!UICONTROL Crear nuevo proyecto]** o abra un proyecto existente.
1. Para cambiar el nombre del proyecto, selecciona **[!UICONTROL Editar proyecto]**, escribe un nombre identificable como `Marketo Qualifier Marketing Highlights` y selecciona **[!UICONTROL Guardar]**.
1. Seleccione **[!UICONTROL Agregar API]**, seleccione **[!UICONTROL API de Experience Platform]** y, a continuación, seleccione **[!UICONTROL Siguiente]**.
1. Elija **[!UICONTROL Servidor a servidor OAuth]** como tipo de autenticación y, a continuación, seleccione **[!UICONTROL Siguiente]**.

   **[!UICONTROL OAuth Server-to-Server]** permite que [!DNL Marketo] llame a la API de Marketo Qualifier directamente desde su servidor, sin que sea necesario que una persona inicie sesión.

1. Escriba un nombre de credencial de 45 caracteres o menos, como `Marketo Qualifier Marketing Highlights Creds`.
1. Para asociar el perfil de producto, selecciónelo y después seleccione **[!UICONTROL Guardar la API configurada]**.
1. En **[!UICONTROL Credenciales conectadas]**, abra la credencial **[!UICONTROL Servidor a servidor OAuth]**. Seleccione **[!UICONTROL Recuperar secreto de cliente]** y copie el **[!UICONTROL ID de cliente]** y el **[!UICONTROL Secreto de cliente]**. Estos valores se usan en [Parte C](#part-c-configure-the-marketo-webhook).

>[!WARNING]
>
>Mantenga el secreto del cliente en privado. Trátela como una contraseña y no la envíe por correo electrónico. Utilice el canal seguro aprobado de su organización para compartirlo con quien configure el webhook.

### Parte B: Recopilar el punto final y los identificadores {#part-b-gather-your-endpoint-and-identifiers}

Necesita tres valores para [Parte C](#part-c-configure-the-marketo-webhook):

* **URL de extremo**: la dirección del webhook de Marketo Qualifier para su región.
* **imsOrg ID**: el identificador de su organización en Adobe Identity Management System (IMS), con el formato `{ORG_ID}@AdobeOrg`.
* **Nombre de zona protegida**: El nombre de la zona protegida de AEP exactamente como aparece en la dirección URL de Marketo Qualifier (el valor `sname`), no el nombre para mostrar mostrado en la interfaz de usuario. Utilice el valor de URL en minúsculas, por ejemplo `prod`, no `Prod`.

| Región | URL de extremo de webhook |
| --- | --- |
| América del Norte | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| EMEA | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| Asia-Pacífico/Australia | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

Si no está seguro de su región, ID de imsOrg o nombre de la zona protegida, su contacto de Adobe puede confirmarlos.

### Parte C: Configuración del webhook de Marketo {#part-c-configure-the-marketo-webhook}

Para crear el webhook:

1. En [!DNL Marketo], seleccione **[!UICONTROL Administrador]** > **[!UICONTROL Webhooks]**.
1. Seleccione **[!UICONTROL Nuevo webhook]**.
1. Establece **[!UICONTROL URL]** a la URL de punto final para tu región desde [Parte B](#part-b-gather-your-endpoint-and-identifiers).
1. Establecer **[!UICONTROL tipo de solicitud]** en `POST`.
1. Establezca la codificación de token de solicitud **[!UICONTROL 1} en `JSON`.]** Esta configuración es obligatoria.
1. Pegue la plantilla de carga útil siguiente en **[!UICONTROL Template]**. Use **[!UICONTROL Insertar token]** de [!DNL Marketo] para que coincidan con los nombres de campo de su instancia.

   >[!NOTE]
   >
   >Con la codificación JSON, no ajuste los tokens de cadena entre comillas. [!DNL Marketo] los agrega automáticamente.

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. Seleccione **[!UICONTROL Acciones de webhook]** > **[!UICONTROL Definir encabezado personalizado]** y, a continuación, agregue los siguientes encabezados, utilizando los valores de [Parte A](#part-a-create-api-credentials) y [Parte B](#part-b-gather-your-endpoint-and-identifiers):

   | Encabezado | Valor |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | Su ID de cliente |
   | `x-client-secret` | Secreto de cliente |
   | `x-gw-ims-org-id` | Su ID de imsOrg |
   | `x-sandbox-name` | Nombre de la zona protegida |

   {style="table-layout:auto"}

1. Seleccione **[!UICONTROL Guardar]**.

### Parte D: Agregar el webhook a una campaña inteligente de déclencheur {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

Agregue un paso de flujo **[!UICONTROL Llamar al webhook]** a una campaña inteligente de déclencheur, ya sea una existente o una nueva. Los déclencheur de listas inteligentes de esa campaña deciden qué actividades se envían a Marketo Qualifier.

Para agregar el webhook:

1. Abra una campaña inteligente de déclencheur existente o cree una nueva (**[!UICONTROL Actividades de marketing]** > **[!UICONTROL Nueva]** > **[!UICONTROL Campaña inteligente]**).
1. En la ficha **[!UICONTROL Lista inteligente]**, agregue el déclencheur o los déclencheur de las actividades que desee enviar; por ejemplo, **[!UICONTROL Hace clic en el vínculo del correo electrónico]**, **[!UICONTROL Rellena el formulario]** o **[!UICONTROL Visita la página web]**.
1. En la ficha **[!UICONTROL Flujo]**, agregue un paso **[!UICONTROL Llamar al webhook]** y seleccione el webhook que creó en [Parte C](#part-c-configure-the-marketo-webhook).
1. Active la campaña inteligente.

La actividad de esa campaña inteligente ahora fluye a Marketo Qualifier. Los representantes ven y filtran esta actividad en **[!UICONTROL Prospects]** > **[!UICONTROL Marketing Highlights]**.

+++

>[!MORELIKETHIS]
>
>* [Administrar integraciones](integrations.md)
>* [Clientes potenciales](prospects.md)
>* [Introducción](getting-started.md)
