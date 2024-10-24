# Tailwind CSS in HTML einrichten

- [Offizielle Dokumentation](https://tailwindcss.com/docs/installation)
- [Kool Tailwind Componente für ALLE DEINE FANTASIEN](https://tailwindflex.com/)
- [Cheatsheet Für Tailwind](https://tailwindcomponents.com/cheatsheet/)

---

## Hier sind die Schritte, um Tailwind CSS in einem HTML-Projekt einzurichten:

1. Erstelle dein `index.html`-Datei wie gewohnt.
2. Erstelle ein `style.css`-Datei und verlinke sie in deinem `index.html`-Dokument.
3. Erstelle eine `tailwind.css`-Datei.
   ```html
   <link rel="stylesheet" href="style.css" />
   ```
4. Füge die folgenden Zeilen im VSCode `Terminal` ein:

   ```bash
   npm init -y
   npm install -D tailwindcss
   npx tailwindcss init
   ```

   - `npm init -y` erstellt eine `package.json`-Datei. **(Optional) - Du kannst diese Datei öffnen und die `name`, `version`, `description`, `author`, etc. ändern.**
   - `npm install -D tailwindcss` installiert Tailwind CSS.
   - `npx tailwindcss init` erstellt eine `tailwind.config.js`-Datei.

5. Offne die `tailwind.config.js`-Datei und ersetze den Zeil `content: []` mit:
   ```js
   content: ["./**/*.html"],
   ```
   - Diese Zeile sagt Tailwind CSS, dass es alle HTML- und JS-Dateien im Projekt durchsuchen soll.
6. Füge die folgenden Zeilen in deiner `tailwind.css`-Datei ein:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```
7. Füge die folgenden Zeilen in deiner `package.json`-Datei im `scripts`-Abschnitt ein:

   ```json

     "dev": "npx tailwindcss -i ./tailwind.css -o ./style.css  --watch"

   ```

   - Diese Zeilen sagen Tailwind CSS, dass es die `tailwind.css`-Datei in die `style.css`-Datei kompilieren soll.

8. Führe den folgenden Befehl im `Terminal` aus:
   ```bash
    npm run dev
   ```
9. Füge ein Testelement in deinem `index.html`-Dokument ein:

```html
<div class="bg-blue-500 text-white p-4">Hello World!</div>
```

11. Öffne dein `index.html`-Dokument im Browser (mit dem `Live Server`-Plugin, wenn du möchtest) und überprüfe, ob das Testelement korrekt angezeigt wird.

12. Erstelle eine `.gitignore`-Datei und füge die folgenden Zeilen ein:

    ```
    node_modules

    package-lock.json
    ```

13. Viel Spaß beim Coden mit Tailwind CSS!
