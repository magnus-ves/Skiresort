# Skisjefen ⛷️

Et nettleserspill der du bygger og driver ditt eget skisenter – et tycoon- og byggespill med heiser, nedfarter, gjester, økonomi, vær og sesonger. Hele spillet ligger i én fil, `index.html` (HTML, CSS og JavaScript med Canvas), og kan spilles direkte i nettleseren på PC og mobil.

## Slik spiller du

Åpne `index.html` i nettleseren, eller spill via GitHub Pages når det er slått på (se under).

* **Tilfeldig fjell** – et generert fjell med skog, steiner, bekker og et tjern.
* **Velg et ekte sted** – søk etter et stedsnavn eller klikk i kartet, og velg et område på 1, 2 eller 3 km. Høydedata og kartobjekter hentes fra nettet. Med «Ekte skisenter» hentes også eksisterende nedfarter og heiser fra OpenStreetMap.

Bygg heiser (dra fra bunn til topp), tegn nedfarter (vanskelighetsgraden regnes ut fra brattheten), sett opp fasiliteter, ansett folk, sett prisen på heiskortet og åpne sesongen. Sesongen går fra desember til april. Jul, vinterferie og påske gir ekstra mange gjester.

**Kontroller:** dra for å flytte kartet, rull eller klyp for å zoome. Mellomrom = pause, 1/2/3 = fart, Esc = avbryt verktøy.

## Spillmoduser

Fri modus, eller scenarioer med mål: «Familiebakken», «500 gjester per dag», «Millionen», «Femstjerners anlegg» og «Mild vinter». Nye heistyper og bygg låses opp etter hvert som skisenteret får flere besøkende.

## Datakilder

* Høyder: [AWS Terrain Tiles](https://registry.opendata.aws/terrain-tiles/) (Terrarium-format), med [Open-Meteo Elevation API](https://open-meteo.com/en/docs/elevation-api) som reserve.
* Kartobjekter (skog, vann, bekker, veier, bygninger, fjelltopper, nedfarter og heiser): [Overpass API](https://overpass-api.de/).
* Stedssøk: [Nominatim](https://nominatim.org/).
* Kartvelger: [Leaflet](https://leafletjs.com/) med OpenStreetMap-fliser. Leaflet er det eneste eksterne biblioteket, og det lastes fra unpkg først når kartvelgeren åpnes.

Nedlastede kart og lagrede spill ligger i nettleserens `localStorage`. Uten nett kan du alltid spille på et tilfeldig fjell.

Kartdata © [OpenStreetMap-bidragsytere](https://www.openstreetmap.org/copyright) (ODbL).

## Publisere med GitHub Pages

Gå til **Settings → Pages** og velg **Source: GitHub Actions**. Workflowen `.github/workflows/pages.yml` sjekker JavaScript-koden og publiserer spillet ved hver push til `main`.
