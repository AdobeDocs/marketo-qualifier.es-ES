---
title: Configuración del complemento CRM
description: Obtenga información sobre cómo instalar el complemento Marketo Qualifier CRM en Salesforce o Microsoft Dynamics 365. Configure acciones de Salesforce para flujos de trabajo y campañas de Marketo.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
  - id: f8f8b877-7295-5853-989f-e21f73bc94c4
    internal-label: Administration
subfeature_v2:
  - id: d2fe5f36-5653-5902-937c-9d3026104284
    internal-label: CRM integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: df256cf271296b82fab2ed10725a0d6bd165e05b
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%
---

# Configuración del complemento CRM

Instale el complemento CRM [!DNL Adobe Marketo Qualifier] para que los representantes puedan utilizar [!DNL Marketo Sales Insights] y las perspectivas generadas por IA en las páginas de registro de cliente potencial, contacto y cuenta sin salir de Salesforce o Microsoft Dynamics 365. El complemento también proporciona una vista de inicio para [priorizar los posibles clientes en su CRM](admin-settings.md#prioritize-leads-in-the-crm-plugin).

En Salesforce, los representantes también pueden agregar clientes potenciales a flujos de trabajo salientes o campañas de Marketo desde las vistas de lista de contactos y posibles clientes y páginas de registro individuales.

## Antes de empezar

Asegúrese de que las personas que instalan y utilizan el complemento tengan el acceso necesario:

* **Administrador de Salesforce**: permiso para instalar paquetes y editar diseños de página.
* **Administrador de Microsoft Dynamics 365**: Permiso para importar soluciones en el entorno de destino en aplicaciones de energía.
* **Representantes**: acceso a Marketo Qualifier y a los registros CRM relevantes.

La instalación del complemento es independiente de [conectar su CRM a Marketo Qualifier](getting-started.md#connect-your-crm).

## Instalar en Salesforce

Instale el paquete y, a continuación, añada sus componentes a las páginas de registro que utilizan los representantes.

1. Abra la [página de instalación de Salesforce](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce) e inicie sesión en Salesforce como administrador.
1. En la página de instalación del paquete, seleccione **[!UICONTROL Instalar para todos los usuarios]** y, a continuación, seleccione **[!UICONTROL Instalar]**.

   Puede seguir controlando el acceso de los usuarios individuales mediante permisos de Salesforce.

1. Cuando se le pida que apruebe el acceso de terceros, active la casilla de verificación de aprobación y seleccione **[!UICONTROL Continuar]**.
1. Cuando finalice la instalación, seleccione **[!UICONTROL Listo]**.

   La instalación tarda unos minutos. Confirme que el paquete aparece en la página **[!UICONTROL Paquetes instalados]**.

1. En Lightning App Builder, edite las páginas de registro de cliente potencial, contacto y cuenta y añada los componentes de Marketo Qualifier.

### Agregar acciones a vistas de lista

Configure **[!UICONTROL Agregar a flujo de trabajo saliente]** y **[!UICONTROL Agregar a Marketo Campaign]** por separado para las vistas de lista de contactos y clientes potenciales. Utilice los botones incluidos en el paquete para evitar duplicados.

1. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Administrador de objetos]** y seleccione **[!UICONTROL Posible cliente]** o **[!UICONTROL Contacto]**.
1. Abra **[!UICONTROL Botones, vínculos y acciones]** y busque los botones de lista **[!UICONTROL AMQ Agregar al flujo de trabajo saliente]** y **[!UICONTROL AMQ Agregar a Marketo Campaign]**.
1. Abra el **[!UICONTROL diseño de botón de vista de lista]** del objeto y seleccione **[!UICONTROL Editar]**.

   Según la configuración de Salesforce, el diseño de vista de lista podría estar en **[!UICONTROL Diseños de búsqueda]** > **[!UICONTROL Vista de lista]**.

1. Mueva ambos botones de lista a **[!UICONTROL Botones seleccionados]** y guárdelos.
1. Repita el proceso para el otro objeto.

Los representantes seleccionan uno o varios registros en una vista de lista y, a continuación, seleccionan la acción.

### Agregar acciones a páginas de registro

Las acciones de página de registro deben configurarse por separado de los botones de vista de lista. Agregue ambas acciones a cada diseño de página de posible cliente y contacto en uso.

1. Vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Administrador de objetos]** y seleccione **[!UICONTROL Posible cliente]** o **[!UICONTROL Contacto]**.
1. Abra **[!UICONTROL Botones, vínculos y acciones]** y busque los botones de detalle **[!UICONTROL AMQ Agregar al flujo de trabajo saliente]** y **[!UICONTROL AMQ Agregar a Marketo Campaign]**.
1. Abra **[!UICONTROL Diseños de página]** y edite un diseño asignado a sus representantes.
1. Agregue ambos botones de detalle a **[!UICONTROL Salesforce Mobile y Acciones de experiencia de Lightning]** y guárdelos.
1. Repita el proceso para cada diseño aplicable y para el otro objeto.

Las acciones aparecen en la barra de acciones del registro o en su menú y se aplican al registro que se está viendo.

>[!NOTE]
>
>Estas acciones funcionan en Salesforce Lightning Experience de escritorio, no en la aplicación móvil de Salesforce. La sección de diseño **[!UICONTROL Salesforce Mobile y Lightning Experience Actions]** también se usa para las acciones de escritorio.

### Reemplazar un botón que falta

Si falta un botón empaquetado, cree un reemplazo bajo los **[!UICONTROL botones, vínculos y acciones]** del objeto.

1. Seleccionar **[!UICONTROL nuevo botón o vínculo]**.
1. Escriba una etiqueta para la acción, como `Add to Outbound Workflow` o `Add to Marketo Campaign`.
1. Elija **[!UICONTROL Botón de lista]** para una vista de lista o **[!UICONTROL Botón de página de detalles]** para una página de registro.
1. Establezca **[!UICONTROL Content Source]** en **[!UICONTROL Visualforce Page]** y elija la página de acción del paquete que coincida con la acción, el objeto y la ubicación.

   Las ubicaciones de lista de posibles clientes, detalles de posibles clientes, lista de contactos y detalles de contacto utilizan páginas diferentes. Confirme que la página seleccionada coincide con la ubicación que está configurando.

1. Para un botón de lista, seleccione **[!UICONTROL Requerir selección de fila]**.
1. Guarde el botón y agréguelo al diseño de botón de vista de lista adecuado o a las acciones de página de registro como se ha descrito anteriormente.

### Comprobación de acciones de Salesforce

Después de guardar los diseños, confirme que ambas acciones aparecen en las vistas de lista de contactos y clientes potenciales y en las páginas de registros. Pruebe cada acción de lista con los registros seleccionados y cada acción de página de registro de un registro individual.

Si una acción no está disponible o no se abre, utilice estas comprobaciones:

| Problema | Qué comprobar |
| --- | --- |
| Falta un botón en una vista de lista | Confirme que el botón de lista se encuentra en **[!UICONTROL Botones seleccionados]** en el **[!UICONTROL diseño de botón de vista de lista]** del objeto correcto y guarde el diseño. |
| Falta el botón en una página de registro | Confirme que el botón de detalles se encuentra en **[!UICONTROL Salesforce Mobile and Lightning Experience Actions]** en el diseño asignado al usuario. Si su organización utiliza Acciones dinámicas, compruebe también la visibilidad de la acción de la página de registro. |
| Opción de página esperada no disponible al crear un botón | Compruebe que el tipo de presentación sea **[!UICONTROL Botón de lista]** para una vista de lista o **[!UICONTROL Botón de página de detalles]** para una página de registro. |
| La acción no se abre o muestra un error de acceso | Confirme que el usuario tiene acceso a Marketo Qualifier y a los registros seleccionados. |

## Instalar en Microsoft Dynamics 365

Importe el paquete del complemento en el entorno en el que trabajan sus representantes.

1. Abra la [página de instalación de Microsoft Dynamics 365](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics) y descargue el archivo ZIP del paquete.
1. Inicie sesión en [Power Apps](https://make.powerapps.com/) como administrador y seleccione el entorno de destino.
1. Abra **[!UICONTROL Soluciones]** y seleccione **[!UICONTROL Importar solución]**.
1. Seleccione **[!UICONTROL Examinar]**, elija el archivo ZIP descargado y seleccione **[!UICONTROL Siguiente]**.
1. Revise los detalles del paquete y seleccione **[!UICONTROL Siguiente]**.
1. Mantenga el valor de variable de entorno rellenado previamente y seleccione **[!UICONTROL Importar]**.
1. Espere a que aparezca el mensaje de confirmación en la parte superior de la página que indica que la solución se importó correctamente.

La importación tarda unos minutos.

>[!MORELIKETHIS]
>
>* [Priorizar posibles clientes en el complemento CRM](admin-settings.md#prioritize-leads-in-the-crm-plugin)
>* [Integraciones](integrations.md)
>* [Introducción](getting-started.md)
