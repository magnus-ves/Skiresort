# Skisjefen ⛷️

Et nettleserspill der du bygger og driver ditt eget skisenter – et tycoon- og byggespill med heiser, nedfarter, gjester, økonomi, vær og sesonger. Hele spillet ligger i én fil, `index.html` (HTML, CSS og JavaScript med Canvas), og kan spilles direkte i nettleseren på PC og mobil.

## Slik spiller du

Åpne `index.html` i nettleseren, eller spill via GitHub Pages når det er slått på (se under).

* **Tilfeldig fjell** – et generert fjell med skog, steiner, bekker og et tjern.
* **Velg et ekte sted** – søk etter et stedsnavn eller klikk i kartet, og velg et område på 1, 2 eller 3 km. Høydedata og kartobjekter hentes fra nettet. Med «Ekte skisenter» hentes også eksisterende nedfarter og heiser fra OpenStreetMap.

Bygg heiser (dra fra bunn til topp) – skibånd (magic carpet), koppheis, T-krok, stolheis med fast klype, stolheis med stasjon og gondol – tegn nedfarter (vanskelighetsgraden regnes ut fra brattheten), sett opp fasiliteter, ansett folk, sett prisen på heiskortet og åpne sesongen. Sesongen går fra desember til april. Jul, vinterferie og påske gir ekstra mange gjester.

**3D og 2D:** spillet vises i 3D som standard, med terreng, trær, heiser, bygninger, gjester, skygger, dag og natt. Knappen **2D/3D** til høyre bytter til et flatt kart ovenfra, som også virker uten nett.

**Kontroller:** dra for å flytte, rull eller klyp for å zoome. I 3D roterer du med høyre museknapp (eller Alt + dra), med to fingre som vris, med Q/E eller med ⟲ ⟳-knappene. ⛰️ endrer vinkelen. Mellomrom = pause, 1/2/3 = fart, Esc = avbryt verktøy.

## Spillmoduser

Fri modus, eller scenarioer med mål: «Familiebakken», «500 gjester per dag», «Millionen», «Femstjerners anlegg» og «Mild vinter». Nye heistyper og bygg låses opp etter hvert som skisenteret får flere besøkende.

## Datakilder

* Høyder: [AWS Terrain Tiles](https://registry.opendata.aws/terrain-tiles/) (Terrarium-format), med [Open-Meteo Elevation API](https://open-meteo.com/en/docs/elevation-api) som reserve.
* Kartobjekter (skog, vann, bekker, veier, bygninger, fjelltopper, nedfarter og heiser): [Overpass API](https://overpass-api.de/).
* Stedssøk: [Nominatim](https://nominatim.org/).
* Kartvelger: [Leaflet](https://leafletjs.com/) med OpenStreetMap-fliser.
* 3D: [Three.js](https://threejs.org/) r149.

De eksterne bibliotekene er Leaflet og Three.js. Begge lastes fra unpkg først når de trengs.

Nedlastede kart og lagrede spill ligger i nettleserens `localStorage`. Uten nett kan du alltid spille på et tilfeldig fjell.

Kartdata © [OpenStreetMap-bidragsytere](https://www.openstreetmap.org/copyright) (ODbL).

## Publisere med GitHub Pages

Gå til **Settings → Pages** og velg **Source: GitHub Actions**. Workflowen `.github/workflows/pages.yml` sjekker JavaScript-koden og publiserer spillet ved hver push til `main`.
