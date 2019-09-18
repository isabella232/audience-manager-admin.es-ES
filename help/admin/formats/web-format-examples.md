---
description: Ejemplos de algunas combinaciones de macros HTTP más utilizadas.
seo-description: Ejemplos de algunas combinaciones de macros HTTP más utilizadas.
seo-title: Ejemplos de macros de formato HTTP
title: ' Ejemplos de macros de formato HTTP'
uuid: a81a2e2a-de7e-4b6a-8771-fcfa0dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# Ejemplos de macros de formato HTTP {#http-format-macro-examples}

Ejemplos de algunas combinaciones de [!DNL HTTP] macros más utilizadas.

Consulte las macros de formato [HTTP](../formats/web-formats.md) para obtener una lista de macros y sus definiciones.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ejemplos de macros </th> 
   <th colname="col2" class="entry"> Formato de salida </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|count:&lt;NUM_USERS&gt;|users:[&lt;USER_LIST:{user|&lt;user.aamUuid&gt;:&lt;user.dpUuid&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>"pid_alias|count:2|users:[uuid1:dpuuid1, uuid2:dpuuid2]"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_AGENT&gt;|&lt;IP&gt;|&lt;TIMESTAMP&gt;|&lt;RANDOM&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_LIST:{u|&lt;u.userAgent&gt;|&lt;u.ip&gt;|&lt;u.timestamp&gt;|&lt;u.random&gt;}; separator=", "&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;DP_UIDS.1&gt; Y &lt;DP_UIDS.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid1 Y dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>usuarios:[&lt;USER_LIST:{user|&lt;user.dpUuids.1&gt; Y &lt;user.dpUuids.2&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>usuarios:[dpuuid1 AND dpuuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_known_string=loremlipsum&amp;segid=&lt;TRAITALIAS_LIST; separator=","&gt;&amp;test_dpuuid_1000=&lt;DP_UIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_known_string=loremlipsum&amp;segid=trait_1,trait_2&amp;test_dpuuid_1000=dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_dpuuids=&lt;DP_UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_dpuuids=dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>"&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;|&lt;REMOVED_TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Usuarios": [&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; "AAM_UID": "&lt;user.aamUuid&gt;", "DataPartner_UID": "&lt;user.dpUuid&gt;", "Segments": [&lt;user.segments:{seg|&lt;OPEN_BRACKET&gt;"Segmento": "&lt;OPEN_BRACKET: .traitAlias&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt;] "Removed_Segments": [&lt;user.removeSegments:{rseg|&lt;OPEN_BRACKET&gt;"Segment": "&lt;rseg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt; &lt;CLOSE_BRACKET}; separator=","&gt;]} </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       { "Users":[ { "AAM_UUID":"uuid1", "DataPartner_UUID":"dpuuid1", "Segments":[ { "Segment":"alias1" }, { "Segment":"alias2" } ], "Eliminved_Segments":[ { "Segment":"alias3" }, { "Segment": alias4" } ] } ] } </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Usuarios": [&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; "AAM_UID": "&lt;user.aamUuid&gt;", "DataPartner_UID": "&lt;user.dpUuid&gt;", "Segments": [&lt;user.segments:{seg|&lt;OPEN_BRACKET&gt;"Segmento": "&lt;OPEN_BRACKET: .traitAlias&gt;","Status": "&lt;seg.status&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt;] &lt;CLOSE_BRACKET&gt;}; separator=","&gt;]} </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       { "Usuarios":[ { "AAM_UUID":"uuid1", "DataPartner_UUID":"dpuuid1", "Segmentos":[ { "Segmento":"alias1" "Estado":"1" }, { "Segmento":"alias2" "Estado":"0" } ] } } ] } </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;|&lt;REMOVED_SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;if(user.segments &amp;&amp; user.removeSegments)&gt;&lt;COMMA&gt;&lt;endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>Imprime una coma si los campos <code>segmentos</code> y <code>removeSegments</code> no están vacíos. Este condicional se puede usar para solicitudes POST al concatenar listas para segmentos y segmentos eliminados. </p> </td> 
  </tr> 
 </tbody> 
</table>
