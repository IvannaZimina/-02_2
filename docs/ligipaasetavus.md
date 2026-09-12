# Ülesanne 1 - semantiline märgend ja ligipääsetavus

| paar                        | suhe    | AA (4,5:1) |
|-----------------------------|---------|------------|
| pohitekst valgel            | 17,40:1 | jah        |
| abitekst valgel             |  7,72:1 | jah        |
| fookuse aaris valgel        |  5,98:1 | jah        |

## Mida automaatkontroll EI leia
  kas alt-tekst on ÕIGE - "pilt123.jpg" läbib kontrolli
  kas fookusjärjekord on LOOGILINE
  kas maamärkide jaotus on mõttekas
  kas aria-label on kasutajale arusaadav

## Ülesanne 2 — Ostuvorm ja valideerimine

### teade() kontrollitud juhtumid
* **tühi kohustuslik väli** -> "See vali on kohustuslik."
* **vale e-posti kuju** -> "Kontrolli e-posti aadressi kuju."
* **minlength=2** -> "Vähemalt 2 tähemärki."
* **max=6** -> "Suurim väärtus on 6."
* **tundmatu põhjus** -> brauseri oma teade
* **valueMissing + typeMismatch** -> kohustuslikkus võidab (kuna tühja välja kuju ei loeta)

### Valijate võrdlus (:invalid vs :user-invalid)
| valija          | millal kehtib                   |
| :-------------- | :------------------------------ |
| `:invalid`      | KOHE lehe avamisel              |
| `:user-invalid` | alles pärast väljaga tegelemist |