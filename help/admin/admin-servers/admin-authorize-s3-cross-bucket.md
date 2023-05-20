---
description: Es posible que algunos clientes no deseen proporcionar su acceso a Amazon Simple Storage Service (Amazon S3) o claves secretas al Adobe para autorizar la carga de datos de destino en sus contenedores.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Cómo autorizar el acceso de bloques de Amazon S3 entre cuentas para destinos por lotes
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Cómo autorizar el acceso de bloques de Amazon S3 entre cuentas para destinos por lotes{#authorize-cross-account-bucket-batch}

Es posible que algunos clientes no deseen proporcionar su [!DNL Amazon S3] Acceda a las claves secretas de Adobe para autorizar la carga de datos de destino en sus contenedores.

Una alternativa que podemos ofrecer a nuestros clientes es [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Este proceso se describe en la [Documentación de AWS](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Para habilitar esta alternativa en Audience Manager, siga los pasos a continuación:

1. Ir a **[!UICONTROL Servers]** y seleccione **[!UICONTROL Create Server]**.
1. Seleccionar **[!UICONTROL S3]** en el **[!UICONTROL Protocol/Credentials]** máscara desplegable.
1. Compruebe la **[!UICONTROL Use Internal Adobe Key]** opción.
1. Utilice la cuenta de cliente y el nombre del bloque en [!DNL Amazon S3].
1. Asegúrese de que el cliente incluye en la lista blanca las [!DNL Amazon S3] account `975822914085` en su [!DNL S3] cubo.

>[!NOTE]
>
>Nuestro editor de salida garantiza que el nivel de permisos `bucket-owner-full-control` se configura en los datos cargados de modo que el cliente pueda ser propietario de esos datos.
