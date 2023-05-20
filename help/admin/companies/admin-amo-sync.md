---
description: De forma predeterminada, todas las empresas sincronizan los datos con Adobe Media Optimizer (AMO). En la IU de administración, cada contenedor de compañía tiene una fuente de datos que administra este proceso. Esta fuente de datos es el Adobe AMO (ID 411). Haga clic en una fila de contenedor (en la pestaña Contenedores ) de una empresa seleccionada para deshabilitar esta sincronización predeterminada o para agregar y quitar otras fuentes de datos al proceso de sincronización de AMO.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: Sincronización de ID con Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 6%

---

# Sincronización de ID con Media Optimizer {#id-syncing-with-media-optimizer}

De forma predeterminada, todas las empresas sincronizan los datos con [!DNL Adobe Media Optimizer] ([!DNL AMO]). En el [!UICONTROL Admin UI], cada contenedor de compañía tiene una fuente de datos que administra este proceso. Esta fuente de datos es [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Haga clic en una fila de contenedor (debajo de la etiqueta [!UICONTROL Containers] para que una empresa seleccionada desactive esta sincronización predeterminada o para agregar y quitar otras fuentes de datos a [!DNL AMO] proceso de sincronización.

![](assets/id-sync.png)

## Estado de sincronización de ID {#id-sync-status}

En la tabla siguiente se describe el estado de sincronización de un origen de datos.

| Estado | Descripción |
|------ | -------- |
| Off | Eliminar todas las fuentes de datos de [!UICONTROL Selected Data Sources] para que este contenedor deshabilite la sincronización de ID con [!DNL AMO] |
| Activado (independientemente de la versión del servicio de ID) | Una fuente de datos se sincroniza con [!DNL AMO] independientemente de la versión del servicio de ID cuando: <ul><li>La fuente de datos aparece en la [!UICONTROL Selected Data Sources] lista.</li><li>El [!DNL AMO] casilla de verificación *no es* seleccionados.</li></ul> |
| Activado (independientemente de la versión del servicio de ID) | Una fuente de datos se sincronizará con [!DNL AMO] con la versión 2.0 del servicio de ID (o la buena) cuando: <ul><li>La fuente de datos aparece en la [!UICONTROL Selected Data Sources] lista.</li><li>El [!DNL AMO] casilla de verificación *es* seleccionados.</li></ul> |

>[!MORELIKETHIS]
>
>* [Administrar contenedores](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

