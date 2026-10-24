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

## Bestel- en contactverzoeken

Contactberichten en bestelverzoeken worden via FormSubmit naar `robindorny61@gmail.com` gestuurd. Bij het eerste gebruik vraagt FormSubmit om het ontvangstadres te bevestigen; bevestig die activeringsmail voordat bezoekers het formulier gebruiken. FormSubmit verwerkt formuliergegevens. De contactmail staat daarom ook als endpoint in de openbare websitecode. Het winkelmandje verzendt alleen een vrijblijvend bestelverzoek met een prijsaanduiding. Er is geen betaling, voorraadbeheer of automatische orderbevestiging; bevestig beschikbaarheid, levering en prijs handmatig.

## Grenzen

GitHub Pages host de openbare site; de wachtwoordlogin en CMS-toegang lopen via Decap Turbo. Video's en liveopnames verschijnen zodra eigen links of opnames zijn toegevoegd. De contact- en bestelformulieren gebruiken FormSubmit als externe dienst.
