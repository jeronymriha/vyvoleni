# Nový web

Jedna testovací úvodní stránka v češtině. Čisté HTML a CSS, bez externích knihoven, fontů nebo instalace závislostí. Stránka má responzivní rozložení pro mobil a počítač.

## Struktura

```text
test-web/
├── dist/
│   ├── index.html
│   └── assets/
│       └── styles.css
├── .gitignore
├── .gitattributes
└── README.md
```

## Lokální zobrazení

Otevřete soubor `dist/index.html` v prohlížeči. Není potřeba spouštět server ani build.

## Vložení do Git repozitáře

Zkopírujte obsah složky `test-web` do kořenové složky svého repozitáře včetně souborů začínajících tečkou. Složku `dist` také commitněte — obsahuje přímo hotový web.

Pokud začínáte s novým prázdným repozitářem, ve složce projektu můžete spustit:

```sh
git init
git add .
git commit -m "Add initial homepage"
git branch -M main
git remote add origin URL_VASEHO_REPOZITARE
git push -u origin main
```

`URL_VASEHO_REPOZITARE` nahraďte skutečnou adresou repozitáře. U existujícího repozitáře použijte jeho stávající větev a remote.

## Nasazení

V hostingu, který umožňuje publikovat statický web z Git repozitáře, nastavte:

- **Typ projektu / framework:** statický web, žádný framework.
- **Kořen projektu:** kořen repozitáře.
- **Build command:** ponechat prázdný (žádný build není potřeba).
- **Publish / output directory:** `dist`.
- **Větev:** vaše publikační větev, obvykle `main`.

Pokud hosting místo nastavení publikační složky požaduje webové soubory přímo v kořeni, vložte do publikačního kořene obsah `dist` (soubor `index.html` a složku `assets`). Konkrétní automatizační workflow není přiložené, protože závisí na zvoleném hostingu.

## Úpravy

- Obsah, název stránky a popis: `dist/index.html`.
- Barvy, rozložení a responzivní vzhled: `dist/assets/styles.css`.
- Favicon je vložený přímo v hlavičce HTML jako SVG.

Všechny odkazy na soubory jsou relativní, takže web může běžet také v podadresáři. Stránka nemá backend ani formulář a nepotřebuje proměnné prostředí.
