# Conventies voor REST API's voor het onderwijs #

## Huidige berichtverkeer ##

### Beveiliging van berichtverkeer ###
Voor beveiligde berichtuitwisselingen in de onderwijsketens worden nu vaak
berichtuitwisselingen gebaseerd op de Edukoppeling standaard gebruikt.
Edukoppeling formuleert een aantal maatregelen voor veilige berichtuitwisseling:
  1. Berichten worden verzonden over http, beveiligd met TLS 1.0 of latere versie
  2. Berichten zijn SOAP 1.1 berichten, met als conventies
        1. De beoogd afzender en ontvanger worden als parameter opgenomen in
          respectievelijk de WSA:From-header en WSA:To- header (tenzij de afzender
          anonymous is)
        2. Berichten bevatten een timestamp van het moment van verzending
        3. Berichten kunnen optioneel worden ondertekend of geencrypt en
          ondertekend.
        4. PKIo certificaten worden gebruikt voor ondertekening en encryptie van de
          berichten.

Met deze maatregelen levert berichtverkeer over Edukoppeling een paar zekerheden
voor zender en ontvanger:
  1. Berichten die tussen verzender en ontvanger worden onderschept, kunnen niet
    worden gelezen
  2. Als de berichten ondertekend zijn: als de ondertekening intact is, is het
  bericht ongewijzigd en is het ook op deze manier door de afzender verzonden
  3. Als de berichten geencrypt zijn, kunnen ze alleen door de ontvanger worden
  gedecrypt
  3. De identiteit van de afzender in het certificaat is op een betrouwbare
  manier vastgesteld, en is volgens de conventies in het onderwijs ofwel een
  onderwijsinstelling, ofwel een SaaS leverancier die diensten levert namens een
  onderwijsinstelling.

### Structuur van berichten ###
Er zijn geen algemene afspraken over de opzet van berichten, standaard
structuren enzovoort. Elke individuele standaard bepaalt zijn eigen structuur,
en de betekenis van de elementen uit de berichten wordt in de documentatie van
de standaard toegelicht.

# Wensen voor REST berichten #

  1. (M) Beveiliging minstens op hetzelfde niveau als Edukoppeling, met dezelfde
  zekerheden
  2. (S) Generieke conventies over hoe de API's en berichtuitwisselingen zijn
  ingericht
  3. (S) Een zo precies mogelijke beschrijving van de syntax van de gebruikte
  berichten
  4. (C) Generieke afspraken over de semantek binnen de berichtvelden die
  gebruikt worden binnen het onderwijsdomein

De API-strategie van het programma [Aan de slag met de
omgevingswet](https://aandeslagmetdeomgevingswet.nl/digitaal-stelsel/documenten/documenten/api-uri-strategie/)
is opgezet om uit te groeien naar een landelijke conventie voor de opzet van
API's. Daarnaast geven verschillende documenten op het internet zicht op wat
er nodig is voor goed opgezette REST API's. We gebruiken hier de indeling van
[Restful API
strategy](https://github.com/restfulapi/api-strategy/blob/master/README.md) als
startpunt.

## Uitgangspunten ##

  1. We beschrijven *resource-georienteerde* REST API's in dit stuk.
  2. We sluiten aan bij internationale en algemene conventies op het gebied van
  REST en HTTP en aanverwante standaarden
  3. Ongeacht deze afspraken blijft in elk geval Postel's principe van robuuste
  communicatie van kracht: "wees conservatief in wat je doet, en liberaal in wat
  je accepteert van anderen."

## Granulariteit van de API ##

## HTTP methoden en return codes ##

## Voorwaardelijke requests en caching ##

## Fouten in validatie en verwerking ##

## URI conventies ##

## API Versies en compatibility ##

## Object representatie ##

## Pagineren ##

## Queries ##

## Media types ##

## Bulk en batch operaties ##

## Authenticatie en autorisatie ##

## Gegevensintegriteit en -beveiliging ##
