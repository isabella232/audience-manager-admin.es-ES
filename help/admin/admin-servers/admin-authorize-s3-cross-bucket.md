---
description: Es posible que algunos clientes no deseen proporcionar a Adobe el acceso a Amazon Simple Almacenamiento Service (Amazon S3) o claves secretas para autorizar la carga de datos de destino en sus bloques.
seo-description: Es posible que algunos clientes no deseen proporcionar a Adobe el acceso a Amazon Simple Almacenamiento Service (Amazon S3) o claves secretas para autorizar la carga de datos de destino en sus bloques.
seo-title: Cómo autorizar el acceso de cubos de cuentas cruzadas a Amazon S3 para destinos por lotes
title: Cómo autorizar el acceso de cubos de cuentas cruzadas a Amazon S3 para destinos por lotes
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

Es posible que algunos clientes no deseen proporcionar a Adobe sus claves de acceso [!DNL Amazon S3] o secreto para autorizar la carga de datos de destino en sus bloques.

Una alternativa en la que podemos oferta a nuestros clientes es [!UICONTROL Cross-Account Bucket Permissions] en [!DNL Amazon S3]. Este proceso se describe en la documentación [de](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)AWS. Para habilitar esta alternativa en Audience Manager, siga los pasos a continuación:

1. Vaya a **[!UICONTROL Servers]** y seleccione **[!UICONTROL Create Server]**.
1. Seleccione **[!UICONTROL S3]** en la máscara **[!UICONTROL Protocol/Credentials]** desplegable.
1. Marque la **[!UICONTROL Use Internal Adobe Key]** opción.
1. Utilice la cuenta y el nombre del depósito de su cliente en [!DNL Amazon S3].
1. Asegúrese de que el blanco del cliente lista la [!DNL Amazon S3] cuenta `975822914085` en su [!DNL S3] bucket.

>[!NOTE]
>
>Nuestro editor saliente garantiza que el nivel de permiso `bucket-owner-full-control` se establezca en los datos cargados, de modo que el cliente pueda ser propietario de esos datos.
