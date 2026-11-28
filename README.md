# Rally Sprint

3D rallye a F1 hra v prohlížeči. **Hraj na https://pavel-pe899.github.io/rally-sprint/**

Na iPhonu: otevři odkaz v Safari, otoč telefon na šířku a přes Sdílet → Přidat na plochu si hru dej jako ikonu.
Hra pro dva: v menu „Proti sobě“ → jeden ťukne na „Založit hru“ a řekne kód, druhý ho napíše a ťukne na „Připojit“
(telefony se spojí napřímo přes WebRTC, k nalezení se používá bezplatný server PeerJS).

Celá hra je v jednom souboru `index.html` (three.js, modely aut i textury uvnitř). Zdrojový kód je v soukromém
repozitáři autora, sem se nahrává jen hotová stránka. Hra je nekomerční (některé modely mají licenci CC BY-NC).

## Autoři použitých děl
- **T-rex (Džungle):** model „Trex“ od [Quaternius](https://quaternius.com) ([Poly Pizza](https://poly.pizza/m/UYtneO5FpF)),
  licence [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) (volné dílo), s kostrou a animacemi.
  Stažený z GitHubu: [netnetdev/net-forge](https://github.com/netnetdev/net-forge)
  (`packages/asset-library-files/library/lowpoly/trex.glb`, tamtéž soubor NOTICE s původem a licencí).
  Ve hře převedený do JSON (`tools/trex-to-json.mjs`), větší a se světlejšími barvami. Zvuky T-rexe jsou vlastní syntéza.
- **3D textury povrchů (CC0 1.0, volná díla):** fotografické PBR textury s normálovými mapami z [Poly Haven](https://polyhaven.com)
  – „Rocky Trail“ (štěrková cesta), „Rock Face 03“ (Dario Barresi a Rico Cilliers, skály), „Aerial Rocks 02“, „Dirt Aerial 02“
  a „Aerial Beach 01“ (Rob Tuytel), „Sparse Grass“ (Amal Kumar), „Rock Boulder Cracked“ – a z [ambientCG](https://ambientcg.com)
  („Ground 092 C“ duny, „Ice 002“ led). Staženo z GitHubu: [playcanvas/engine](https://github.com/playcanvas/engine)
  (`examples/assets/textures`, včetně záznamu o původu) a [mrdoob/three.js](https://github.com/mrdoob/three.js)
  (`examples/textures/ambientcg`). Zmenšené a převedené skriptem `tools/prep-tex.py`; normálové mapy štěrku, balvanu
  a betonu dopočtené z jasu fotky.
- **Monster truck:** model [„Free Monster Truck Model“](https://sketchfab.com/3d-models/free-monster-truck-model-96d16754451d4ca3a0b4c5252452f0b5)
  od steelcyclonestudios (Sketchfab), licence [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
  Stažený z GitHubu: [freaxnx01/game-rhyflitzer](https://github.com/freaxnx01/game-rhyflitzer)
  (`assets/src/free_monster_truck_model.glb`, nezměněný originál je v `web/assets/src/monster.glb`).
  Změny (`tools/prep-monster.mjs`): zvětšený na skutečnou velikost, kola rozdělená do čtyř uzlů, odstraněný znak
  na bocích korby, materiály s kovem a leskem, zjednodušená geometrie (177 tisíc → 38 tisíc trojúhelníků).
- **Rodinné domky na ostrově:** `house_a`–`house_d` a garáž z [Starter Kit City Builder](https://github.com/KenneyNL/Starter-Kit-City-Builder)
  od [Kenney](https://kenney.nl), licence MIT (Copyright (c) 2025 Kenney), převod `tools/props-to-json.mjs` → `web/assets/props.json`.
- **Valník na ostrově:** kabina rozvážkové dodávky z Car Kit (Kenney, CC0, viz auta v provozu), korba dřevěná s bočnicemi (vlastní).
- **Budovy a příroda na ostrově:** domy (building a–h), stromy, palmy, keře, květiny a kameny od [Kenney](https://kenney.nl),
  licence [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). Staženo z GitHubu: [netnetdev/net-forge](https://github.com/netnetdev/net-forge)
  (`packages/asset-library-files/library/lowpoly`, licence balíčků v `NOTICE`). Převod: `tools/props-to-json.mjs` → `web/assets/props.json`.
- **Auta v provozu na ostrově:** modely sedan, sportovní sedan, SUV, luxusní SUV, taxi, dodávka a rozvozová dodávka
  z [Car Kit](https://kenney.nl/assets/car-kit) od [Kenney](https://kenney.nl), licence
  [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) (volné dílo). Staženo z GitHubu:
  [netnetdev/net-forge](https://github.com/netnetdev/net-forge) (`packages/asset-library-files/library/lowpoly`,
  seznam balíčků a licencí v `NOTICE`). `tools/traffic-to-json.mjs` je převádí do čitelného JSON (`web/assets/traffic.json`).
- **Bugatti Chiron:** model „Bugatti Chiron 2017“ od Boba Kimaniho (Kimz Auto), sdílený na
  [Blend Swap](https://blendswap.com/blend/32484) (apexmesh) pod licencí CC BY-NC (Creative Commons Uveďte původ – Neužívejte komerčně), jak ji uvádí Blend Swap:
  **jen nekomerční použití** (stejně jako u G 63). Webovou verzi (rovné auto ve skutečné velikosti, kola a křídlo zvlášť,
  méně materiálů) připravil Mohammed Benkhattab v repozitáři [1337Impact/bugatti-chiron-showroom](https://github.com/1337Impact/bugatti-chiron-showroom)
  na GitHubu (`public/models/chiron.glb`). Pro hru zjednodušený (`tools/prep-chiron.mjs`) a bez znaků a nápisů značky.
  Bugatti a Chiron jsou ochranné známky Bugatti; hra s nimi není nijak spojená.
- **Model auta:** [„[FREE] BMW M3 E30“](https://sketchfab.com/3d-models/free-bmw-m3-e30-ac3c7013434e403e8faff87948caf422)
  od Martina Trafase (Sketchfab), licence [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
  Stažený z repozitáře [Distinguish101/raj-garage](https://github.com/Distinguish101/raj-garage).
  Změny (`tools/prep-car.mjs`): odstraněné odznaky BMW, srovnaná přední kola, zjednodušená geometrie,
  textury zmenšené na 512 px, komprese meshopt; ve hře vlastní lak, startovní čísla a rallyové doplňky.
  BMW a M3 jsou ochranné známky BMW AG; hra s nimi není nijak spojená.
- **Další auta** (staženo z veřejných ukázek na GitLabu, kde byla s licencí uvnitř souboru):
  - [„FREE 1975 Porsche 911 (930) Turbo“](https://sketchfab.com/3d-models/free-1975-porsche-911-930-turbo-8568d9d14a994b9cae59499f0dbed21e)
    od Lionsharp Studios, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (z gitlab.com/Hussain.H/car-showcase)
  - [„McLaren Senna Free“](https://sketchfab.com/3d-models/mclaren-senna-free-ea3e43a6eb004853a87fe9c58422eb96)
    od Black Snow, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (z gitlab.com/Sunil56224972/Wretched-Lab-Nfs-Unbound-Virtual-Lab)
  - [„Mercedes-Benz G63 AMG (W464)“](https://sketchfab.com/3d-models/mercedes-benz-g63-amg-w464-3b25ec59233a4a82a6732b0a1419e553)
    od ceron_alex, [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): **jen nekomerční použití**, proto je celá hra nekomerční
    (z gitlab.com/kukmara-tech/car-configurator)
  - [„Formula 1 Car (Version 1)“](https://sketchfab.com/3d-models/formula-1-car-version-1-84423c99221240c497f38a549ea50a2a)
    od Snoozy, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (z gitlab.com/dev.keshwani345/termf1);
    obarveno do barev zvoleného týmu, bez log
  - [„2020 Audi RS5 Coupé“](https://sketchfab.com/3d-models/2020-audi-rs5-coupe-db82f980fc0d408fbbde8deff36a82bd)
    od Ddiaz Design, [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/): upravený model
    `web/assets/cars/audi.json` se šíří pod stejnou licencí (z gitlab.com/kukmara-tech/car-configurator)
  - [„Skoda Fabia R5 Rally Car“](https://sketchfab.com/3d-models/skoda-fabia-r5-rally-car-fe062f0fd05e43a6a32a88a1aa39ef14)
    od SenturyUK, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (z github.com/cherchimarc-pixel/speciale-deco,
    kde je model s autorem a licencí uvnitř souboru); `tools/prep-fabia.mjs` rozdělil kola na samostatné díly,
    auto vycentroval a zjednodušil geometrii; vlastní lak. Škoda a Fabia jsou ochranné známky Škoda Auto a.s.
  - změny: odstraněný interiér, motor, podvozek, značky a loga (kde byla samostatným dílem), zjednodušená geometrie,
    menší textury, vlastní lak a rallyové doplňky. Porsche, McLaren, Mercedes-Benz, Audi, Formule 1 a jména týmů
    (Ferrari, Mercedes, Red Bull, Aston Martin, Alpine, McLaren, Williams, Racing Bulls, Haas, Sauber) a názvy sponzorů na vozech jsou ochranné známky svých vlastníků;
    hra s nimi není nijak spojená.
- **Postava jezdce:** X Bot z [Adobe Mixamo](https://www.mixamo.com), převzatý z ukázek [three.js](https://github.com/mrdoob/three.js/tree/dev/examples/models/gltf) (Mixamo dovoluje postavy použít ve hrách a projektech bez poplatků); zjednodušená síť, vlastní barvy a helma.
- **Tvary okruhů Miami, Monza, Silverstone, Red Bull Ring a Spa:** [bacinger/f1-circuits](https://github.com/bacinger/f1-circuits) od Tomislava Bacingera, licence MIT.
- **Fotografické textury:** skeny Asphalt033, Ground111, Grass005 a Concrete034 z [ambientCG](https://ambientcg.com) (CC0, volné dílo),
  převzaté z repozitáře [amazingsammed/mini_textures](https://github.com/amazingsammed/mini_textures)
  a zmenšené na 512 px (`web/assets/tex/`).
- **three.js** (MIT) včetně doplňků z `examples/jsm` (EffectComposer, UnrealBloomPass).
- **PeerJS** (MIT) – přímé spojení telefonů pro hru s kamarádem.
