---
type: meta
tags: [meta, glosszárium, ocr]
---

# Glosszárium és OCR-normalizáló térkép

Kettős célú referencia:
1. **Kanonikus tulajdonnevek** — a világ visszatérő nevei, egységes írásmóddal.
2. **OCR-normalizálás** — a `source/full_codex.md` gyakori olvasási hibái és helyes alakjuk.

Ingestion közben ezt a listát bővítsd minden új tulajdonnévvel és felismert OCR-hibával.

## Kanonikus tulajdonnevek

| Kanonikus alak | Típus | Megjegyzés / aliasok |
|---|---|---|
| Abrýss | kontinens/birodalom | a fő szárazulat; OCR: „Abröss", „Abryss", „Abrïss", „Abýrss" |
| Nadýss | világ (glóbusz) | Abrýsst hordozó világ; OCR: „Nadjss" |
| Nîtor | hely | világok közti örvény középpontja |
| Sárkánygerinc Hegység | helyszin | Abrýss gerince |
| Abrýss Kelyhe | helyszin | belső édesvízű tenger |
| Zorawa | vallas | a Birodalom államvallása (Zorawa Miszticizmus) |
| Shinwa | vallas/fogalom | „Shinwa harmónia" |
| Nadîr | vallas/lény | „Nadîr, az Ős-Szellem"; Nadîr Királyság (régió) |
| Napcsászár | cím/szereplő | az Isteni Uralkodó; II. Napcsászár rendelete a rangokról |
| titoknokok | frakcio/szereplő | a Napcsászár szolgái, Zorawa nagymesterek |
| Shagîr | régió/sziget | Shagîri harciskola; OCR: „Shagîr", „Shagír" |
| Ardúnia | régió | dún nyelvű vidék |
| Goragar | régió/sziget | a gorgok lakják |
| Naisur | nép/régió | „Hatalmasságok" közt |
| ghodi | nep | alacsony, éles eszű lovasnép |
| kharag | nep | hatalmas termetű hegyibarbárok |
| nador | nep | hallgatag hegyinép; „Nagy Öreg" vezetőjük |
| gorg | nep | Goragar szigetének népe |
| moradok | nép/lény | az Óidőkben legyőzött lények |
| Khîrin | magia/fogalom | harci transz képessége |
| Óidők | korszak | a démonikus mágusbirodalmak kora |
| Óbirodalom / Közép-Birodalom / Új-Birodalom | korszak | az Óidők három démoni birodalma |
| Napcsászárok kora | korszak | i.e. 8. évezred körül |
| Sýtis | település | a tavak országának városa |
| Mîthis | település | Zorawa rejtett kolostorvárosa |
| Nemesi Házak (Nagy Házak) | frakcio | az „árnyékháborút" vívó nemesi dinasztiák |
| Nadîr, az Ős-Szellem | vallas/lény | bolygószellem; a nador kultusz; OCR: „Ós-Szellem" |
| Nadîr Királyság | régió | a nador nép hegyi királysága Abrýss nyugatán |
| Sápadt Vándor | fogalom/égitest | Nadýss megmaradt holdja, 12 naponta; „dagály" a mágiában |
| Ashvîl | fogalom/égitest | a lezuhant hold, a Közép-Birodalom pusztítója |
| Dún Birodalom (Dún vallás) | frakcio/vallas | elsöpörte a Napnyugati Démonikus Császárságot; Terra ni Mare központtal |
| kevert lények | leny | az Óidők mágusai által alkotott torz fenevadak |
| elveszett városok | helyszin | az Óidők építményei; „senki sem akarja megtalálni" |

### Feldolgozásra váró nevek (a „Világ Könyve", L1869-ből)

Salagas Hercegség, Yorsenar, Meldoa, Terra ni Mare, Úti Királyság, meldánok, Napudvar,
Shrîl-Ashra seregek, Carvis Ház (Sýtis), Tiltott Tartomány / Császári Kanton
meditációs kertjei, Tízezer Lépés Kertje, Álmok Csatornája, Miraclea obeliszkje
(mágiakioltó fennsík). — Ezekhez még nincs jegyzet; ingestkor dolgozandók fel.

## OCR-normalizálási szabályok

| Hibás alak | Helyes alak | Jelleg |
|---|---|---|
| `sten` (sor elején/önállóan) | `Isten` | levágott kezdőbetű |
| `id ` / `idó` / `id` | `idő` | ő→o/levágás |
| `túz`, `túz` | `tűz` | ű→ú |
| `súrú`, `súrűbb` | `sűrű`, `sűrűbb` | ű→ú |
| `húvös` | `hűvös` | ű→ú |
| `múve`, `múvészet` | `műve`, `művészet` | ű→ú |
| `Îátszik`, `À`, `Á` sor elején | `látszik`, `A`, `A` | téves diakritika |
| `碧`, `中`, `Td`, elszórt latin szemét | — | törlendő szemétkarakter |
| kötőjeles sortörés a szó közepén (`elkép-\nzelhetetlen`) | egybeírás | tördeléshiba |

> [!note] Az ű/ő betűket az OCR rendszeresen ú/ó alakban adja vissza. Magyar helyesírás
> szerint javítsd, de tulajdonnévnél óvatosan (a világ neveiben a `î`, `ý`, `â` szándékos).
