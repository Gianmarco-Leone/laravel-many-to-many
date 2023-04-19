<div align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a>
<h1><strong style="color: #EF3B2D;">9 + BOOTSTRAP TEMPLATE</strong></h1></div>

# Laravel Boolfolio

> Sistema di gestione del Portfolio dei miei progetti.

![Screenshot](./public/img/Screenshot_1.png)

## Descrizione:

Realizzazione progetto usando laravel breeze ed il pacchetto Laravel 9 Preset con autenticazione.

## Svolgimento

### Admin

Iniziamo con il definire il layout, `Model`, `Migration`, `Controller` e `Route` necessarie per il sistema portfolio:

1.  _Autenticazione_: si parte con l'autenticazione e la creazione di un layout per back-office.
2.  Creazione del modello Project con relativa `migration`, `seeder`, `controller` e `routes`
3.  Per la parte di back-office creiamo un _resource controller_ Admin\ProjectController per gestire tutte le operazioni CRUD dei progetti.
4.  Possibilità di cliccare sul titolo della colonna nella tabella Backoffice per visualizzare risultati in oridine crescente.
    Al successivo click, l'ordine si invertirà, e quello visualizzato sarà quindi decrescente.
    Di default l'ordine di visualizzazione è da quello con la modifica più recente in poi.
5.  Possibilità di allegare le immagini ai progetti come dei veri e propri file tramite il `Restore`. Se non viene caricata nessuna immagine o se fallisce l'upload, ne verrà visualizzata una di placeholder
6.  Creazione di una checkbox per decidere se pubblicare o meno un progetto, se e solo se il check è 'on' questo sarà visibile sul lato guest.
7.  Aggiunta di una nuova entità `Type`, con rispettive `CRUD`, che è in relazione one to many con i progetti.
8.  Aggiunta di una nuova entità `Technology`, con rispettive `CRUD`, che è in relazione many to many con i progetti.
9.  Aggiunta della `softDelete()` per avere un cestino dove spostare i record alla prima eliminazione. Dal cestino è poi possibile reinserire gli elementi nel DB o eliminarli definitivamente
    ![Screenshot](./public/img/Screenshot_trash.png)

### Guest

1.  Visualizzazione progetti lato client.
    ![Screenshot](./public/img/Screenshot_guest.png)
