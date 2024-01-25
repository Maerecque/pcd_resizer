# Point Cloud Resizer™
Point Cloud Resizer™ is een Python-script waarmee je puntenwolken in het LAS- of LAZ-formaat kunt openen, aanpassen en opslaan. Je kunt de puntenwolk downsamplen (verkleinen) door een voxelgrootte op te geven en vervolgens het resultaat bekijken of opslaan in een nieuw LAS-bestand.

 Dit script maakt gebruik van de volgende Python bibliotheken:

 - `tkinter` voor de GUI (graphical user interface).
- `laspy` voor het lezen en schrijven van LAS/LAZ-bestanden.
- `open3d` voor het werken met puntenwolken en visualisatie.
- `numpy` voor het bewerken van numerieke gegevens.
- `os` voor het werken met bestandspaden en bestandsbeheer.
- `subprocess` voor het starten van een apart proces voor visualisatie.
- `threading` voor het uitvoeren van bewerkingen in aparte threads om de GUI-reactiviteit te behouden.

## Gebruik
1. Open de folder waar het bestand `pointCloudResizer.py` staat. In de Windows verkenner selecteer locatie balk, op dezelfde manier als in stap 4 van installatie. In plaats dat je de locatie kopieert druk je op de Backspace-knop (←) op het toetsenbord wanneer de locatie blauw is geselecteerd en typ je in `cmd` en druk je op de Enter-toets. Nu zal Command-Prompt voor CAD-gebruikers starten op de correcte locatie. Om de applicatie te starten typ je in `Python pointCloudResizer.py`. Er zal nu een venster openen met een aantal knoppen.
2. Klik op de knop "Open file" om een LAS- of LAZ-bestand te selecteren.
3. Selecteer een voxelgrootte (de afstand tussen punten) in het "Voxel size" veld.
4. Klik op de knop "Apply subsampling" om de puntenwolk te downsamplen op basis van de opgegeven voxelgrootte.
5. De puntenwolkgrootte na het downsamplen wordt weergegeven in het "Point cloud size after subsampling" veld, en de subsamplingfactor wordt weergegeven in het "Subsampling factor" veld.
6. Je kunt de downgesamplede puntenwolk voorbeeld bekijken door op de knop "Preview" te klikken. Dit opent een 3D-visualisatievenster met de puntenwolk.
7. Als je tevreden bent met het resultaat, kun je de puntenwolk opslaan in een nieuw LAS-bestand door op de knop "Save" te klikken. Hiermee wordt een dialoogvenster geopend waarin je de bestandsnaam en locatie kunt kiezen.
8. Het nieuwe LAS-bestand wordt opgeslagen en een melding verschijnt met de opslaglocatie.

## Opmerkingen
- Dit script is ontworpen voor het werken met LAS- en LAZ-bestanden, veelgebruikte formaten voor puntenwolken in de geomatica en 3D-scanningindustrie.
- Zorg ervoor dat je het `logo.ico`-bestand hebt in dezelfde map als het script voor het weergeven van het pictogram in het venster van de toepassing.
- Als het LAS/LAZ-bestand een onbekend formaat heeft of niet kan worden verwerkt, wordt een foutmelding weergegeven.
- De puntenwolk wordt downgesampled met behulp van een regulier grid op basis van de opgegeven voxelgrootte. Het script normaliseert de grootte van de puntenwolk op basis van de oorspronkelijke dichtheid van punten.
