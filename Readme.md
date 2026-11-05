# 🛠️ Hub d'Eines Web (`eines`)

Col·lecció d'eines web modulars de processament local. Totes les utilitats s'executen directament al navegador (**client-side**), garantint la privacitat total de les dades (cap informació s'envia a servidors externs).

Desplegat automàticament amb **GitHub Pages**.

---

## 📂 Estructura del Repositori

```text
eines/
├── index.html                           # Menú principal i catàleg d'eines
├── README.md                            # Documentació del projecte
└── eines/                               # Carpeta amb les utilitats
    └── gestor-tasques-excel/            # Eina 1: Consolidador de Tasques Excel
        └── index.html
```

---

## ➕ Com Afegir una Nova Eina (Pas a Pas)

Per afegir una nova funcionalitat al projecte, només cal seguir aquests 3 passsos:

### 1. Crear la carpeta de la nova eina
Dins de la carpeta `eines/`, crea una subcarpeta amb el nom de la teva utilitat (fes servir minúscules i guions):
```text
eines/nom-de-la-teva-eina/
```

### 2. Afegir el codi de l'eina
Dins d'aquesta nova carpeta, crea un fitxer anomenat `index.html` amb tot el codi (HTML, CSS i JavaScript) de la nova funcionalitat.

> **Consell:** Inclou un botó a la capçalera de la nova eina per poder tornar còmodament al menú principal:
> ```html
> <a href="../../" class="text-xs text-slate-600 hover:text-brand-500 font-medium flex items-center space-x-1 border border-slate-200 px-3 py-1.5 rounded-lg hover:bg-slate-50 transition-colors">
>     <i class="fa-solid fa-house"></i>
>     <span>Tornar al Hub</span>
> </a>
> ```

### 3. Registrar l'eina al menú principal
Obre el fitxer `index.html` de l'arrel del repositori i afegeix una nova targeta com aquesta dins del grid (`<div class="grid ...">`):

```html
<!-- Nova Eina -->
<a href="./eines/nom-de-la-teva-eina/" class="group bg-white p-6 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md hover:border-brand-500 transition-all flex flex-col justify-between">
    <div>
        <div class="w-12 h-12 rounded-xl bg-blue-50 group-hover:bg-brand-500 text-blue-600 group-hover:text-white flex items-center justify-center transition-colors mb-4">
            <i class="fa-solid fa-wand-magic-sparkles text-2xl"></i>
        </div>
        <h3 class="font-bold text-slate-800 group-hover:text-brand-500 text-base mb-2 transition-colors">
            Nom de la Nova Eina
        </h3>
        <p class="text-xs text-slate-500 line-clamp-3">
            Descripció breu de la funcionalitat que realitza aquesta eina.
        </p>
    </div>
    <div class="mt-4 pt-4 border-t border-slate-100 flex items-center justify-between text-xs font-semibold text-brand-500">
        <span>Obrir eina</span>
        <i class="fa-solid fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
    </div>
</a>
```

---

## 🚀 Desplegament

En fer `git push` o guardar els canvis a la branca `main`, GitHub Pages actualitzarà el lloc web automàticament en 1-2 minuts.

---

## 🔒 Privacitat i Seguretat

- Tot el processament de fitxers (Excel, imatges, text, etc.) es realitza en la memòria RAM local del dispositiu utilitzant JavaScript.
- No s'utilitzen bases de dades externes ni APIs de tercers que emmagatzemin dades.