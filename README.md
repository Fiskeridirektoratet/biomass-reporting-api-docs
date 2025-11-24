# Hjelp til innsending av biomasserapporter via API
Produksjonsmiljø for APIet er tilgjengelig på: https://api.fiskeridir.no/biomass-reporting-api-protected/swagger-ui/index.html


## Maskinporten og delegering av rettigheter for ulike aktører:

### Rapporteringspliktig som ønsker å sette opp integrasjon selv.

* Dere må opprette en integrasjon (en OAuth 2.0-klient) i Maskinporten med scope `fdir:biomassreportingapi`
* Se `https://samarbeid.digdir.no/maskinporten/ta-i-bruk-maskinporten/97` under “Konsument”.

### Rapporteringspliktig som ønsker å benytte en tjenesteleverandør

* Dere må gi “Tilgang til Programmeringsgrensesnitt - API” i Altinn til tjenesteleverandør.
* Søk og velg “Tilgang til API for biomasserapportering”
* Se `https://samarbeid.digdir.no/maskinporten/ta-i-bruk-maskinporten/97` under “Konsument - delegert til leverandør.”

### En tjenesteleverandør som vil tilby innsending for rapporteringspliktige

* Gjelder leverandør av fagsystem med integrasjon mot Fiskeridirektoratet’s APIer.
* Din kunde må ha tildelt API-tilgang i Altinn til leverandør.
* Leverandør av system må opprette en Maskinporten med scope `fdir:biomassreportingapi`.
* Samme klient kan brukes til å rapportere for flere kunder ved å endre `consumer_org` verdien.
* Se `https://samarbeid.digdir.no/maskinporten/ta-i-bruk-maskinporten/97` under “Leverandør”.

## Testmiljø:

Testmiljø for APIet er tilgjengelig på: https://testapi.fiskeridir.no/biomass-reporting-api-protected/swagger-ui/index.html

* For å teste rapportering av biomasse i testmiljøet må dere bruke en test-organisasjon. Vi benytter syntetiske organisasjoner fra Skatteetatens Tenor testdatabase `https://www.skatteetaten.no/testdata/`.
* Ta kontakt med oss for å få tildelt organisasjonsnummer som er tilknyttet tillatelser i akvakulturregisteret sitt testmiljø, og som brukes for pålogging i Samarbeidsportalen: `https://sjolvbetjening.test.samarbeid.digdir.no/login`.
* Det må opprettes egen Maskinporten klient i testmiljøet til Maskinporten. Logg inn i testmiljøet for Samarbeidsportalen og opprett klient for testorganisasjonen.
* For tjenestetilbydere må klienten opprettes for en syntetisk organisasjon som skal representere organisasjonen til tjenestetilbyderen. Organisasjonen til tjenestetilbyderen må også ha fått delegert tilgang i testmiljøet til Altinn av den som det skal rapporteres på vegne av.
* Rapportering av biomasse i testmiljøet krever bruk av gyldige lokaliteter i dette miljøet. Disse vil dere også få tildelt sammen med testorganisasjon av oss.

Kontakt epost: akva-hjelp@fiskeridir.no
