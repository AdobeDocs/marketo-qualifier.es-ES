---
title: Notas de la versión de [!DNL Adobe Marketo Qualifier]
description: Descubra las novedades de [!DNL Adobe Marketo Qualifier].
feature: Agentic AI, Sales Insights, Account Journeys
role: User
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 11%
---
# Notas de la versión de [!DNL Adobe Marketo Qualifier]

## Próxima versión

* Encuentre y priorice las cuentas y los posibles clientes adecuados con Audiencia inteligente (Beta). Describa las cuentas que desea en un lenguaje sencillo, añada datos de CRM y señales de crecimiento, revise los posibles clientes puntuados y agréguelas a un flujo de trabajo saliente. [Más información](smart-audience.md).
* Filtre los contactos por campos de cuenta, junto con los campos de contacto y oportunidad, para encontrar los contactos adecuados y segmentar los flujos de trabajo salientes de forma más precisa. [Más información](prospects.md#filter-and-find-prospects).
* Los contactos muestran su cuenta asociada y su nombre de propietario, y la página de un cliente potencial ahora muestra 90 días de actividad de marketing, frente a los 30 anteriores. [Más información](prospects.md#review-prospect-details).

## 10-08-2026

Esta versión incluye:

* Reutilice un flujo de trabajo saliente o cambie los puntos de contacto de un flujo de trabajo en ejecución, duplíquelo y edite la copia. La copia comienza como borrador privado sin perspectivas y el flujo de trabajo original no cambia. [Más información](outbound-workflows.md#duplicate-an-outbound-workflow).
* Configure los flujos de trabajo salientes en un diseño compacto con navegación entre el objetivo, el objetivo, los puntos de contacto y la configuración. [Más información](outbound-workflows.md#create-an-outbound-workflow).
* Las solicitudes de borrado de exclusión en las respuestas de correo electrónico se reconocen automáticamente. El cliente potencial se marca como excluido y no se envían más puntos de contacto. [Más información](outbound-workflows.md#opt-out-requests-in-replies).
* Prepárese para reuniones con una sola información que combine investigación web y estudios de casos de clientes específicos de productos, con puntos de conversación clasificados por relevancia y fuentes identificadas. [Más información](prospects.md#generate-meeting-prep).
* Los correos electrónicos generados se contrastan con las directrices de calidad y se reescriben cuando es necesario antes de revisarlos. Aún puede revisar, editar y aprobar cada correo electrónico antes de enviarlo. [Más información](outbound-workflows.md#review-and-refine-generated-emails).

## 09-22-2026

Esta versión incluye:

* Vea [!DNL Marketo Sales Insights] y los datos agénticos en el complemento CRM incrustado y agregue clientes potenciales a [!DNL Marketo Qualifier]. [Más información](admin-settings.md#crm-mcp-and-the-embedded-plugin).
* Priorice los posibles clientes de CRM con las opciones más probables, mi lista de observación, actividad web, participación por correo electrónico y actividad de seminario web. [Más información](admin-settings.md#prioritize-leads-in-the-crm-plugin).
* Inscriba automáticamente a los posibles clientes en flujos de trabajo salientes cuando su actividad [!DNL Marketo] activa coincida con los criterios del flujo de trabajo. [Más información](home.md#automatically-enroll-prospects-from-marketing-highlights).
* Revise el contexto del cliente potencial y exporte la lista de clientes potenciales y vea los resúmenes de personas de IA en [!DNL Marketo Optimizer] instancias de Prime y Ultimate. [Más información](prospects.md#review-prospect-context-and-export-the-list).
* Revise y apruebe los correos electrónicos de clientes potenciales generados desde la cola de tareas y responda con sugerencias del agente durante un flujo de trabajo saliente. [Más información](tasks.md).

## 09-08-2026

Esta versión incluye:

* Establezca su propio estilo de dibujo de correo electrónico una vez en la configuración del perfil, y cada correo electrónico generado lo sigue. [Más información](profile-settings.md#email-drafting-context).
* Genere la preparación de la reunión personalizada o basada en objetivos desde la página de un posible cliente, en una nueva pestaña de investigación de la reunión. [Más información](prospects.md#generate-meeting-prep).
* Los administradores pueden asignar un flujo de trabajo saliente a un compañero de equipo y restablecer la configuración del flujo de trabajo a sus valores predeterminados. [Más información](outbound-workflows.md#create-an-outbound-workflow).
* Asigne campos personalizados al importar clientes potenciales desde un CSV y utilice esos valores en los correos electrónicos generados. [Más información](prospects.md#build-your-prospect-list).
* Los correos electrónicos generados utilizan cualquier dato de cliente potencial adicional que importe y pueden escribirse de forma nativa en el idioma del cliente potencial. [Más información](outbound-workflows.md#step-5-add-prospects-and-start-email-generation).
* Rendimiento saliente muestra la tasa de apertura y la tasa de clics de forma predeterminada, con un conmutador para los recuentos sin procesar y los prospectos totales en el nivel de organización. [Más información](performance.md).
* Las reglas de sincronización de CRM actualizan automáticamente el estado de CRM a medida que un cliente potencial avanza por un flujo de trabajo saliente. [Más información](admin-settings.md#configure-crm-sync-rules).
* Haga preguntas sobre el chat de IA en sus datos de [!DNL Marketo Qualifier], CRM, [!DNL Marketo] y [!DNL Marketo Optimizer]. [Más información](ai-assistant.md#ask-ai-chat-across-your-connected-data).

## 08-17-2026

[!DNL Marketo Qualifier] ya está disponible como una aplicación independiente. Admite [!DNL Marketo Engage] y [!DNL Marketo Optimizer].

Esta versión incluye:

* Priorización de clientes potenciales y cuentas con resúmenes de actividades generados por IA y puntuación basada en señales. [Más información](prospects.md#review-prospect-details) sobre los posibles clientes o [cuentas](accounts.md#account-insights).
* Flujos de trabajo salientes orientados a objetivos con cadencias propuestas por IA y correos electrónicos redactados. [Más información](outbound-workflows.md).
* Una cola de tareas unificada para llamadas telefónicas, LinkedIn InMails y revisiones de correo electrónico. [Más información](tasks.md).
* Reserva automática de reuniones mediante integración de calendario. [Más información](outbound-workflows.md#meeting-booking).
* Un centro de conocimientos para fundamentar el alcance de la IA en sus propios materiales de libro de estrategias. [Más información](admin-settings.md#knowledge-center).
* Chat de IA para preguntas en lenguaje natural basadas en los datos de su CRM, participación y centro de conocimiento. [Más información](ai-assistant.md).
* Informes de rendimiento de correo electrónico y reservas de reuniones. [Más información](performance.md).
* Complementos de explorador y correo electrónico para acceder a dentro de su CRM o Outlook. [Más información](admin-settings.md#crm-mcp-and-the-embedded-plugin).
* Compatibilidad con integraciones de Salesforce y Microsoft Dynamics 365. [Más información](integrations.md).
