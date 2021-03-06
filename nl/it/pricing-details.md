---

copyright:
  years: 2015, 2018, 2019
lastupdated: "2019-02-28"

subcollection: discovery

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:important: .important}
{:deprecated: .deprecated}
{:codeblock: .codeblock}
{:screen: .screen}
{:download: .download}
{:hide-dashboard: .hide-dashboard}
{:apikey: data-credential-placeholder='apikey'} 
{:url: data-credential-placeholder='url'}
{:curl: #curl .ph data-hd-programlang='curl'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:swift: .ph data-hd-programlang='swift'}
{:go: .ph data-hd-programlang='go'}

# Piani dei prezzi di Discovery
{: #discovery-pricing-plans}

Il servizio {{site.data.keyword.discoveryfull}} offre tre piani -- **Lite**, **Advanced** e **Premium** -- che forniscono livelli differenti di risorse e funzionalità per rispondere alle tue esigenze.
{: shortdesc}

I **casi d'uso di dati privati** presentano le funzioni, i limiti e i prezzi di seguito indicati:

## Lite
{: #lite}

Dimensione | Limite di archiviazione documenti | Numero di documenti\* | Prezzo 
------ | ------ | ------ | ------  
N/D | 50 MB | 1.000 al mese | Gratuito 

Il piano Lite è un piano iniziale e non deve essere utilizzato per la produzione. Quando esegui l'upgrade a un piano a pagamento, puoi conservare tutti i documenti inseriti.  Le istanze del piano di Lite sono eliminate dopo 30 giorni di inattività. 

Attributi:
- 1 ambiente
- Fino a 2 raccolte
- Miglioramenti NLU gratuiti\*\*

Opzioni aggiuntive:<br> [Modelli personalizzati](/docs/services/discovery?topic=discovery-integrating-with-wks#integrating-your-custom-model):<br>
Un modello Watson Knowledge Studio incluso. Modelli aggiuntivi. non disponibili<br>[Element Classification](/docs/services/discovery?topic=discovery-element-classification#element-classification)\*\*\*:
500 pagine incluse al mese. Pagine aggiuntive: non disponibili <br>[Query di notizie](/docs/services/discovery?topic=discovery-watson-discovery-news#watson-discovery-news):
200 query di notizie incluse al mese. Query aggiuntive: non disponibili<br>[Query Expansions](/docs/services/discovery?topic=discovery-query-concepts#query-expansion):
500 espansioni di query con un totale di 1.000 termini. Espansioni aggiuntive: non disponibili

Per informazioni sull'upgrade da Lite ad Advanced, vedi [Upgrade del tuo servizio](/docs/services/discovery?topic=discovery-upgrading-your-plan#service)

Per informazioni sulle prestazioni delle query, vedi [Prestazioni delle query](/docs/services/discovery?topic=discovery-qp#qp). Le query sono limitate in base al piano. Frequenze delle query medie stimate per i piani **Lite** e **Standard**: 1 QPS per le query riclassificate con due campi di testo di livello superiore.

## Advanced
{: #advanced}

Quando scegli una dimensione di piano Advanced, nota che sono necessarie delle risorse sia per l'archiviazione che per l'esecuzione di query dei documenti. Pertanto, potresti avere bisogno di un ambiente più grande se sei prossimo al limite massimo di documenti per una dimensione del piano e hai anche i seguenti requisiti: 

-  Requisiti di prestazioni delle query più elevati (ad esempio utilizzando la formazione della pertinenza)
-  Prevedi un ampio numero di utenti simultanei
-  Esigenze di query più complesse 

Per ulteriori dettagli sui fattori che influenzano le prestazioni delle query, vedi [Prestazioni delle query](/docs/services/discovery?topic=discovery-qp#qp). Le query sono limitate in base al piano. Frequenze delle query medie stimate per i piani **Advanced** (S, MS): 10 QPS per le query riclassificate con due campi di testo di livello superiore.

Dimensione | Limite di archiviazione documenti | Numero di documenti\* | Prezzo 
------ | ------ | ------ | ------ 
X-Small\*\*\*\* | 40 GB | Fino a 50.000 documenti al mese | A partire da $500 al mese  
Small | 160 GB | Fino a 1M di documenti al mese | A partire da $1.500 al mese  
Medium-Small | 320 GB | Fino a 2M di documenti al mese | A partire da $3.000 al mese 
Medium| 640 GB | Fino a 4M di documenti al mese | A partire da $5.000 al mese 
Medium-Large | 1,2 TB | Fino a 8M di documenti al mese | A partire da $10.000 al mese 
Large| 2,4 TB | Fino a 16M di documenti al mese | A partire da $15.000 al mese 
X-Large| 4 TB | Fino a 32M di documenti al mese | A partire da $20.000 al mese 
XX-Large | 5,5 TB | Fino a 64M di documenti al mese | A partire da $35.000 al mese 
XXX-Large | 12 TB | Fino a 100M di documenti al mese | A partire da $45.000 al mese 

X-Small è l'ambiente più piccolo disponibile ed è consigliato solo per sviluppo e test.\*\*\*\*

Il passaggio da un livello Advanced a un altro non richiede la creazione di nuove istanze. Delle nuove istanze saranno richieste se si passa da un piano Advanced a un piano Premium. Per informazioni sull'upgrade da un livello Advanced a un altro, vedi il documento relativo al [passaggio da un livello Advanced a un altro](/docs/services/discovery?topic=discovery-upgrading-your-plan#upgrading-your-plan).

\*\*\*\*Attributi dei piani X-Small: 
- 1 ambiente
- Fino a 4 raccolte
- Miglioramenti NLU gratuiti\*\*

Attributi di tutti gli altri piani Advanced:
- 1 ambiente
- Fino a 100 raccolte
- Miglioramenti NLU gratuiti\*\*

Opzioni aggiuntive:<br> [Modelli personalizzati](/docs/services/discovery?topic=discovery-integrating-with-wks#integrating-your-custom-model):<br>
Un modello Watson Knowledge Studio incluso. Modelli aggiuntivi: $800 ciascuno<br>[Element Classification](/docs/services/discovery?topic=discovery-element-classification#element-classification)\*\*\*:
500 pagine incluse al mese. Pagine aggiuntive: $0,40 ciascuna<br>[Query di notizie](/docs/services/discovery?topic=discovery-watson-discovery-news#watson-discovery-news):
200 query di notizie incluse al mese  
10.000 query aggiuntive (al mese): $0,10 per query<br>
Da 10.001 a 100.000 query aggiuntive (al mese): $0,05 per query<br>
Oltre 100.000 query (al mese): $0,03 per query<br>
[Espansioni di query](/docs/services/discovery?topic=discovery-query-concepts#query-expansion):
5.000 espansioni di query con 25.000 termini in totale

`-----`
<br>
\* Il limite documento presume una dimensione di documento media di 100KB su disco. La dimensione di documento è calcolata dopo essere passata per la conversione e l'arricchimento e, pertanto, può variare in modo significativo rispetto all'input originale. Puoi visualizzare il numero di documenti archiviati e la quantità totale di archiviazione utilizzata servendoti dell'API [Environments](https://{DomainName}/apidocs/discovery#get-environment-info) o [Collections](https://{DomainName}/apidocs/discovery#get-collection-details) oppure della strumentazione. Se i tuoi documenti sono in media più grandi di 100KB su disco, raggiungerai il limite di archiviazione di un piano prima del limite di documento massimo. Se esegui la [segmentazione del documento](/docs/services/discovery?topic=discovery-configservice#doc-segmentation) sui tuoi documenti, ciascun documento viene contato come un documento separato.

\*\* Gli [arricchimenti NLU (Natural Language Understanding)](/docs/services/discovery?topic=discovery-configservice#adding-enrichments) sono: Entity Extraction, Sentiment Analysis, Category Classification, Concept Tagging, Keyword Extraction, Relation Extraction, Emotion Analysis, Element Classification e Semantic Role Extraction.  Vengono arricchiti solo i primi 50.000 caratteri di ciascun documento. 

\*\*\* Element Classification è un arricchimento che analizza interamente i documenti di controllo per convertire, identificare e classificare gli elementi rilevanti. Utilizza Natural Language Processing per estrarre i seguenti elementi da documenti PDF: parte (a cui fa riferimento), natura (tipo di elemento) e categoria (classe specifica).

Per avvalerti delle nuove opzioni di dimensione dell'ambiente (`LT`, `XS`, `S`, `MS`, `M`, `ML`, `L`, `XL`, `XXL`, `XXXL`), devi utilizzare la data della versione API `2018-08-01` o successiva quando crei ambienti con l'API. Le dimensioni dell'ambiente ora hanno il tipo `string` (in precedenza il tipo era `integer`).
{: note}

## Premium
{: #premiumplan}
   
I piani Premium offrono agli sviluppatori e alle organizzazioni un'istanza a singolo tenant di uno o più servizi Watson per un isolamento e una sicurezza migliori. Questi piani offrono isolamento a livello di calcolo sulla piattaforma condivisa esistente, come pure dati crittografati end-to-end sia in transito che inattivi. 

Per ulteriori informazioni o per acquistare un piano Premium, contatta il reparto [Vendite](https://ibm.biz/contact-wdc-premium). 

## Ulteriori informazioni
{: #pricingadd}

Per informazioni sul calcolo dei costi, vedi [Calcolatore del prezzo IBM Cloud ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/pricing/platform/watson){: new_window}.

Per informazioni sulla sicurezza di IBM Cloud, vedi il documento relativo alla [Sicurezza e riservatezza dei dati dei servizi cloud![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/software/sla/sladb.nsf/sla/csdsp?OpenDocument){: new_window}.

Per ulteriori informazioni sui prezzi, vedi il [catalogo {{site.data.keyword.discoveryshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/catalog/services/discovery){: new_window}.

## Note per i clienti con piani esistenti
{: #pricingnotes}

- A partire dal **1° agosto 2018**, la tua fatturazione e il tuo utilizzo saranno basati su questo piano di prezzi.
- Il piano Lite è stato ridotto da 2.000/400 query {{site.data.keyword.discoverynewsshort}} al mese a 1.000 documenti/200 query {{site.data.keyword.discoverynewsshort}} al mese.  Se già hai superato i nuovi limiti del piano Lite, non puoi aggiungere ulteriori documenti. Puoi tuttavia continuare a utilizzarlo oppure puoi eseguire un upgrade a un piano Advanced o Premium.
- Il piano Standard è stato ritirato e non sarà più disponibile per i nuovi utenti. Se sei attualmente su un piano Standard esistente, puoi continuare a usarlo oppure puoi eseguire un upgrade a un piano Advanced o Premium.
- I piani Advanced e Premium sono ora basati su livello di documento; non sono più basati sulle ore di documento. La tua fatturazione mensile non varierà in base al numero di documento a meno che tu non passi da un livello a un altro.
- I clienti Premium sono invitati a contattare il reparto [Vendite ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.biz/contact-wdc-premium){: new_window} per i dettagli relativi alle modifiche alla fatturazione.	
