---
description: Ejemplos de algunas combinaciones de macro HTTP utilizadas habitualmente.
seo-description: Ejemplos de algunas combinaciones de macro HTTP utilizadas habitualmente.
seo-title: Ejemplos de macros de formato HTTP
title: Ejemplos de macros de formato HTTP
uuid: a 81 a 2 e 2 a-de 7 e -4 b 6 a -8771-fcfa 0 dc 74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# Ejemplos de macros de formato HTTP {#http-format-macro-examples}

Ejemplos de algunas combinaciones [!DNL HTTP] de macro utilizadas comúnmente.

Consulte las macros Formato [HTTP](../formats/web-formats.md) para obtener una lista de macros y sus definiciones.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ejemplos de macro </th> 
   <th colname="col2" class="entry"> Formato de salida </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS &gt;|&lt; DP_ UUID &gt;|&lt; TRASINGAS_ LIST; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS &gt;| count: &lt; NUM_ USERS &gt;| usuarios: [&lt; USER_ LIST: {user|&lt; user. aamuuid &gt;: &lt; user. dpuuid &gt;}; separator = "," &gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>" pid_ alias | count: 2 | usuarios: [uuid 1: dpuuid 1, uuid 2: dpuuid 2] "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ AGENT &gt;|&lt; IP &gt;|&lt; TIMESTAMP &gt;|&lt; RANDOM &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>" Firefox | 255.255.255.255 | 1395758143 | 42341 "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ LIST: {u|&lt; u. useragent &gt;|&lt; u. ip &gt;|&lt; u. timestamp &gt;|&lt; u. random &gt;}; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>" Firefox | 255.255.255.255 | 1395758143 | 42341 "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; DP_ UUIDS .1 &gt; AND &lt; DP_ UUIDS .2 &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid 1 AND dpuuid 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>usuarios: [&lt; USER_ LIST: {user|&lt; user. dpuuids .1 &gt; AND &lt; user. dpuuids .2 &gt;}; separator = "," &gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>usuarios: [dpuuid 1 AND dpuuid 2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ known_ string = lorelipsum &amp; segid = &lt; TRASINGAS_ LIST; separator = "," &gt; &amp; test_ dpuuid_ 1000 = &lt; DP_ UUIDS .1000 &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ known_ string = loremlipsum &amp; segid = trait_ 1, trait_ 2 &amp; test_ dpuuid_ 1000 = dpuuid_ 1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ dpuuids = &lt; DP_ UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ dpuuids = dpuuid 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>" &lt; PID_ ALIAS &gt;|&lt; DP_ UUID &gt;|&lt; TRASINGAS_ LIST; separator = "," &gt;|&lt; REMOVED_ TRAITALIAS_ LIST; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2 | trait_ 3, trait_ 4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"Usuarios": [&lt; USER_ LIST: {user|&lt; OPEN_ BRACKET &gt; 
 " AAM_ UUID ": " &lt; user. aamuuid &gt; ", 
 " Datapartner_ UUID ": " &lt; user. dpuuid &gt; ", 
 " Segmentos ": [&lt; user. segments: {seg|&lt; OPEN_ BRACKET &gt; "Segment": " &lt; seg. traitalias &gt; " &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;] 
 " Removed_ Segments ": [&lt; user. removedsegments: {rseg|&lt; OPEN_ BRACKET &gt; "Segment": " &lt; rseg. traitalias &gt; " &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;] 
 &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{{{{{{{{{{ 
 " Usuarios ": [[ 
 {{{{{{{{{{ 
 " AAM_ UUID ": " uuid 1 ", 
 " Datapartner_ UUID ": " dpuuid 1 ", 
 " Segmentos ": [[ 
 {{{{{{{{{{ 
 " Segmento ": " alias 1 " 
 }, 
 {{{{{{{{{{ 
 " Segmento ": " alias 2 " 
 } 
 ], 
 " Removed_ Segments ": [[ 
 {{{{{{{{{{ 
 " Segmento ": " alias 3 " 
 }, 
 {{{{{{{{{{ 
 " Segmento ": " alias 4 " 
 } 
 ] 
 } 
 ] 
 } </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"Usuarios": [&lt; USER_ LIST: {user|&lt; OPEN_ BRACKET &gt; 
 " AAM_ UUID ": " &lt; user. aamuuid &gt; ", 
 " Datapartner_ UUID ": " &lt; user. dpuuid &gt; ", 
 " Segmentos ": [&lt; user. segments: {seg|&lt; OPEN_ BRACKET &gt; "Segment": " &lt; seg. traitalias &gt; "," Status ": " &lt; seg. status &gt; " &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;] 
 &lt; CLOSE_ BRACKET &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{{{{{{{{{{ 
 " Usuarios ": [[ 
 {{{{{{{{{{ 
 " AAM_ UUID ": " uuid 1 ", 
 " Datapartner_ UUID ": " dpuuid 1 ", 
 " Segmentos ": [[ 
 {{{{{{{{{{ 
 " Segmento ": " alias 1 " 
 " Estado ": " 1 " 
 }, 
 {{{{{{{{{{ 
 " Segmento ": " alias 2 " 
 " Estado ": " 0 " 
 } 
 ] 
 } 
 ] 
 } </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS &gt;|&lt; DP_ UUID &gt;|&lt; SEGMENTOS: {seg|&lt; seg. traitalias &gt;}; separator =\ ",\" &gt;|&lt; REMOVED_ SEGMENTS: {seg|&lt; seg. traitalias &gt;}; separator =\ ",\" &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2 | trait_ 3, trait_ 4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; if (user. segments &amp; &amp; user. removedsegments) &gt; &lt; COMA &gt; &lt; endif &gt;</code> </p> </td> 
   <td colname="col2"> <p>Imprime una coma si <code>los segmentos de campos</code> y <code>removedsegments no</code> están vacíos. Esta condicional se puede utilizar para solicitudes POST al concatenar listas para segmentos y eliminar segmentos. </p> </td> 
  </tr> 
 </tbody> 
</table>
