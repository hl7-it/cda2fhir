### Scopo


Questa guida all'implementazione fornisce le mappe per trasformare i documenti da CDA a FHIR utilizzando il [FHIR Mapping Language (FML)](https://www.hl7.org/fhir/mapping-language.html).

Le mappe possono essere riutilizzate all'interno di altre mappe, infatti, è definita la trasformazione dei datatypes del CDA nei corrispettivi FHIR, la trasformazione dei campi del header di un documento CDA2 in risorse FHIR e infine, la mappa dei campi del body del documento specifico.

### Definizione delle Mappe di trasformazione


Le mappe elencate nella tabella seguente sono disponibili come [FHIR Structure Maps](https://www.hl7.org/fhir/structuremap.html).

I documenti previsti per la trasformata includono i documenti del nucleo minimo per l'attuazione del FSE (Fascicolo Sanitario Elettronico).

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
| | [Certificato Vaccinale e Singola Vaccinazione in Bundle](StructureMap-cda2fhirVaccination.html)|
| | [Verbale di Pronto Soccorso in Bundle](StructureMap-cda2fhirEdReport.html)|
| | [Profilo Sanitario Sintetico (PSS) in Bundle](StructureMap-cda2fhirPs.html)|



### Funzionalità delle Mappe di trasformazione


L'architettura del FSE nazionale prevede la progettazione di un Gateway FHIR che rappresenta il punto di governo dell’intera piattaforma in quanto avrà il compito di verificare che i dati clinici, prodotti dai sistemi delle strutture sanitarie, rispettino le regole sintattiche e semantiche, di data quality e di privacy previste dall’affinity domain.
Dopo la validazione, il Gateway ha il compito di tradurli nel formato HL7 FHIR.

Le mappe rappresentano lo strumento tramite il quale il Gateway può generare una Bundle a partire da un documento CDA, abilitando il processo di trasformazione.


<table>
<tbody>
<tr class="odd">
<td><p><img src="Trasformazione.png" style="width:4.00in;height:2.74in" /></p>
<p>Figura 1 - Logica di Trasformazione in FHIR</p></td>
</tr>
</tbody>
</table>



### Autori e contributori


<table>
    <thead>
        <tr class="header">
            <th>Ruolo</th>
            <th>Nome</th>
            <th>Organizzazione</th>
            <th>Contatto</th>
        </tr>
    </thead>
    <tbody>
        <tr class="odd">
            <td>Autore</td>
            <td>Ilenia Centonze</td>
            <td>EY Advisory spa</td>
            <td>ilenia.centonze@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Maria Teresa De Pippo</td>
            <td>EY Advisory spa</td>
            <td>maria.teresa.de.pippo@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Xhuliana Haxhi</td>
            <td>EY Advisory spa</td>
            <td>Xhuliana.haxhi@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Orgest Kuqi</td>
            <td>EY Advisory spa</td>
            <td>orgest.kuqi@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Marta Oliverio</td>
            <td>EY Advisory spa</td>
            <td>marta.oliverio@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Davide Spanu</td>
            <td>EY Advisory spa</td>
            <td>davide.spanu@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Eleny Mulugeta Teklehaimanot</td>
            <td>EY Advisory spa</td>
            <td>eleny.mulugeta.teklehaimanot@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Autore</td>
            <td>Augusto Ruggeri</td>
            <td>EY Advisory spa</td>
            <td>augusto.ruggeri@it.ey.com</td>
        </tr>
        <tr class="odd">
            <td>Contributore</td>
            <td>Giorgio Cangioli</td>
            <td>Hl7 Italia</td>
            <td>giorgio.cangioli@gmail.com</td>
        </tr>
        <tr class="odd">
            <td>Contributore</td>
            <td>Leonardo Alcaro</td>
            <td>Hl7 Italia</td>
            <td>leonardo.alcaro@teamdigitale.governo.it</td>
        </tr>
        <tr class="odd">
            <td>Contributore</td>
            <td>Mario Sicuranza</td>
            <td>HL7 Italia</td>
            <td>mario.sicuranza@icar.cnr.it</td>
        </tr>
    </tbody>
</table>