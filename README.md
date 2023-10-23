  ## Drive with Avada

n.b. per i numeri delle sezioni si fa riferimento allo schema pubblicato in public/schema-app/Schema-App-Drive-With-Avada.jpg

- Organizzazione dei Componenti:
dopo l'analisi del layout, ho definito i macro-componenti dell'App, come Header.vue, Main.vue e Footer.vue. Li ho posizionati nelle cartelle corrispondenti all'interno della directory "components". Ho anche creato una cartella "partials" per i micro-componenti ricorrenti del sito.

- Stile e Design:
ho identificato elementi comuni in termini stilistici e ho creato la cartella "scss" contenente un file principale chiamato "main". Questo file include istruzioni generali del sito (contenute in "_generals.scss") e variabili per la palette colori e i font.

- Header:
ho strutturato il componente Header, che include una navbar inizialmente statica.

- Main Section:
ho suddiviso il componente Main in 8 sezioni.
Per la sezione 2 (SectionForm), ho collegato un componente Form.
Nella sezione 3 (SectionStartCourses), ho inserito i componenti CoursesInfo e LearnMore, collegandoli tramite props e ciclando su un array definito in "Data/cardCourses.js".

- Card Components:
per la sezione 4 e 5, ho creato un componente "GenericCard" per gestire le cards simili. Questo componente riceve proprietà diverse in base al contenuto della card. Ho gestito la difficoltà nell'inserire il range utilizzando un elemento grafico modificato, passando la prop "percentage".

- Testimonials Section:
Ho implementato un carosello per la sezione Testimonials, con una serie di pallini generati dinamicamente. Ho creato un file .js con un array di persone e citazioni, implementando un metodo per nascondere l'immagine precedente ad ogni interazione.

- Latest News Section:
Ho riutilizzato lo stile della card per la sezione Latest News, creando un file con l'array "news.js".

- Call to Action Button:
Prima di arrivare al footer, ho creato un componente "BtnCta" (bottone call to action) con una prop "text", per poterlo inserire in diverse parti del sito.

- Footer:
Ho strutturato il footer, utilizzando il file "navsMenu.js" per rendere dinamiche le navigazioni, con array distinti per l'header e i due menù del footer.

- Ho creato un file .js per gestire i social della pagina, con array distinti per la sezione degli istruttori e il footer.
Dettagli Grafici:

- Ho lavorato su elementi grafici minori, come la freccia "chevron" nel footer e i pulsanti in alto a destra.


      