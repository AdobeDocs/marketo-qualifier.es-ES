---
title: Configuración de administración
description: Obtenga información sobre cómo administrar campos CRM, sincronización de actividades, exclusión de correo electrónico y otras configuraciones de administración de [!DNL Adobe Marketo Qualifier].
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
internal-label: Administration
autotag-review: '2026-10-08T17:58:28.029Z'
TQID: 'https://experienceleague.adobe.com/2eccZWj1XY7qP20n6GcnBe6PZwNkp0ALhZfOhljwZF8'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: f8f8b877-7295-5853-989f-e21f73bc94c4
    internal-label: Administration
  - id: ace0d1fc-8e69-4e6a-a442-37fc40985eea
    internal-label: Account Qualification Agent
subfeature_v2:
  - id: bdb3c167-3513-52b9-948f-cab8397ca360
    internal-label: Knowledge center
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ab54d20ccc80d88c3592d89c9f43feeb062ed82c
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%
---

# Configuración de administración

Use **[!UICONTROL Configuración de administración]** para configurar integraciones de CRM, administrar el Centro de conocimiento y configurar la exclusión de correo electrónico.

[!DNL Adobe Marketo Qualifier] se conecta a Salesforce o Microsoft Dynamics 365. La conexión proporciona a Account Qualification Agent (AQA) una vista coherente de los posibles clientes, las cuentas, los contactos, las actividades y los propietarios. Marketo Qualifier también puede escribir actividades de divulgación y estados de exclusión en CRM y sincronizar las actividades de divulgación con Marketo.

Para configurar las conexiones de CRM, la asignación de campos y la sincronización de actividades, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Configuración de administración]** > **[!UICONTROL Conexiones de CRM]**. Los usuarios estándar pueden utilizar los datos y filtros de CRM configurados, pero no pueden cambiar esta configuración. Para conectar un CRM por primera vez, consulte [Introducción](getting-started.md#connect-your-crm).

>[!IMPORTANT]
>
>El acceso a **[!UICONTROL Configuración de administración]** requiere la pertenencia a los grupos de usuarios `Marketo Qualifier` y `Marketo Qualifier Admins`.

## CRM MCP y el complemento incrustado

Marketo Qualifier trabaja con su CRM de las siguientes maneras:

* **CRM MCP queries**: Account Qualification Agent consulta datos de CRM activos para que las respuestas y perspectivas reflejen el estado actual de sus registros.
* **Complemento incrustado**: el complemento CRM muestra [!DNL Marketo Sales Insights] (MSI) datos y datos auténticos en su CRM. Use el complemento para agregar un cliente potencial a [!DNL Marketo Qualifier].
* **Sincronización de actividades**: cuando un administrador activa **[!UICONTROL Sincronización de actividades]**, las actividades de alcance se sincronizan con CRM y Marketo.

### Priorizar posibles clientes en el complemento CRM

El complemento CRM proporciona un inicio predeterminado en el que los representantes pueden priorizar los posibles clientes sin salir de CRM. Las pestañas disponibles organizan el trabajo por origen e intención:

* **[!UICONTROL Más probables]**: recomendaciones de posibles clientes listas para la acción.
* **[!UICONTROL Mi lista de seguimiento]**: posibles clientes a los que está realizando un seguimiento.
* **[!UICONTROL Actividad web]**: visitas recientes al sitio de posibles clientes conocidos.
* **[!UICONTROL Actividad web anónima]**: visitas de visitantes no identificados.
* **[!UICONTROL Mi correo electrónico]**: participación por correo electrónico asociada con sus posibles clientes.
* **[!UICONTROL Seminario web]**: actividad de registro y asistencia al seminario web.

Cada posible cliente puede incluir una vista previa del correo electrónico [!DNL Marketo], un vínculo a los detalles del posible cliente e investigación de LinkedIn. Las pestañas y los datos a los que puede acceder dependen de la configuración del complemento CRM.

## Ámbito de acceso CRM

Marketo Qualifier lee usuarios, contactos, asignaciones de propietarios, posibles clientes, cuentas, oportunidades y actividades desde CRM. Solo escribe las actividades de divulgación registradas y el estado de exclusión en CRM, y sincroniza las actividades de divulgación con Marketo. El administrador de CRM prepara el acceso a la API en Salesforce o Dynamics. A continuación, un administrador de Marketo Qualifier conecta el CRM, asigna campos de entrada y elige si desea sincronizar las actividades.

>[!NOTE]
>
>Los pasos de credenciales en [Introducción](getting-started.md#connect-your-crm) describen el acceso de lectura a objetos CRM. Si activa la sincronización de actividades o la reescritura de exclusión, trabaje con su administrador de CRM para conceder el acceso de escritura correspondiente requerido por su configuración de CRM.

## Asignar campos CRM (asignación de entrada)

Una vez conectado el CRM, seleccione **[!UICONTROL Administrar]** para la conexión y abra **[!UICONTROL Asignación entrante]**. La asignación de entrada controla qué campos CRM extrae Marketo Qualifier en la aplicación.

1. Seleccione **[!UICONTROL Agregar sección]**.
1. Introduzca un nombre de sección y una descripción.
1. Seleccione un tipo de entidad. **[!UICONTROL Clientes potenciales]** está seleccionado de forma predeterminada. También están disponibles **[!UICONTROL Contactos]**, **[!UICONTROL Cuentas]** y **[!UICONTROL Oportunidades]**.
1. Para importar campos de CRM, seleccione los campos.

   Cada fila de campo muestra su **[!UICONTROL nombre para mostrar]**, **[!UICONTROL nombre de campo]** y **[!UICONTROL tipo de datos]**.

1. Active **[!UICONTROL Filtrable]** para cada campo de cliente potencial, contacto, cuenta u oportunidad que desee poner a disposición como filtro en la lista de **[!UICONTROL clientes potenciales]** y en [Segmentación de flujo de trabajo saliente](outbound-workflows.md#step-2-configure-targeting-filters).
1. Previsualice la sección y seleccione **[!UICONTROL Agregar]**.

Los campos asignados aparecen en las áreas correspondientes de Marketo Qualifier:

* Los campos de clientes potenciales aparecen en la ficha **[!UICONTROL Persona]**.
* Los campos de cuenta aparecen en la ficha **[!UICONTROL Cuenta]**. En una sección con el tipo de entidad **[!UICONTROL Cuentas]**, haga que los campos sean filtrables para que los representantes puedan filtrar los contactos por los atributos de su cuenta asociada, como sector, región o tipo de cuenta.
* Los campos de oportunidad aparecen en la sección **[!UICONTROL Oportunidad de cuenta]**. Los campos de oportunidad que se pueden filtrar también aparecen como sus propias columnas en **[!UICONTROL Mis contactos de oportunidad]**, con etiquetas como **[!UICONTROL Etapa (oportunidad)]** para distinguirlos de los campos de contacto.

El filtrado de campos de cuenta está disponible para Salesforce y Microsoft Dynamics 365. Los representantes pueden combinar los campos filtrables de cuenta, contacto y oportunidad para encontrar contactos y definir los criterios de segmentación del flujo de trabajo saliente.

## Configuración de la sincronización de actividades (asignación saliente)

1. De **[!UICONTROL conexiones CRM]**, seleccione **[!UICONTROL Administrar]** para el CRM conectado.
1. Abrir **[!UICONTROL asignación saliente]**.
1. Active **[!UICONTROL Sincronización de actividades]** para sincronizar las actividades de Marketo Qualifier con CRM y Marketo.

Cuando la sincronización de actividades está desactivada, Marketo Qualifier sigue utilizando datos CRM entrantes, pero no sincroniza las actividades de divulgación con su CRM o Marketo.

## Configurar reglas de sincronización de CRM

Marketo Qualifier puede escribir las actualizaciones de estado de los posibles clientes en Salesforce y Microsoft Dynamics automáticamente a medida que un posible cliente avanza a través de un flujo de trabajo saliente, de modo que los representantes ya no actualicen el CRM manualmente.

### Qué hacen las reglas de sincronización CRM

Una actualización puede dirigirse al registro **[!UICONTROL Posible cliente]**, **[!UICONTROL Contacto]**, **[!UICONTROL Cuenta]** o **[!UICONTROL Oportunidad]**, no solo al posible cliente.

Las actualizaciones se activan en estos momentos del flujo de trabajo saliente:

* Se agrega a un flujo de trabajo, se responde o se reserva una reunión
* Eliminado por un representante o flujo de trabajo completado sin respuesta
* Exclusión o correo electrónico devuelto

Los valores de campo se pueden personalizar con tokens dinámicos para que la actualización de CRM refleje los recorridos reales del cliente potencial en lugar de un valor estático. Los tokens están disponibles para obtener detalles como el nombre del representante, el nombre del flujo de trabajo saliente y la fecha y hora de la reunión.

Solo se escriben valores compatibles con CRM, un campo con error no bloquea los demás y los problemas temporales se reintentan automáticamente. Se realiza un seguimiento de cada actualización para poder ver qué se sincroniza y qué necesita atención.

### Configurar reglas de sincronización de CRM

Para configurar las reglas de sincronización de CRM:

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Configuración de administración]** > **[!UICONTROL Conexiones CRM]**.
1. Seleccione **[!UICONTROL Administrar]** para el CRM conectado, luego seleccione **[!UICONTROL Reglas de sincronización]**.
1. Elija la entidad y los campos de CRM de destino, asígnelos al flujo de trabajo momentos antes y active la opción.

Con las reglas de sincronización de CRM configuradas, los equipos de ventas ven un estado preciso, personalizado y actualizado en todos los posibles clientes, contactos, cuentas y oportunidades en cada fase, con menos retraso de datos y trabajo manual.

## Creación de un manual de centro de conocimiento {#knowledge-center}

El **[!UICONTROL Centro de conocimientos]** proporciona a Account Qualification Agent (AQA) acceso a sus materiales de ventas. Marketo Qualifier utiliza estos materiales para generar investigaciones, perspectivas de cualificación y actividades de divulgación que reflejen las ventas de su organización. Solo los administradores pueden crear y administrar el manual de implementación.

![Centro de conocimientos](assets/knowledge-center.png){width="800" zoomable="yes"}

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración]**, seleccione **[!UICONTROL Configuración de administración]** y seleccione **[!UICONTROL Centro de conocimiento]**.
1. Establezca **[!UICONTROL Nombre de la compañía]** y **[!UICONTROL Dirección URL de la compañía]** que Marketo Qualifier usa para investigar su compañía y redactar correos electrónicos.
1. Cargar reproducciones de ventas, perfiles de cliente (ICP) ideales, guías de posicionamiento y otros materiales de promoción de ventas en formato PDF, PPTX o DOCX.
1. Seleccione **[!UICONTROL Generar libro de estrategias]**.

La página muestra el estado del último manual creado y proporciona la siguiente acción después de cargar contenido. Para recuperar el estado más reciente después de una compilación, seleccione **[!UICONTROL Actualizar]**.

Cada documento cargado también muestra su estado de procesamiento, como **[!UICONTROL Listo]**, y la última vez que se actualizó.

>[!NOTE]
>
>El procesamiento de un manual puede tardar hasta 24 horas.

Cuando el manual está listo, los representantes pueden utilizarlo en dos lugares:

* **Mensajes de correo electrónico salientes**: en un mensaje de punto de contacto, asigne un nombre al documento y describa el contexto que se va a utilizar. Por ejemplo, escriba `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Consulte [Configurar puntos de contacto](outbound-workflows.md#step-3-generate-and-review-touchpoints).
* **Chat de IA**: consulta el Centro de conocimiento en tu pregunta. Por ejemplo, escriba `From the Knowledge Center, help me position our security solution for ABC Corp before tomorrow's call`. Consulte [Chat de IA](ai-assistant.md).

En ambos casos, el contenido generado refleja la mensajería en su manual en lugar de la investigación genérica.

## Configuración de la exclusión de correo electrónico global

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Configuración de administración]**.
1. Seleccione **[!UICONTROL Configuración de correo electrónico]** en **[!UICONTROL Cumplimiento]**.
1. Active **[!UICONTROL Incluir vínculo de no participación en cada correo electrónico]** para anexar un pie de página de cancelación de suscripción a los correos electrónicos salientes.
1. En **[!UICONTROL Plantilla de mensaje de exclusión]**, escriba el texto del pie de página. Incluya el token `{opt_out_link}` donde debería aparecer el vínculo para cancelar la suscripción.

La configuración se guarda automáticamente.

Cuando un cliente potencial selecciona el vínculo, Marketo Qualifier deja de enviarle correos electrónicos y sincroniza el estado de exclusión con el CRM conectado. Marketo Qualifier también reconoce solicitudes claras de exclusión en la respuesta de correo electrónico de un cliente potencial, como &quot;por favor, deje de enviarme correos electrónicos&quot; o &quot;cancelar la suscripción&quot;, y marca al cliente potencial como excluido automáticamente. Se aplican el mismo estado **[!UICONTROL exclusión]** y el mismo distintivo, y no se envían más puntos de contacto. No se necesita ninguna configuración adicional. Las respuestas que no piden claramente detenerse, como &quot;no ahora mismo&quot;, no se tratan como exclusiones. Ver [solicitudes de exclusión en las respuestas](outbound-workflows.md#opt-out-requests-in-replies).

## Referencia: Parámetros de API de muestra

Su equipo de CRM puede utilizar estos ejemplos para confirmar que el acceso de lectura devuelve los campos de posibles clientes esperados.

### Ejemplo de OData de Dynamics

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

### Ejemplo de SOQL de Salesforce

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

>[!MORELIKETHIS]
>
>* [Introducción](getting-started.md)
>* [Clientes potenciales](prospects.md)
