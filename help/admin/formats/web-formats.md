---
description: Enumera las macros que puede utilizar para crear archivos de datos HTTP. HTTP envía datos en formato JSON.
seo-description: Enumera las macros que puede utilizar para crear archivos de datos HTTP. HTTP envía datos en formato JSON.
seo-title: ' Macros de formato HTTP'
title: ' Macros de formato HTTP'
uuid: 91021f60-75d0-4b1d-86ca-91c9dadafac1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# Macros de formato HTTP {#http-format-macros}

Enumera las macros que puede utilizar para crear archivos [!DNL HTTP] de datos. [!DNL HTTP] envía datos en un [!DNL JSON] formato.

Consulte los ejemplos [de macros de formato](../formats/web-format-examples.md) HTTP para obtener una lista y ejemplos de algunas combinaciones de macros más utilizadas.

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Tipo de método </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> ID de Audience Manager </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>ID de usuario único del socio de datos. Esta macro devuelve el ID que ha asignado a un usuario si su ID ya se ha sincronizado con un ID de dispositivo de <span class="keyword"> Audience Manager </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>ID del proveedor de datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>ID del proveedor de datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>GENERATION_TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Marca de hora Unix UTC. Una marca de tiempo interna representa la hora en que se notificó a AAM que publicara el destino <span class="wintitle"> S2S </span> en nuestros socios. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>La dirección IP del usuario. </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>ID de Experience Cloud. (MCID significa Marketing Cloud, que es el nombre heredado de Experience Cloud) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>El número (entero) de segmentos al que ya no pertenece un usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Número de segmentos a los que pertenece un usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>ID de pedido o destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Un alias para el ID del socio. También se conoce como ID de cuenta extranjera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ALEATORIO</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Genera un número aleatorio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REGION_ID_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Región DCS de <a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> Audience Manager </a> donde se originó la actividad.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Devuelve una lista de ID de segmento, si los hay, para los que un usuario ya no cumple los requisitos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Lista de segmentos para los que un usuario ya no cumple los requisitos. También puede devolver campos de segmento específicos que incluyen: </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>traitAlias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>heredadoSegmentId (anteriormente segmentId)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>newSegmentId</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>dateTime</code> </li> 
     </ul> </p> <p>Especifique estos campos en una matriz como se muestra en este ejemplo: </p> <p> <code>[&lt;REMOVED_SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapping":&lt;seg.traitAlias&gt;,"Status:"&lt;seg.status&gt;, "Time":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&lt;CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p>Consulte también <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Ejemplos de macros de formato HTTP </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> Una lista de las últimas realizaciones para segmentos para los que el usuario ya no cumple los requisitos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Lista de nombres con alias de segmentos para los que un usuario ya no cumple los requisitos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Devuelve una lista de ID de segmentos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENTOS</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Lista de segmentos para los que un usuario cumple los requisitos. También puede devolver campos de segmento específicos que incluyen: </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>traitAlias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>heredadoSegmentId (anteriormente segmentId)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>newSegmentId</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>dateTime</code> </li> 
     </ul> </p> <p>Especifique estos campos en una matriz como se muestra en este ejemplo: </p> <p> <code>[&lt;SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapping":&lt;seg.traitAlias&gt;,"Status:"&lt;seg.status&gt;, "Time":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&gt;&lt;CLOSE_Id RACKET&gt;}; "separator=","&gt;]</code> </p> <p>Consulte también <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Ejemplos de macros de formato HTTP </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Una lista de las últimas realizaciones. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MARCA DE HORA</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Marca de hora Unix, UTC. Representa la última realización del segmento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Una lista de nombres con alias para un segmento en particular. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>OBTENER</code> </p> </td> 
   <td colname="col3"> <p>Agente de usuario de la solicitud inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p>Una lista de <span class="keyword"> ID de </span> usuario de Audience Manager. También puede devolver campos específicos que incluyan lo siguiente: </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user.aamUuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user.dpUuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user.segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user.removeSegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user.userAgent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user.ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user.dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user.timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user.random</code> </li>
     <li><code>user.regionIds</code></li> 
    </ul> <p>Especifique estos campos como se muestra en este ejemplo: </p> <p> 
     <codeblock>
       "AAM_UUID": "&lt;user.aamUuid&gt;" "DataPartner_UUID": "&lt;user.dpUuid&gt;" 
     </codeblock> </p> <p>Consulte también <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Ejemplos de macros de formato HTTP </a> para ver un ejemplo completo. </p> </td> 
  </tr>
 </tbody>
</table>