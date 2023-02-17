### Contesto di riferimento

Coerentemente con l'attuazione della Missione 6 Salute del PNRR e la misura rifierita alla realizzazione del FSE 2.0, le Linee Guida di Attuazione FSE 2.0 Decreto n.160 del 20 maggio 2022, prescrivono di uniformare i dati e documenti dell'FSE secondo standard HL7 FHIR per i dati HL7 CDA2  per i  documenti.

### Infrastruttura

L'adeguamento normativo (DL4/2022) introduce due nuovi elementi tecnologici all'interno dell'ecosistema del FSE 2.0: il gateway e l'Ecosistema Dati Sanitari. L’architettura del FSE 2.0 prevede che i sistemi produttori si interfaccino con la componente Gateway o con il middleware regionale seguendo regole tecniche e di processo definite. Il Gateway offrirà numerosi servizi, tra cui:

● **Validazione dei documenti CDA2**: secondo quanto previsto dal decreto, in linea con le IG dei documenti del nucleo minimo pubblicate da Hl7 Italia ([Specifiche e Guide di HL7 Italia](http://www.hl7italia.it/hl7italia_D7/node/2359));

● **Validazione dei metadati**: validazione dei metadati in conformità con l'Affinity Domain ai fini della pubblicazione dei documenti;

● **Trasformazione in FHIR**: i documenti CDA2, una volta validati, sono tradotti nel formato HL7 FHIR, qualora questi non siano generati direttamente in questo formato nativo.

<table>
<tbody>
<tr class="odd">
<td><p><img src="Processo_logico.png" style="width:7.00in;height:2.47in" /></p>
<p>Figura 2 - Flusso dei documenti/dati previsto per FSE 2.0 e attori coinvolti</p></td>
</tr>
</tbody>
</table>

Un Mapping Engine basato sullo standard FHIR mapping Language è già presente e funzionante all’interno dell’infrastruttura FSE 2.0 in realizzazione.
All’interno del motore del FSE 2.0 esiste un apposito [microservizio](https://github.com/ministero-salute/it-fse-gtw-fhir-mapping-engine) incaricato di trasformare i CDA2 in input in FHIR R4 Resource, utilizzando i files .map definiti per le singole tipologie di documento.
L’implementazione prevede una separazione tra la componente di trasformazione ed il [sistema di configurazione](https://github.com/ministero-salute/it-fse-srv-fhir) in modo da rendere indipendente il motore dall’aggiornamento delle regole di mapping, facilitando la manutenzione delle singole componenti anche per competenza.	
