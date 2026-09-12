## Ülesanne 3 — Kaskaad, kihid ja disainižetoonid

### Spetsiifilisuse tabel
| spetsiifilisus | selektor / märkus                |
| :------------- | :------------------------------- |
| `0-1-0`        | `.valja` (raamistik)             |
| `0-1-0`        | `.valja` (meie) — SAMA           |
| `0-2-0`        | `.leht .valja`                   |
| `0-0-0`        | `:where(h1, h2, h3)` (lahtestus) |
| `0-0-1`        | `:is(h2, h3)` (rühm)             |
| `0-2-1`        | `.kaardid > li:not(...)`         |
| `1-1-0`        | `#ost .valja`                    |

### Miks kiht asendab !important-i
Kihtide järjekord (kaskaadikihid) võimaldab määrata reeglite prioriteete struktuurselt — hilisem kiht kirjutab varasema üle isegi siis, kui varasemal on suurem spetsiifilisus. See lahendab stiilide konflikte puhtalt ja loogiliselt, muutes `!important` kasutamise enamikul juhtudest tarbetuks.