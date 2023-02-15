### Scopo


Questa guida all'implementazione fornisce le mappe per trasformare i documenti da CDA a FHIR utilizzando il [FHIR Mapping Language (FML)](https://www.hl7.org/fhir/mapping-language.html).

Le mappe possono essere riutilizzate all'interno di altre mappe, infatti, è definita la trasformazione dei datatypes del CDA nei corrispettivi FHIR, la trasformazione dei campi del header di un documento CDA2 in risorse FHIR e infine, la mappa dei campi del body del documento specifico.

### Definizione delle Mappe di trasformazione


Le mappe elencate nella tabella seguente sono disponibili come [FHIR Structure Maps](https://www.hl7.org/fhir/structuremap.html).

I documenti previsti per la trasformata includono, come definito dal DPCM n.18 del 29 settembre 2015, i documenti del nucleo minimo per l'attuazione del FSE (Fascicolo Sanitario Elettronico).

{:class="table table-bordered"}
| Mapping di  | Trasformata da CDA a FHIR |
|----------------|-------------|
| Tipo di dati | [Trasformata del tipo di dato](StructureMap-cda2fhirDataTypes.html) |
|----------------|-------------|
| Documenti | [Header CDA in Bundle](StructureMap-cda2fhirHeader.html)|
|----------------|-------------|
| | [Referto di Laboratorio in Bundle](StructureMap-cda2fhirLabReport.html)|
| | [Referto di Radiologia in Bundle](StructureMap-cda2fhirRadReport.html)|
| | [Lettera di Dimissione Ospedaliera in Bundle](StructureMap-cda2fhirLdo.html)|
| | [Referto di Specialistica Ambulatoriale in Bundle](StructureMap-cda2fhirAmbReport.html)|
| | [cda2fhirVaccination in Bundle](StructureMap-cda2fhirVaccination.html)|
| | [Verbale di Pronto Soccorso in Bundle](StructureMap-cda2fhirEdReport.html)|
| | [Profilo Sanitario Sintetico (PSS) in Bundle](StructureMap-cda2fhirPs.html)|



### Funzionalità delle Mappe di trasformazione


L'architettura del FSE nazionale prevede la progettazione di un Gateway FHIR che rappresenta il punto di governo dell’intera piattaforma in quanto avrà il compito di verificare che i dati clinici, prodotti dai sistemi delle strutture sanitarie, rispettino le regole sintattiche e semantiche, di data quality e di privacy previste dall’affinity domain.
Dopo la validazione, il Gateway ha il compito di tradurli nel formato HL7 FHIR e inviarli al Data Repository Centrale (EDS).

Le mappe rappresentano lo strumento tramite il quale il Gateway può generare una Bundle a partire da un documento CDA, abilitando il processo di trasformazione.


<!-- ![Logica di Trasformazione in FHIR](Trasformazione.png) -->
<table>
<tbody>
<tr class="odd">
<td><p><img src="Trasformazione.png" style="width:6.00in;height:4.95in" /></p>
<p>Figura XX - Logica di Trasformazione in FHIR</p></td>
</tr>
</tbody>
</table>
