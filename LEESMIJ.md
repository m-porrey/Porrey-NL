# Website porrey.nl

Cloudflare Pages-project voor porrey.nl. Zelfde opzet als boshuisje-oisterwijk: GitHub → Cloudflare Pages, contactformulier via Web3Forms.

## Inhoud

| Bestand | Wat |
|---|---|
| `index.html` | De hele website (opmaak en werking zitten erin) |

## Online zetten

1. Maak op github.com een nieuwe repository, bijvoorbeeld `porrey-nl` (privé mag).
2. Upload `index.html` en `LEESMIJ.md` (Add file > Upload files).
3. Cloudflare: Workers & Pages > Create > Pages > Connect to Git > kies de repository.
   - Framework preset: None
   - Build command: leeg laten
   - Build output directory: `/`
4. Domein naar Cloudflare halen (porrey.nl staat nu nog bij Interip):
   - Cloudflare: Add a domain > `porrey.nl` > Free plan.
   - Controleer in de ingelezen DNS-lijst de MX-records (SpamExperts) en TXT/SPF-records. Neem ontbrekende records over uit het Interip-paneel. Dit vóór de volgende stap, anders valt de mail weg.
   - Interip: zet de nameservers van porrey.nl op de twee nameservers die Cloudflare geeft.
5. Als Cloudflare het domein als actief meldt: Pages-project > Custom domains > Set up a custom domain > `porrey.nl`, en daarna ook `www.porrey.nl`.

Wijzigingen: pas `index.html` aan in GitHub (potloodje), Cloudflare zet het binnen een minuut online.

## Contactformulier

Gebruikt dezelfde Web3Forms-sleutel als het boshuisje. Berichten komen met als onderwerp "Nieuw bericht via porrey.nl" in je mailbox.
Andere sleutel nodig? Maak er een aan op web3forms.com en vervang de waarde van `access_key` in `index.html`.

## Talen

De site is er in het Nederlands, Engels, Duits en Frans. Bezoekers kiezen rechtsboven; de browsertaal bepaalt de eerste keuze.
Direct linken naar een taal: `porrey.nl/#en`, `#de` of `#fr`.
Teksten aanpassen: Nederlands staat in de HTML zelf, de andere talen onderaan in `index.html` bij `const T`.
In het contactbericht zie je in het veld `taal` welke taal de afzender gebruikte.

## Nog in te vullen


- Foto's van motoren en skyrunning
- Stamboom zodra die er is
