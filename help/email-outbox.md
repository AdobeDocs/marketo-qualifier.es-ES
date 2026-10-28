---
title: Revisar la bandeja de salida de correo electrónico
description: Obtenga información sobre cómo revisar los correos electrónicos que Adobe Marketo Qualifier ha enviado en su nombre, incluidas las respuestas, en la bandeja de salida de correo electrónico.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: e6e1112f-735e-4244-9aeb-08972bded7e7
    internal-label: Email
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
    internal-label: Email marketing
source-git-commit: fcdc5d36cbb1500cf984e1439291aa8dbf17b72b
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%
---

# Bandeja de salida de correo

Use **[!UICONTROL Bandeja de salida de correo electrónico]** para revisar los mensajes de correo electrónico enviados por los flujos de trabajo salientes y las respuestas. Puede confirmar lo que se ha enviado, leer las respuestas en contexto y abrir el flujo de trabajo saliente que ha enviado un mensaje.

La página tiene dos paneles: una lista de correos electrónicos a la izquierda y una vista de lectura a la derecha. Arrastre el divisor entre ellos para cambiar el tamaño de la lista.

## Leer la lista de correo electrónico

La lista **[!UICONTROL Todos los correos electrónicos]** contiene una fila por cada correo electrónico enviado, con el correo electrónico más reciente primero. Cada fila muestra el nombre, el asunto y la fecha de envío del destinatario. Un correo electrónico sin asunto muestra _(sin asunto)_. Desplácese para cargar correos electrónicos más antiguos.

Al abrir la página, Adobe Marketo Qualifier selecciona el primer correo electrónico automáticamente para que su contenido aparezca a la derecha.

Si no has enviado ningún correo electrónico, la lista muestra _Tu bandeja de salida está vacía_. Después de enviar o programar un correo electrónico a través de un flujo de trabajo saliente, aparece aquí.

## Leer un correo electrónico y sus respuestas

Para abrir un correo electrónico a la derecha, selecciónelo en la lista. La vista de lectura consta de tres partes:

* **Destinatario**: el nombre, el puesto y la cuenta del destinatario, cuando estén disponibles.
* **Asunto y flujo de trabajo saliente**: el asunto, el nombre del [flujo de trabajo saliente](outbound-workflows.md) que envió el correo electrónico y el estado del flujo de trabajo saliente. Para abrir el flujo de trabajo saliente, seleccione su nombre.
* **Conversación**: el correo electrónico enviado y las respuestas en un subproceso. Cada entrada identifica si el mensaje se envió o recibió e incluye una marca de tiempo.

Los correos electrónicos se procesan según se enviaron, incluido el contenido personalizado. Si el cuerpo de un mensaje no está disponible, Marketo Qualifier mostrará una breve nota _Contenido de correo electrónico no disponible_ en su lugar.

>[!NOTE]
>
>La Bandeja de salida de correo electrónico es de solo lectura. Para realizar un seguimiento con un cliente potencial que haya respondido, abra el flujo de trabajo saliente o el cliente potencial. Para revisar el rendimiento del correo electrónico y las respuestas, consulte [Rendimiento de salida](performance.md).

>[!MORELIKETHIS]
>
>* [Flujos de trabajo salientes](outbound-workflows.md)
>* [Rendimiento de salida](performance.md)
>* [Tareas](tasks.md)
