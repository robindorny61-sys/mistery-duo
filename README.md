# MISTERY DUO

Een responsive website met HTML, CSS en JavaScript. De openbare pagina leest de bewerkbare inhoud uit `content/site.json`. Het beheerportaal staat in `admin/` en gebruikt Decap CMS met de beheerde Decap Turbo GitHub-backend.

## Lokaal bekijken

Start in de projectmap `python -m http.server 8000` en open `http://localhost:8000`. De site leest dan de inhoud uit `content/site.json`. De admin kan pas aanmelden nadat Decap Turbo en de repository zijn gekoppeld.

## Beveiligde admin activeren

De wachtwoordlogin loopt via Decap Turbo. Een wachtwoord wordt niet in de websitecode opgeslagen. Decap Turbo beheert de login en geeft het CMS via zijn GitHub-app toegang tot de gekoppelde repository.

1. Maak een account aan bij Decap Turbo en maak een organisatie aan.
2. Verbind GitHub met de organisatie door de Decap Turbo GitHub-app te installeren voor deze repository.
3. Maak in Turbo een site aan met deze repository, branch `main`, configpad `admin/config.yml` en de exacte gepubliceerde URL van `/admin/`.
4. Kopieer de Site ID uit het siteoverzicht en vervang `VUL_HIER_DE_DECAP_TURBO_SITE_ID_IN` in `admin/config.yml`.
5. Commit en push de wijziging. Zodra GitHub Pages heeft gepubliceerd, open je `https://<jouw-site>/admin/` en meld je aan met je Decap Turbo e-mailadres en wachtwoord.
6. Nodig eventuele extra beheerders uit via de Decap Turbo-organisatie/site-instellingen.

De Site ID en de GitHub-appkoppeling zijn nog niet ingevuld, omdat ze pas worden aangemaakt in jouw eigen Turbo-account. Zonder die eenmalige accountkoppeling blijft `/admin/` gesloten en kan het CMS niet bij de repository. Controleer in Turbo de toegangsrechten en beperk de koppeling tot deze repository. De Turbo-documentatie vermeldt momenteel een gratis startplan voor een site en een gebruiker; extra gebruikers kunnen een ander plan vereisen.

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
