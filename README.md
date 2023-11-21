# proj-html-vuejs

## Cosa fare

Riprodurre il layout proposto solo in versione Desktop

## Tecnologie:

```sh
HTML/CSS/VueJs
```

Aggiungere Header e Footer con VueJs creando una struttura dati che consenta di inserire i link nelle navbar. Su questo non ci sono API da interrogare, ma create i dati a mano nel vostro js.

## Deadline

Giovedì 23/11 ore 18.00

---

---

---

# Commenti

## Header

- fixed
- logo / lista v-for + hover sottolista v-for / menù a comparsa(sx) + button

## Main

-> 7 sezioni

1. carosello
2. img + text
3. carosello con cards (hover)
4. cards v-for + click su btn cambia grafica (?)
5. 4 cards (hover) | titolo sfonfo fbfbfb
6. 3 cards con lista tutte uguali (hover che gira con info)
7. 4 cards (hover) | titolo sfondo fbfbfb

## Footer

- 2 macro sezioni verticali (contenuto e diritti)

- footer-top 3 sezioni:

1. info Gobike
2. mini form
3. 2 liste flexate

## Altro

- modificare cursor
- scrollbar nera consfondo bianco
- btn che risale la pagina sfondo nero icona bianca

---

---

---

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

# Scaffolding progetto

## Se creo prima repo

- clona la repo dentro cartella esercizi
- apro la cartella in vs code
- digitare:

  ```sh
    npm create vue@latest
  ```

  alla prima domanda sul nome del progetto mettere un punto ad indicare che il progetto è quello della cartella corrente

  alla seconda domanda 'pacckage-name' inserire il nome del progetto ovvero lo stesso nome della repo

  proseguire rspondndo sempre no

- digitare:
  ```sh
      npm install
  ```
- per controllare che tutto funziona far partire il server
  ```sh
      npm run dev
  ```
- per arrestare il server:

```sh
        ctrl + c
```

## Se creo prima progetto

- apro la cartella degli esercizi in vs code
- digitare:

  ```sh
    npm create vue@latest
  ```

  alla prima domanda sul nome del progetto mettere il nome della repo

  proseguire rspondendo sempre no

  mi porto dentro la cartella creata:

  ```sh
        cd  nome repo
        code . -r
  ```

- digitare:
  ```sh
      npm install
  ```
- per controllare che tutto funziona far partire il server
  ```sh
      npm run dev
  ```
- per arrestare il server:

```sh
        ctrl + c
```

Se tutto funziona pusho su github

## Pulizia dello scaffolding

- Apro App.vue e cancello tutto e scrivo il mio codice in modalità 'options'
- Apro la cartella components e la svuoto
- Apro la cartella assets svuoto tutto tranne main.css
- Cancello tutto il contenuto del main.css e lo rinomino in main.scss
- creo in assets le cartelle images e styles
- sposto dentro la cartella styles main.scss
- aggiorno il path a main.scss in main.js
- aggiungo eventuale cartella immagini a public
- aggiungo dentro la cartella styles una cartella partials per i file partial scss (es. varibili, animazioni, mixins, ecc)

##Installare dipendenze

```sh
        npm install -D sass
```

```sh
        npm install bootstrap axios  @fortawesome/fontawesome-free
```

- importo bootstrap dentro main.scss @import 'bootstrap/scss/bootstrap';
