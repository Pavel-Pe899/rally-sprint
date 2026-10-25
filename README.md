# Rally Sprint

3D rallye a F1 hra v prohlížeči. **Hraj na https://pavel-pe899.github.io/rally-sprint/**

Na iPhonu: otevři odkaz v Safari, otoč telefon na šířku a přes Sdílet → Přidat na plochu si hru dej jako ikonu.
Hra pro dva: v menu „Proti sobě“ → jeden ťukne na „Založit hru“ a řekne kód, druhý ho napíše a ťukne na „Připojit“
(telefony se spojí napřímo přes WebRTC, k nalezení se používá bezplatný server PeerJS).

Celá hra je v jednom souboru `index.html` (three.js, modely aut i textury uvnitř). Zdrojový kód je v soukromém
repozitáři autora, sem se nahrává jen hotová stránka. Hra je nekomerční (některé modely mají licenci CC BY-NC).

## Autoři použitých děl
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
  - změny: odstraněný interiér, motor, podvozek, značky a loga (kde byla samostatným dílem), zjednodušená geometrie,
    menší textury, vlastní lak a rallyové doplňky. Porsche, McLaren, Mercedes-Benz, Audi, Formule 1 a jména týmů
    (Ferrari, Mercedes, Red Bull, Aston Martin, Alpine, McLaren) jsou ochranné známky svých vlastníků;
    hra s nimi není nijak spojená.
- **Postava jezdce:** X Bot z [Adobe Mixamo](https://www.mixamo.com), převzatý z ukázek [three.js](https://github.com/mrdoob/three.js/tree/dev/examples/models/gltf) (Mixamo dovoluje postavy použít ve hrách a projektech bez poplatků); zjednodušená síť, vlastní barvy a helma.
- **Tvary okruhů Miami, Monza a Silverstone:** [bacinger/f1-circuits](https://github.com/bacinger/f1-circuits) od Tomislava Bacingera, licence MIT.
- **Fotografické textury:** skeny Asphalt033, Ground111, Grass005 a Concrete034 z [ambientCG](https://ambientcg.com) (CC0, volné dílo),
  převzaté z repozitáře [amazingsammed/mini_textures](https://github.com/amazingsammed/mini_textures)
  a zmenšené na 512 px (`web/assets/tex/`).
- **three.js** (MIT) včetně doplňků z `examples/jsm` (EffectComposer, UnrealBloomPass).
- **PeerJS** (MIT) – přímé spojení telefonů pro hru s kamarádem.
