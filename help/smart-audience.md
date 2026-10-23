---
title: Audiencia inteligente (Beta)
description: Aprenda a utilizar la audiencia inteligente (Beta) para crear listas de cuentas, añadir datos de CRM y señales de crecimiento, priorizar posibles clientes y añadirlos a un flujo de trabajo saliente.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
badgeBeta: label="Beta" type="Informative"
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%
---

# Audiencia inteligente (Beta)

La audiencia inteligente (Beta) le ayuda a encontrar las cuentas y las personas que seguirán trabajando en [!DNL Adobe Marketo Qualifier]. Describa la audiencia en lenguaje sencillo, perfeccione la lista de cuentas con datos de CRM y señales de crecimiento, busque posibles clientes relevantes y añada los posibles clientes seleccionados a un flujo de trabajo saliente.

Trabaje en la vista de lista con su cuadrícula, filtros y botones, o utilice el gráfico para describir lo que desea. Ambos funcionan en la misma lista: los cambios en uno aparecen en el otro. Si no aparece un cambio de inmediato, seleccione **[!UICONTROL Actualizar]**.

El rastreador de progreso de la parte superior de cada lista muestra tres fases: **[!UICONTROL Crear lista de audiencia inteligente]**, **[!UICONTROL Priorizar posibles clientes]** y **[!UICONTROL Agregar a flujo de trabajo saliente]**.

## Antes de empezar

La audiencia inteligente requiere una Salesforce conectada o Microsoft Dynamics 365 CRM. Lee los datos de CRM activos y no escribe en CRM. Para obtener instrucciones de conexión, consulte [Introducción](getting-started.md#connect-your-crm).

Puede crear hasta 100 listas. Cada lista tiene hasta 500 cuentas y 2.000 posibles clientes. No se agregan cuentas o posibles clientes que sobrepasen estos límites. Limite los criterios o divida la audiencia en varias listas, por ejemplo, por región o segmento.

## Describir y previsualizar cuentas

Comience con una descripción de las cuentas a las que desee llegar. La vista previa no guarda una lista.

1. Abra **[!UICONTROL Audiencia inteligente]** y seleccione **[!UICONTROL Nueva audiencia inteligente]** o **[!UICONTROL Crear lista]**.
1. En el chat, describa las cuentas que desee. Por ejemplo, escriba `Find healthcare accounts with revenue over $50M`.
1. Revise el número de cuentas coincidentes y el ejemplo en la vista previa.

Su solicitud puede incluir estos criterios:

| Criterios | Ejemplos |
| --- | --- |
| Firmografía | Sector, recuento de empleados, ingresos anuales, tipo de cuenta y calificación |
| Ubicación | Región, país, estado o ciudad |
| Propiedad | Sus cuentas o cuentas asignadas a un propietario con nombre |
| En preparación | Cuentas con o sin oportunidad abierta, sujetas a los [límites de Salesforce](#current-scope-and-limits) |
| Detalles de la cuenta | Nombre, sitio web o dominio y número de cuenta |

Otras solicitudes de ejemplo incluyen:

* `Accounts in the US with more than 1000 employees`
* `My accounts in Germany or France`
* `Accounts with no open opportunity`

Si parte de una solicitud no se puede aplicar a los datos de CRM, el chat identifica la condición omitida. La vista previa refleja únicamente las condiciones aplicadas. Revise estas omisiones antes de guardar.

## Guardar o restringir la previsualización

Guarde la vista previa cuando coincida con la audiencia a la que va dirigida.

1. Para cambiar la vista previa, envíe una nueva solicitud con las condiciones que desee. No se guarda nada hasta que confirme la acción.
1. Cuando la previsualización esté lista, pida al chat que la guarde como lista y que le asigne un nombre.
1. Revise las cuentas guardadas en la ficha **[!UICONTROL Cuentas]**.

Puede cambiar el nombre de una lista desde su página. Para eliminar una lista, ábrala y seleccione **[!UICONTROL Eliminar lista de audiencias inteligentes]**.

>[!CAUTION]
>
>Al eliminar una lista, se eliminan permanentemente sus cuentas, posibles clientes y columnas de la audiencia inteligente. No elimina los registros CRM.

## Enriquecimiento y preselección de cuentas

Agregue columnas de información para decidir qué cuentas usar. Pida una columna o una señal por solicitud.

Para agregar información de CRM, escriba una solicitud como `Add a column showing which accounts have an open opportunity`. Vea [Ámbito y límites actuales](#current-scope-and-limits) para restricciones de Salesforce.

Para agregar señales de crecimiento, selecciona **[!UICONTROL Enriquecer cuentas]** en la vista de lista o pregunta en el chat. Las señales disponibles incluyen:

| Señal | Lo que muestra |
| --- | --- |
| Financiación | Financiación y eventos de financiación recientes |
| Contratación | Ofertas de empleo y demanda de contratación recientes |
| Señales de expansión | Nuevas oficinas, nuevos mercados y anuncios de expansión |
| Cambios tecnológicos | Adiciones y cambios en la pila tecnológica de una empresa |
| Despidos | Información de despido solicitada a través del chat |

Por ejemplo, escriba `Which of these accounts have raised funding recently?` o `Which of these accounts have had layoffs?`.

En listas grandes, agregar una señal puede tardar unos minutos. Siga el progreso mostrado en la lista, revise cada nueva columna y manténgala o deséchela.

Para reducir y priorizar las cuentas:

1. En la ficha **[!UICONTROL Cuentas]**, abra **[!UICONTROL Filtros]**.
1. Filtre por cuenta, dominio, sector, propietario, empleados mínimos o máximos, ingresos mínimos o máximos o columnas personalizadas. Las columnas personalizadas son las columnas CRM y de señal que ha agregado. Por ejemplo, filtre las cuentas donde la columna de contratación esté establecida en `Yes`.
1. De manera opcional, seleccione **[!UICONTROL Priorizar cuentas]** para clasificar las cuentas por puntuación.
1. Elimine las cuentas que no desee que funcionen.

Los filtros se guardan con la lista. Los posibles clientes solo se encuentran para las cuentas filtradas, por lo que debe configurar los filtros de cuenta antes de priorizar los posibles clientes.

## Buscar y priorizar posibles clientes

Encuentre personas relevantes en las cuentas que preseleccionó. En **[!UICONTROL Priorizar posibles clientes]**, elija un ajuste preestablecido o describa a las personas que desee en el chat.

| Ajuste preestablecido | Contactos que encuentra |
| --- | --- |
| **[!UICONTROL Contactos de ventas]** | Contactos del director de ventas y del responsable de ventas |
| **[!UICONTROL Contactos de marketing]** | Vicepresidente de contactos de Marketing and Marketing Manager |
| **[!UICONTROL Contactos del producto]** | Contactos de SVP Product y Product Manager |
| **[!UICONTROL Contactos de tecnología]** | Director de TI y vicepresidente de Ingeniería contactos |
| **[!UICONTROL Todos los contactos de CRM]** | Todos los contactos disponibles en las cuentas, hasta el límite de 2000 posibles clientes |

Para una solicitud de chat, ingrese `Find VP and Director level people at these accounts`, `Find C-level executives (CEO, CTO, CFO) at these accounts` o `Find managers at these accounts`.

Revise los resultados de la ficha **[!UICONTROL Posibles clientes]**. Cada posible cliente muestra su nombre, título, cuenta, correo electrónico, propietario y puntuación. Filtre por antigüedad, si hay una dirección de correo electrónico disponible, puntuación mínima o máxima, o si el posible cliente está en un flujo de trabajo. La columna **[!UICONTROL Razonamiento]** explica por qué cada posible cliente se clasifica donde está.

### Cómo funcionan las puntuaciones

Las puntuaciones van del 0 al 100. Una puntuación más alta indica un mejor ajuste y una mayor disposición para participar. Los mismos datos producen la misma puntuación.

Una puntuación combina:

* **Ajuste**: La medida en que la cuenta coincide con el perfil de cliente ideal, como el sector y el tamaño.
* **Señales de compra y crecimiento**: Señales como contratación, financiamiento y cambios de liderazgo. Las señales recientes cuentan más.
* **Contexto de ventas**: un contexto como el de un cliente existente con una oportunidad de expansión.

Revise el razonamiento y los datos disponibles antes de decidir con quién ponerse en contacto.

## Añadir posibles clientes a un flujo de trabajo saliente

Después de revisar los posibles clientes, agregue los que desee a un flujo de trabajo saliente existente.

1. En la ficha **[!UICONTROL Posibles clientes]**, filtre y seleccione los posibles clientes que desee. Por ejemplo, seleccione posibles clientes con una dirección de correo electrónico y una puntuación mínima de 70.
1. Seleccione **[!UICONTROL Agregar a flujo de trabajo saliente]**.
1. Seleccione el flujo de trabajo y confirme.
1. Revise la confirmación. La columna **[!UICONTROL Flujo de trabajo]** muestra **[!UICONTROL Asignado]** para los posibles clientes agregados.

También puede pedir al chat que añada los posibles clientes a un flujo de trabajo por su nombre. Si no conoce el nombre, pida al chat que enumere los flujos de trabajo disponibles. Compruebe el nombre del flujo de trabajo y el número de posibles clientes en la respuesta.

Añadir posibles clientes no reemplaza la revisión y aprobación por correo electrónico. Siga los pasos para [revisar los correos electrónicos generados](outbound-workflows.md#review-and-refine-generated-emails) y [aprobar e inscribir a los posibles clientes](outbound-workflows.md#approve-and-enroll-prospects) antes de que se envíe el alcance.

## Alcance y límites actuales

Durante la Beta, tenga en cuenta estos límites:

* Pida una columna o una señal por solicitud.
* La audiencia inteligente utiliza campos de cuenta de CRM estándar. No se admiten campos CRM personalizados.
* No se admite el filtrado por los productos que posee una cuenta.
* Para Salesforce, no está disponible la búsqueda de cuentas que tengan una oportunidad abierta. La búsqueda de cuentas sin oportunidades abiertas funciona con ambos CRM.
* Para Salesforce, las solicitudes sobre contratación para una función específica, como representantes de ventas, no están disponibles.

>[!MORELIKETHIS]
>
>* [Cuentas](accounts.md)
>* [Clientes potenciales](prospects.md)
>* [Flujos de trabajo salientes](outbound-workflows.md)
>* [Chat de IA](ai-assistant.md)
