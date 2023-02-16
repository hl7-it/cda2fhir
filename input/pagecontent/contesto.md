### Contesto di riferimento

Coerentemente con quanto stabilito nel DPCM n.18 del 29 settembre 2015, ovvero il Regolamento in materia di fascicolo sanitario elettronico, "i contenuti del FSE sono rappresentati da un nucleo minimo di dati e documenti, nonchè da dati e documenti integrativi chepermettono di arricchire il Fascicolo stesso".

Rispetto i documenti "si adotta lo standard HL7 (Health Level 7) per descrivere le definizioni dei dati da scambiare in termini di messaggi e documenti costituenti il FSE, e in particolare è prescritto l'utilizzo del CDA (Clinical Document Architecture) release 2 (ISO/HL7 27932:2009)".

Successivamente, tramite il Decreto n.160/2022, per l'attuazione del FSE (Fascicolo Sanitario Elettronico), è stato stabilito che i documenti devono essere "mappati in standard FHIR" e memorizzati. Questi dati devono essere conservati in Data Repository Centrali, a norma dell'articolo 21 del DL 4/2022 nell'ambito di EDS (Ecosistema di dati Sanitari), e resi disponibili via API per la costruzione di servizi di:

● **Prevenzione, diagnosi, cura e riabilitazione** rivolti ai professionisti sanitari e alle strutture sanitarie abilitate, secondo le autorizzazioni l trattamento rilasciate dagli assistiti, oltre che ai cittadini al fine di consultare le proprie informazioni cliniche;

● **Prevenzione, sorveglianza epidemiologica e governo** di supporto alle Direzioni Sanitarie Regionali e delle Province Autonome, nonché di prevenzione e profilassi internazionale, di supporto al Ministero della Salute.

### Infrastruttura

L'architettura del FSE 2.0 prevede che le strutture sanitarie si interfaccino con il Gateway. Il Gateway offrirà numerosi servizi, tra cui:

● **Validazione dei documenti CDA2**: secondo quanto previsto dal decreto, in linea con le IG dei documenti del nucleo minimo pubblicate da Hl7 Italia ([Specifiche e Guide di HL7 Italia](http://www.hl7italia.it/hl7italia_D7/node/2359));

● **Trasformazione in FHIR**: i documenti CDA2, una volta validati, sono tradotti nel formato HL7 FHIR , qualora questi non siano generati direttamente in questo formato nativo, e inviarli al Data Repository Centrale.(EDS)

● **Validare il processo per permettere la conservazione del documento e del suo indice**: se entrambe le fasi precedenti sono eseguite nel modo corretto, il Gateway permetterà all'infrastruttura di pubblicare il documento clinico corrispondente per poterlo indicizzare sul Registry nazionale (tramite i servizi INI e ANA), oltre che sul Registry regionale.
<!-- 
![](Infrastruttura.png) -->

<!-- <table>
<tbody>
<tr class="odd">
<td><p><img src="Infrastruttura.png" style="width:7.00in;height:4.44556in" /></p>
<p>Figura XX - Flusso dei dati previsto per FSE 2.0 e attori coinvolti</p></td>
</tr>
</tbody>
</table> -->


### Implementazione

<table>
<tbody>
<tr class="odd">
<td><p><img src="Processo_Logico.png" style="width:7.00in;height:2.47in" /></p>
<p>Figura XX - Flusso dei documenti/dati previsto per FSE 2.0 e attori coinvolti</p></td>
</tr>
</tbody>
</table>

