# CODEX Codex — Világ-kompendium (Obsidian vault)

A **CODEX** strukturált, összelinkelt
tudásbázisa.

> A CODEX és világa **Nyulászi Zsolt és Szalkai László szellemi
> tulajdona**. Ez a vault nem hivatalos, rajongói feldolgozás; minden lore-jog a
> szerzőket illeti.

---

## Beállítás Obsidianban

1. **Klónozd a repót:**
   ```bash
   git clone git@github.com:dokker/obsidian-worldbuilding-codex.git
   ```
2. **Nyisd meg vaultként:** Obsidian → *Open folder as vault* → válaszd a klónozott
   mappát.
3. **Bízz meg a vaultban** (*Trust author and enable plugins*), ha kéri.
4. **Szinkron git-en át:** húzz `git pull --rebase` mindig, mielőtt commitolnál.
   A community pluginek (`.obsidian/plugins/`) nincsenek verziózva — ezeket
   Obsidianon belül telepítsd (pl. a *github-sync* plugint a szinkronhoz).

---

## Használat

### Új jegyzet sablonból

A `_Sablonok/` mappa típusonként tartalmaz sablont (Helyszín, Nép, Vallás, Mágia,
Frakció, Szereplő, Esemény, Korszak, Kultúra, Lény, Fogalom).

- **Templates plugin:** *Settings → Core plugins → Templates* engedélyezése, a
  *Template folder location* legyen `_Sablonok`. Ezután új jegyzetben:
  *Insert template* (parancspaletta) → válaszd a megfelelő sablont.
- Vagy: másold a megfelelő sablon tartalmát az új jegyzetbe.
- Az új jegyzetet a helyes mappába tedd (lásd `_Meta/Stílus-útmutató.md`).

### Konvenciók (kötelező)

- **Frontmatter** minden tartalmi jegyzetben: `type`, `aliases`, `tags`, `status`,
  `kanon`, `forras`, `ocr_bizonytalan`, `kapcsolodo`. Részletek:
  `_Meta/Stílus-útmutató.md`.
- **Minden állítás mögött forráshivatkozás** (`full_codex.md#Lx-Ly`) és kánon-bizalom
  (`biztos` / `bizonytalan` / `kikovetkeztetett`).
- **Ne találj ki kánont.** A következtetést jelöld, a hiányt „Nyitott kérdések" alá.
- A `[[wikilinkek]]` kötik össze a jegyzeteket; alias-okkal az OCR-változatok is
  megtalálhatók.

### Belépési pontok

- `00-Home.md` — főoldal, Maps of Content (MOC) szekciók.
- `_Meta/Ingest-napló.md` — feldolgozási állapot, következő teendő.
- `_Meta/Glosszárium.md` — nevek, OCR-javítások.
- `_Meta/Stílus-útmutató.md` — teljes konvenciógyűjtemény.

