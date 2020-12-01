---
description: De forma predeterminada, todas las compañías sincronizan datos con Adobe Media Optimizer (AMO). En la interfaz de usuario del administrador, cada contenedor de compañía tiene un origen de datos que administra este proceso. Esta fuente de datos es AMO de Adobe (ID 411). Haga clic en una fila de contenedor (en la ficha Contenedores) de una compañía seleccionada para desactivar esta sincronización predeterminada o para agregar y quitar otras fuentes de datos al proceso de sincronización de AMO.
seo-description: De forma predeterminada, todas las compañías sincronizan datos con Adobe Media Optimizer (AMO). En la interfaz de usuario del administrador, cada contenedor de compañía tiene un origen de datos que administra este proceso. Esta fuente de datos es AMO de Adobe (ID 411). Haga clic en una fila de contenedor (en la ficha Contenedores) de una compañía seleccionada para desactivar esta sincronización predeterminada o para agregar y quitar otras fuentes de datos al proceso de sincronización de AMO.
seo-title: Sincronización de ID con Media Optimizer
title: Sincronización de ID con Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 6%

---


# Sincronización de ID con Media Optimizer {#id-syncing-with-media-optimizer}

De forma predeterminada, todas las compañías sincronizan datos con [!DNL Adobe Media Optimizer] ([!DNL AMO]). En [!UICONTROL Admin UI], cada contenedor de compañía tiene un origen de datos que administra este proceso. Esta fuente de datos es [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Haga clic en una fila de contenedor (en la ficha [!UICONTROL Containers]) para que una compañía seleccionada desactive esta sincronización predeterminada o para agregar y eliminar otras fuentes de datos al proceso de sincronización [!DNL AMO].

![](assets/id-sync.png)

## Estado de sincronización de ID {#id-sync-status}

En la tabla siguiente se describe el estado de sincronización de un origen de datos.

| Estado | Descripción |
|------ | -------- |
| Off | Quite todas las fuentes de datos de [!UICONTROL Selected Data Sources] para este contenedor a fin de deshabilitar las sincronizaciones de ID con [!DNL AMO] |
| Activado (independientemente de la versión del servicio de ID) | Un origen de datos se sincroniza con [!DNL AMO] independientemente de la versión del servicio de ID cuando: <ul><li>El origen de datos aparece en la lista [!UICONTROL Selected Data Sources].</li><li>La casilla de verificación [!DNL AMO] *no está* seleccionada.</li></ul> |
| Activado (independientemente de la versión del servicio de ID) | Una fuente de datos se sincronizará con [!DNL AMO] con la versión 2.0 (o buena) del servicio de ID cuando: <ul><li>El origen de datos aparece en la lista [!UICONTROL Selected Data Sources].</li><li>La casilla de verificación [!DNL AMO] *está* seleccionada.</li></ul> |

>[!MORELIKETHIS]
>
>* [Administrar contenedores](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

