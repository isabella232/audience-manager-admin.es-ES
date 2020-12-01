---
description: Es posible que algunos clientes no deseen proporcionar el acceso a Amazon Simple Almacenamiento Service (Amazon S3) o claves secretas de Adobe para autorizar la carga de datos de destino en sus bloques.
seo-description: Es posible que algunos clientes no deseen proporcionar el acceso a Amazon Simple Almacenamiento Service (Amazon S3) o claves secretas de Adobe para autorizar la carga de datos de destino en sus bloques.
seo-title: Cómo autorizar el acceso de bucket a cuentas múltiples de Amazon S3 para destinos por lotes
title: Cómo autorizar el acceso de bucket a cuentas múltiples de Amazon S3 para destinos por lotes
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Cómo autorizar el acceso de bucket a cuentas múltiples de Amazon S3 para destinos por lotes{#authorize-cross-account-bucket-batch}

Es posible que algunos clientes no deseen proporcionar su acceso [!DNL Amazon S3] o claves secretas al Adobe para autorizar la carga de datos de destino en sus bloques.

Una alternativa para la oferta de nuestros clientes es [!UICONTROL Cross-Account Bucket Permissions] en [!DNL Amazon S3]. Este proceso se describe en la [documentación de AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Para habilitar esta alternativa en Audience Manager, siga los pasos a continuación:

1. Vaya a **[!UICONTROL Servers]** y seleccione **[!UICONTROL Create Server]**.
1. Seleccione **[!UICONTROL S3]** en la máscara desplegable **[!UICONTROL Protocol/Credentials]**.
1. Marque la opción **[!UICONTROL Use Internal Adobe Key]**.
1. Utilice la cuenta y el nombre del depósito del cliente en [!DNL Amazon S3].
1. Asegúrese de que el blanco del cliente enumera la cuenta [!DNL Amazon S3] `975822914085` en su bloque [!DNL S3].

>[!NOTE]
>
>Nuestro editor saliente garantiza que el nivel de permisos `bucket-owner-full-control` se establezca en los datos cargados, de modo que el cliente pueda ser propietario de esos datos.
