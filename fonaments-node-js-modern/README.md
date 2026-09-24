# Activitat 2 · JavaScript modern

Inventari i préstecs de material de l'aula. Bloc 1 · Sense IA.

## Posada en marxa

1. Descomprimeix aquest fitxer a la carpeta del curs (`node-curs/`), al costat de `fonaments-node/`. Es crearà la carpeta `fonaments-node-js-modern/`.
2. Comprova que tens aquesta estructura:

```
node-curs/
├── fonaments-node/            ← Activitat 1
└── fonaments-node-js-modern/  ← Activitat 2
    ├── README.md
    ├── package.json
    ├── .gitignore
    ├── antic.js
    ├── punt-control-3.md
    └── data/
        ├── material.json
        └── material.original.json
```

3. Obre la carpeta a VS Code i, al terminal integrat, crea el repositori:

```
git init
git add .
git commit -m "Activitat 2 · Punt de partida"
```

4. Executa-ho tot des de l'arrel de `fonaments-node-js-modern/`:

```
node antic.js
```

## Les dades

`data/material.json` és un array amb 12 elements de l'inventari. Cada element té:

| Camp | Descripció |
|---|---|
| `id` | Identificador únic (UUID) |
| `codi` | Codi d'inventari (`INV-2026-0001`) |
| `nom` | Nom de l'element |
| `tipus` | `portatil`, `tauleta`, `projector`, `cable` o `altres` |
| `aula` | On es guarda |
| `valor` | Valor en euros (compte: n'hi ha un que val 0) |
| `estat` | `disponible`, `prestat` o `avariat` |
| `prestatA` | A qui s'ha prestat (només si està prestat) |
| `dataPrestec` | Quan s'ha prestat (només si està prestat) |
| `dataAlta` | Quan es va donar d'alta |

Si modifiques `material.json` i vols tornar a començar, restaura'l (també funciona a PowerShell):

```
cp data/material.original.json data/material.json
```

## Exercicis

Tots els fitxers es creen a l'arrel de `fonaments-node-js-modern/`. Un commit per pas.

| Pas | Fitxers que has de crear |
|---|---|
| 0 · Repte diagnòstic | `modern.js` |
| 1 · const, let, arrow functions i template literals | `valors.js` |
| 2 · Destructuring, rest i spread | `fitxa.js` |
| 3 · `?.` i `??` | `punt-control-3.md` (omplert), `disponibilitat.js` |
| 4 · Mètodes d'array | `filtres.js`, `cerca.js`, `estadistiques.js` |
| 5 · JSON i fitxers | `alta.js`, `prestec.js`, `retorn.js` |
| 6 · Mòduls | `material.js` (opcional: `material.mjs`, `prova-esm.mjs`) |
| Repte final (opcional) | `inventari.js`, `material.test.js` |
| Ampliació | carpeta `ampliacio/` |

El recorregut mínim és del Pas 0 al Pas 6. El que està marcat com a opcional suma punts extra.

El `package.json` ja té l'script de tests: `npm test` executa tots els fitxers `*.test.js`.

## Avaluació

| Criteri | Punts |
|---|---|
| Funcionament (Pas 0 a Pas 6) | 3 |
| JavaScript modern | 3 |
| Validacions i errors | 1,5 |
| Mòdul `material.js` | 1,5 |
| Git i lliurament | 1 |
| Extra: repte `inventari.js` (+0,5) i tests que passen (+0,5) | fins a +1 |

Lliurament: un `.zip` de `fonaments-node-js-modern/` amb la carpeta `.git` i sense `node_modules/`.

## Normes

- Tot a mà: pots consultar nodejs.org/docs i developer.mozilla.org, però **sense IA**.
- Cap script ha de petar sense arguments: sempre un missatge d'ús.
- Abans de lliurar, restaura `material.json`.
