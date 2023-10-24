  ## Drive with Avada

n.b. per i numeri delle sezioni si fa riferimento allo schema pubblicato in public/schema-app/Schema-App-Drive-With-Avada.jpg

#### Organizzazione dei Componenti:

dopo l'analisi del layout, ho definito i macro-componenti dell'App, come Header.vue, Main.vue e Footer.vue. Li ho posizionati nelle cartelle corrispondenti all'interno della directory "components". Ho anche creato una cartella "partials" prevedendo i micro-componenti ricorrenti del sito.

#### Stile e Design:

ho identificato elementi comuni in termini stilistici e ho creato la cartella "scss" contenente un file principale chiamato "main". Questo file include istruzioni generali del sito (contenute in "_generals.scss") e variabili per la palette colori e i font.

### Header:

ho strutturato quindi il componente Header, che include una navbar inizialmente statica , ho omesso il bottone per il momento.

#### Main Section:

ho suddiviso il componente Main in 8 sezioni. 
Per la sezione 2 (SectionForm), ho collegato un componente Form.
Nella sezione 3 (SectionStartCourses), ho inserito i componenti CoursesInfo (la card) e LearnMore (serie di cards), collegandoli tramite props alla sezione e ciclando  in quest’ultimo un array definito in "Data/cardCourses.js".

#### Card Components:

per la sezione 4 e 5, ho creato un componente "GenericCard" per gestire le cards simili. Questo componente riceve proprietà diverse in base al contenuto della card. Ho gestito la difficoltà nell'inserire il range utilizzando un elemento grafico disponibile sul web, l’ho modificato, e passato tramite la prop "percentage".

#### Testimonials Section:

ho implementato un carosello per la sezione Testimonials, con un array di pallini stampati dinamicamente. Ho creato un file .js con un array di persone e citazioni, implementando un method e un bind della classe hide per nascondere l'immagine precedente ad ogni interazione.

#### Latest News Section:

ho riutilizzato lo stile delle card della sezione 4 e 5 per la sezione Latest News, in cui ho importato e ciclato l'array "news.js".

#### Call to Action Button:

prima di arrivare al footer, ho creato un componente "BtnCta" (bottone call to action) con una prop "text", per poterlo inserire in diverse parti del sito.

#### Footer:

ho strutturato il footer, utilizzando il file "navsMenu.js" per rendere dinamiche le navigazioni: vi sono array distinti per l'header e per il menù del footer.

ho quindi creato un file .js per gestire i social della pagina, con array distinti per la sezione degli istruttori e per il footer.

#### Dettagli Grafici:

Ho lavorato su elementi grafici minori, come la freccia "chevron" nel footer e i pulsanti in alto a destra.



      