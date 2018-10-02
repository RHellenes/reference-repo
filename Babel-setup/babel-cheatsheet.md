# Babel Cheatsheet - Norsk

###### Steg for steg, hvordan sette opp babel i et prosjekt.

&nbsp;

Dette avhenger av at man har installert Node Package Manager [npm] for å kunne startes.

1. Sett opp en `package.json` fil ved å skrive `npm init` i root. Følg så stegene og fyll ut relevante felt.

   &nbsp;

1. Installer 'Babel command line' og 'Babel preset enviroment' npm packages

   ```git
   npm install babel-cli -D
   npm install babel-preset-env -D
   ```

   &nbsp;

1. Lag en **.babelrc** fil i prosjektet ditt og legg denne koden inn:

   ```git
   {
       "presets": ["env"]
   }
   ```

   &nbsp;

1. Legg følgende script inn i `package.json` filen:

   ```json
   "build": "babel js -d compiled"
   ```

   - **js** byttes ut med navnet på mappen du har javascript filene som skal kompileres i.
   - **compiled** byttes ut med navnet på mappen du vil ha de kompilerte filene i. Du trenger ikke å lage mappen før du kjører koden.

   Alt settes inn i `"scripts"`, etter `"test"` e.g:

   package.json:

   ```diff
   {
   "name": "form-option-component",
   "version": "1.0.0",
   "description": "Test case from Netlife Dialog",
   "main": "index.js",
   "scripts": {
       "test": "echo \"Error: no test specified\" && exit 1",
   +   "build": "babel js -d compiled"
   },
   ```

   **NB:** Husk `,` på slutten av `"test"`/ før du `"build"` begynner på neste linje.

   &nbsp;

1. Kjør `npm run build` når du vil kompilere koden din fra **js** til **compiled**
