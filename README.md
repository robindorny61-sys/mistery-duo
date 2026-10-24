# MISTERY DUO

Een responsive website met HTML, CSS en JavaScript. De openbare pagina leest de bewerkbare inhoud uit `content/site.json`. Het beheerportaal staat in `admin/` en gebruikt Decap CMS met de beheerde Decap Turbo GitHub-backend.

## Lokaal bekijken

Start in de projectmap `python -m http.server 8000` en open `http://localhost:8000`. De site leest dan de inhoud uit `content/site.json`. De beheerlogin is ingesteld voor de gepubliceerde admin-URL; lokaal gebruik vereist dat lokale URL ook in de Turbo-site-instellingen wordt toegelaten.

## Beveiligde admin

De admin is beschikbaar op [de live beheerpagina](https://robindorny61-sys.github.io/mistery-duo/admin/). Meld je aan met je Decap Turbo-account. De websitecode bevat geen wachtwoord. Decap Turbo verwerkt de login; de GitHub-app is beperkt geïnstalleerd voor `robindorny61-sys/mistery-duo`.

De CMS-configuratie gebruikt branch `main` en `admin/config.yml`. Wijzigingen en afbeeldingen die via het CMS worden gepubliceerd, worden naar de repository geschreven; GitHub Pages publiceert daarna de bijgewerkte website. Voor extra beheerders gebruik je de leden- en toegangsinstellingen van de Turbo-organisatie/site.

## Wat via de admin kan worden aangepast

- Sitenaam en logo.
- Home-, video-, live-, shop-, over-ons- en contactteksten.
- Videolijst met categorie, duur en videolink.
- Liveoptredens met titel, datum, locatie en opnamelink.
- Productlijst met naam, voorbeeldprijs, beschrijving en afbeelding.
- Portret en afbeeldingen. Uploads worden in `images/uploads/` in de repository geplaatst.

Publiceren via het CMS commit inhoud en afbeeldingen naar de gekoppelde branch; GitHub Pages publiceert de bijgewerkte statische site daarna.

## Grenzen

GitHub Pages kan de openbare site hosten; de wachtwoordlogin en beveiligde wijzigingstoegang worden geleverd door Decap Turbo. De contactpagina valideert invoer, maar verstuurt of bewaart geen berichten. Koppel daarvoor een backend of formulierdienst. Het mandje is een lokale demo; bestellen, voorraad en betalingen vragen een e-commercebackend en betaalprovider. Video's worden via aangeleverde links afgespeeld; er is geen video-upload of hostingdienst gekoppeld.
