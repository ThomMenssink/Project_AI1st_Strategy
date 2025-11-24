# Inpact AI-First Master Maturity Model  
_Focus: Inpact Insurance Platform (IIP), schadeverzekeringen, volledige keten advies → verzekeren → schadeafhandeling_  
> Let op: dit model bevat nog nuances die verder aangescherpt en gevalideerd moeten worden in vervolgsessies.

---

## Doel van het model

- Gecontroleerd en respectvol uitfaseren van de “vertrouwde software” (legacy van twee bedrijven, meerdere producten per bedrijf).
- IIP als AI-first insurance platform neerzetten voor de **volledige keten**:
  - advies/orientatie  
  - offerte  
  - bind/polis  
  - administratie  
  - schadeafhandeling  
- Silo’s in structuur, techniek, data en teams structureel voorkomen.
- SDLC ontwikkelen richting een **AI SDLC Factory** (vergaande AI-automatisering van het ontwikkelproces).
- Consistent aansluiten op **LeSS** en **DevOps/CI-CD**.

---

## Overzicht van het model

### Niveaus (4)

0. Dual-Legacy Chaos  
1. IIP Foundation (Product & Chain)  
2. IIP Integrated Value Chain  
3. AI-First Insurance Ecosystem (IIP-centrisch, post-legacy)

### Dimensies (6)

1. Propositie & Productcatalogus (Insurance Product Factory)  
2. Waardeketen & Proces (advies → verzekeren → schade)  
3. Architectuur & Data  
4. Teams & Operating Model (LeSS / anti-silo)  
5. SDLC & AI Factory (DevOps + AI-automatisering)  
6. Klant & Ecosysteem (verzekeraar–volmacht–adviseur)

---

## Level 0 – Dual-Legacy Chaos (huidige spanningsveld)

### 1. Propositie & Productcatalogus

- Producten zitten opgesloten in de vertrouwde software van twee bedrijven.
- Per systeem en per klant bestaan varianten en afwijkingen.
- Time-to-market is traag en sterk afhankelijk van maatwerk.

### 2. Waardeketen & Proces

- Keten **advies → offerte → polis → schade** is niet end-to-end ontworpen.
- Veel handovers tussen systemen, afdelingen en teams.
- Geen uniforme keten-definitie die voor alle klanten/volmachten geldt.

### 3. Architectuur & Data

- Twee legacy-stapels met meerdere producten per stapel.
- Data is verspreid, deels redundant en inconsistent per product/klant.
- Er is geen centraal ketenmodel of productmodel dat als “bron van waarheid” fungeert.

### 4. Teams & Operating Model (LeSS)

- Teams zijn historisch gegroepeerd rond systemen/producten.
- LeSS-principes zijn gedeeltelijk toegepast, maar feitelijk bestaan er nog product- en techniek-silo’s.
- Coördinatie loopt via PO’s/architecten met risico op micro-silo’s.

### 5. SDLC & AI Factory

- CI/CD en DevOps worden toegepast, maar niet volledig uniform over alle producten.
- AI speelt nog een beperkte rol in de SDLC-automatisering.
- Er is geen expliciete AI SDLC Factory-visie over de volledige keten.

### 6. Klant & Ecosysteem

- Volmachten en adviseurs ervaren “software plus maatwerk”, geen coherent platform.
- Integraties met verzekeraars/adviseurs zijn vaak point-to-point opgebouwd.
- IIP is meer ambitie en concept dan realiteit.

---

## Level 1 – IIP Foundation (Product & Chain)

_Doel (globaal jaar 1): één IIP-fundament voor schade en eerste eenduidige ketenintegratie._

### 1. Propositie & Productcatalogus

- IIP introduceert een **centrale schade-productcatalogus**:
  - dekking
  - clausules
  - premiestructuren
  - productvarianten
- Producten worden modulair gedefinieerd (configuratie) in plaats van in code verstopt.
- Nieuwe producten gaan alleen nog via het IIP-productmodel.

### 2. Waardeketen & Proces

- Er wordt een eenvoudige maar uniforme blueprint van de keten vastgesteld:
  - prospect  
  - advies/orientatie  
  - offerte  
  - akkoord/bind  
  - polisbeheer  
  - schadeafhandeling (basale “happy flow”)
- IIP dekt eerst de standaard, minder complexe ketenvarianten.

### 3. Architectuur & Data

- IIP wordt neergezet als **platform** met:
  - productengine (productcatalogus)  
  - keten-engine (workflow, businessregels)  
  - integratielaag (API’s naar legacy en externe partijen)
- Eén eerste schade-datamodel wordt gedefinieerd als doelplaat.
- Mapping-tabellen naar de vertrouwde software worden ingericht.

### 4. Teams & Operating Model (LeSS)

- LeSS-productdefinitie: **“IIP Schadeketen”** als één product.
- Teams worden gegroepeerd rond waardeketen-segmenten in plaats van systemen, bijvoorbeeld:
  - Advies & Offerte-team  
  - Polis & Mutatie-team  
  - Schade Intake-team
- Er is één Product Backlog en één end-to-end Product Owner/CPO-lijn; geen losse backlogs per systeem.

### 5. SDLC & AI Factory

- Eén uniforme CI/CD-pipeline wordt verplicht voor alle IIP-teams.
- Testautomatisering wordt expliciet versterkt (shift-left).
- AI ondersteunt eerste stappen:
  - testgeneratie
  - code review
  - documentatie
- Doel wordt vastgelegd: binnen 3 jaar een duidelijk percentage SDLC-activiteiten AI-ondersteund.

### 6. Klant & Ecosysteem

- IIP exposeert eerste API’s naar volmachten en adviseurs:
  - met name offerte- en polisfunctionaliteit via productcatalogus + keten-blueprint.
- Legacy blijft volledig operationeel; IIP loopt ernaast als nieuw spoor.
- Nieuwe klanten/features worden, waar mogelijk, al via IIP gedaan.

---

## Level 2 – IIP Integrated Value Chain (advies → schade)

_Doel (globaal jaar 2): end-to-end schadeketen grotendeels via IIP; legacy is nog nodig, maar niet leidend._

### 1. Propositie & Productcatalogus

- Alle nieuwe schadeproducten worden **exclusief** via de IIP-productfactory ingericht.
- Producten zijn parametriseerbaar:
  - dekkingen  
  - distributiekanalen  
  - volmacht- en verzekeraarspecifieke varianten
- Time-to-market wordt drastisch verkort (weken i.p.v. maanden, streefwaarden worden gedefinieerd).

### 2. Waardeketen & Proces

- IIP orkestreert nu de volledige keten:
  - advies → productmatching → offerte → bind → polisbeheer → schadeafhandeling
- Ketenregels en businesslogica zijn gecentraliseerd en configureerbaar:
  - keten-sjablonen per type verzekeraar/volmacht
  - varianten per distributiekanaal (adviseur, direct, etc.)

### 3. Architectuur & Data

- IIP wordt de **primaire** keten-engine; vertrouwde software wordt gevoed door IIP of afgebouwd.
- Event-driven architectuur:
  - belangrijke ketenacties genereren events (offerte aangemaakt, polis gebonden, schade gemeld, uitkering gedaan).
- Er is één geïntegreerd datamodel voor:
  - klant  
  - polis  
  - risico  
  - schade  

### 4. Teams & Operating Model (LeSS)

- Teams zijn nu daadwerkelijk **stream-aligned** rond ketenstromen, bijvoorbeeld:
  - “Van advies tot polis”  
  - “Van polis tot schade-uitkering”
- Een platform-/productcatalogus-team levert generieke bouwblokken:
  - productconfiguratie  
  - tariefmotor  
  - workflowcomponenten
- Anti-silo principe:
  - geen team beheert een “eigen product-silo”; teams dragen ketenverantwoordelijkheid.

### 5. SDLC & AI Factory

- AI wordt standaard in SDLC gebruikt voor:
  - analyse van requirements → AI-voorstellen voor user stories  
  - genereren van ketenbrede testscenario’s  
  - statische code-analyse + refactoring-suggesties  
- DORA-metrics worden actief gestuurd, onder andere:
  - time-to-change productconfiguratie  
  - time-to-fix ketenissues  
  - deployment frequency per ketenstroom

### 6. Klant & Ecosysteem

- Volmachten en adviseurs interacteren via IIP-API’s of IIP-portalen:
  - allemaal op basis van dezelfde productcatalogus en ketenlogica.
- Verzekeraars koppelen hun backoffice aan IIP als “front”-platform richting advies/volmacht.
- IIP wordt zichtbaar als platform in plaats van als set losse applicaties.

---

## Level 3 – AI-First Insurance Ecosystem (IIP-centrisch, post-legacy)

_Doel (post-migratie): IIP is hét AI-first schadeplatform voor de volledige keten; vertrouwde software is uitgefaseerd of minimaal passief._

### 1. Propositie & Productcatalogus

- Productcatalogus is AI-enabled:
  - AI ondersteunt tariefvoorstellen  
  - AI suggereert dekkingscombinaties en personalisaties per segment
- Productontwikkeling is data-gedreven:
  - real-life performance data uit advies, aanbod, acceptatie en schade.

### 2. Waardeketen & Proces

- De keten is **self-optimizing**:
  - AI ondersteunt advies (next best product, next best action).  
  - Straight-through-processing van standaardschades.  
  - Complexe schades worden door experts behandeld met AI-assistentie.
- De klantervaring is end-to-end gemonitord:
  - bottlenecks in de keten worden automatisch gesignaleerd  
  - experimenten (A/B, canary) op ketenniveau zijn standaard.

### 3. Architectuur & Data

- IIP is volledig event-driven; alle ketenacties produceren events waar AI en analytics op draaien.
- Data wordt georganiseerd als domain data products:
  - advies  
  - productconfiguratie  
  - polis  
  - schade  
- Eén governance-model bewaakt consistentie, privacy, security en compliance.

### 4. Teams & Operating Model (LeSS / network-of-teams)

- Teams zijn autonoom maar verbonden via:
  - productcatalogus  
  - keten-engine  
  - platform-standaarden (API, events, security, data)
- Medewerkers bewegen tussen teams (rotatie) om kennis-silo’s te voorkomen.
- Naast LeSS wordt extra nadruk gelegd op:
  - AI-guilds  
  - data-guilds  
  - security- en compliance-guilds

### 5. SDLC & AI Factory

- SDLC is grotendeels AI-gedreven:
  - AI helpt bij discovery (identificeren van keten-knelpunten).  
  - AI doet oplossingsvoorstellen (proces- en productconfiguratievarianten).  
  - AI bouwt een substantieel deel van code en tests; mensen reviewen en sturen.
- “First time right” wordt hergeïnterpreteerd als:
  - de juiste **capabilities en keteninrichting** in één keer goed neerzetten  
  - fouten zijn acceptabel op feature-niveau, maar niet op strategisch platform- en ketenniveau
- AI ondersteunt:
  - simulaties  
  - keten-testen  
  - impactanalyses bij changes

### 6. Klant & Ecosysteem

- Inpact is een **insurance-ecosysteemhub** voor schade:
  - verzekeraars  
  - volmachtbedrijven  
  - adviseurs  
  - externe partijen (fraude-services, databronnen, weer/mobiliteit, identity, etc.)
- Nieuwe partners worden snel aangesloten via:
  - productcatalogus  
  - keten-sjablonen  
  - gestandaardiseerde IIP-API’s
- IIP is platform én AI-engine in één ecosysteem.

---

## First Time Right vs “Je Maakt Altijd Fouten”

Er is een expliciet spanningsveld tussen:

- **“Making the right things the first time right”**  
  → Focus op: architectuur, ketenontwerp, productcatalogus en platformcapabilities die in één keer robuust moeten zijn.

- **CPO-visie: “je maakt altijd (veel) fouten”**  
  → Realiteit van software-ontwikkeling en leren, met ruimte voor itereren.

**Positionering in dit model:**

- We accepteren fouten op feature-/implementatieniveau.  
- We minimaliseren fouten op:
  - ketenontwerp  
  - platform-architectuur  
  - productcatalogus-structuur  
- De AI SDLC Factory wordt ingezet om:
  - fouten vroegtijdig te detecteren  
  - regressie en impact te simuleren  
  - iteraties sneller en veiliger te maken

---

## Anti-silo principes (IIP-keten-specifiek)

1. **Eén product in LeSS:**  
   - “IIP Schadeketen” is het centrale product, geen aparte productdefinities per systeem.

2. **Eén centrale productcatalogus:**  
   - Productlogica zit in de catalogus en keten-engine, niet verspreid over teams en codebases.

3. **Teams langs ketenstromen, niet langs systemen:**  
   - Teams zijn verantwoordelijk voor end-to-end resultaten (advies t/m schade) binnen hun stream.

4. **Nieuwe functionaliteit altijd IIP-first:**  
   - Legacy wordt niet meer uitgebreid, alleen nog gemigreerd en gemapt.

5. **AI-kennis horizontaal georganiseerd:**  
   - AI-guilds en data-guilds voorkomen dat een “AI-team” zelf een silo wordt.

6. **Eén SDLC-/AI-toolstack:**  
   - Alle teams gebruiken dezelfde CI/CD-, test- en AI-ondersteuningstools om fragmentatie te voorkomen.

---

## Nuances en open punten

Dit model is een **eerste geïntegreerde versie** en bevat nog nuances die verder uitgewerkt moeten worden, o.a.:

- Precieze timing en fasering over de 3 jaar migratieperiode.
- Detailniveau per subproces (advies, polisbeheer, schade) en verschillen in volwassenheidsniveau per ketendeel.
- Concrete KPI’s per niveau (bijvoorbeeld percentages migratie, time-to-market, STP-ratio’s, AI-adoptie in SDLC).
- De praktische invulling van de AI SDLC Factory (toolingkeuze, rolverdeling, governance).
- De exacte vertaling van LeSS-principes naar de Inpact-teams (aantal teams, indeling, rol van PO/CPO).

Deze punten vragen verdere iteratie met het leadershipteam en de betrokken product-/techrollen.

---
