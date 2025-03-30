# Základní koncepce

Hra je zamýšlena jako **2D survival RPG** s **pixelovou grafikou** a **pohledem shora**, převážně inspirované hrami jako *Stardew Valley, Sun Haven* nebo *Fields of Mistria*.  
Projekt se momentálně bude zaměřovat na (zatím) velice **jednoduchý příběh**, objevování světa a interakci s ním a různými postavami.  
Hlavní prvky hratelnosti budou zahrnovat **průzkum, dialogy a plnění questů**.  
Mým hlavním nástrojem pro vývoj bude **Godot Engine**, který nabízí podporu pro 2D hry a snadnou implementaci pixelové grafiky.

---

## Proveditelnost a zdroje

Zdroje budou obsahovat převážně **tutoriály na YouTube**, či **oficiální nebo neoficiální články a dokumenty**.  
Momentálně všechny assety, ať už se jedná o **postavy, pozadí, uživatelské rozhraní, zvukové efekty, hudbu a veškeré další assety**, si chci vytvořit sám.  
Nějaká inspirace z ostatních her tu bude, ale jen proto, abych **zbytečně neházel pixely tam, kde nemají být**.  
V žádném případě to nebude **1:1 kopie**, chci, aby to byla **“moje” hra** a aby měla **jedinečný vizuální styl – můj styl**.

---

## Hrubý popis hry a záměr

V tuto chvíli plánuji, že hra nabídne **prozkoumávání rozmanitého fantasy světa** s (zatím) jednoduchým příběhem a dobrodružstvím.  
Hráč se bude moct **bavit s NPC postavami, přijímat od nich questy a objevovat i nějaká ta tajemství**.  
Zde jsou některé z hlavních prvků hratelnosti:

- **Vyrábění a stavění**: Hráč bude moct vyrábět a stavět užitečné předměty.
- **Pěstování a farmaření**: Jednoduché možnosti farmaření poskytnou jídlo a suroviny potřebné k přežití.
- **Bojování s příšerami**: Souboje s různými tvory, kteří obývají svět, nabídnou akční prvky a další výzvy.
- **Plnění questů a úkolů**: Herní svět bude plný příběhových i vedlejších questů, které hráče odmění a poskytnou další důvody k průzkumu.
- **Bavení se s NPC postavami**: Interakce s obyvateli světa budou klíčové nejen pro příběh, ale také pro získání cenných informací.

---

## Technologie a architektura

- **Godot Engine**: Hlavní nástroj pro vývoj hry, využívající jeho 2D podporu a skriptovací jazyk **GDScript**, který umožňuje snadnou implementaci herních mechanik.
- **Pixelová grafika**: Grafické prvky budou vytvořeny pomocí **pixelového stylu**, protože se mi vždy líbil a chci ho použít. Myslím si, že je jednodušší na implementaci a dokáže přinést **“nostalgický nádech”**.
- **Pohled shora**: Použití **pohledu shora** poskytne hráči dobrý přehled o herním světě, podobně jako ve hrách, které jsem zmínil na začátku.
- **Dialogový systém**: Systém, pomocí kterého se hráč bude moct s NPC bavit. Například vybere jednu ze tří možností dialogu a NPC mu na ni odpoví.
- **Questový systém**: Hráč bude moct plnit úkoly přímo od NPC nebo pomocí dalších způsobů.

# GameDesign

## Životy a zdraví  
- Hráč začíná s **maximálním počtem životů** (např. 5 srdíček).  
- Pokud je **poškozen nepřáteli nebo pastmi**, ztratí **srdíčko**.  
- Zdraví lze obnovit pomocí **jídla, lektvarů nebo odpočinku**.  
- Pokud hráč ztratí všechna srdíčka, **zemře** a vrátí se na poslední uložený bod.  

---

## Stamina  
- Stamina se spotřebovává při **běhu, boji a těžké práci** (např. těžení, sekání stromů).  
- Regeneruje se **pomalu automaticky** nebo rychleji pomocí **jídla, odpočinku**.  
- Pokud stamina dojde, hráč **nemůže běhat ani útočit**, dokud se neobnoví.  

---

## Questy  
- Hráč může **přijímat úkoly** od NPC nebo ze speciálních tabulí.  
- Úkoly mohou být různých typů:  
  - **Doručovací** – Najdi a dones předmět.  
  - **Sbírací** – Sesbírej určitý počet materiálů.  
  - **Lovící** – Poraz určité nepřátele.  
  - **Příběhové** – Pokračují v hlavním ději hry.  
- Po splnění úkolu hráč získá **odměny** (peníze, materiály, zkušenosti).  

---

## Materiály a sběr surovin  
- Hráč může získávat materiály **těžením, kácením stromů, sbíráním rostlin nebo poražením nepřátel**.  
- Existují různé typy materiálů:  
  - **Dřevo** (stromy)  
  - **Kámen** (skály)  
  - **Rudy a kovy** (dolování)  
- Některé vzácnější materiály **potřebují lepší nástroje** k získání.  

---

## Vyrábění (Crafting)  
- Hráč může z nasbíraných materiálů vyrábět:  
  - **Nástroje** (sekery, krumpáče, meče)  
  - **Jídlo** (pro obnovu života a staminy)  
  - **Zbraně** (pro boj s nepřáteli)  
  - **Stavební materiály** (pro úpravy světa)  
- Některé věci vyžadují **speciální pracovní stoly**.  

---

## Boj  
- Hráč může útočit na nepřátele pomocí **zbraní nebo magie**.  
- Každý útok **spotřebovává staminu**, takže je potřeba bojovat strategicky.  
- Nepřátelé mají různé chování, některé lze **omráčit nebo zastrašit**.  
- Po poražení nepřítele hráč získává **odměny (materiály, zkušenosti, zlato)**.  

# Grafika

## Styl a vizuální směr  
- Hra využívá **pixelovou grafiku** inspirovanou klasickými 2D RPG hrami.  
- Grafika je navržena tak, aby byla **jednoduchá na pochopení**, ale zároveň vizuálně atraktivní.  

---

## Technické zpracování  
- **2D vizuál** – Veškerá grafika je kreslená ve dvou rozměrech, s důrazem na přehlednost a estetiku.  
- **Software: Aseprite** – Všechny spritey, animace a tilesety jsou tvořeny v tomto pixel-art programu.  
- **Vytvořeno na PC pomocí myši** – Každý prvek hry je ručně kreslený bez použití grafického tabletu.  

---

## Prvky grafiky  
- **Herní prostředí** – Ručně kreslené lokace jako lesy, vesnice a dungeony.  
- **Postavy** – Unikátní design NPC i nepřátel, každá postava má svou animaci pro chůzi a idle stav.  
- **UI a ikony** – Minimalistické uživatelské rozhraní s přehlednými pixel-art ikonami.  

# Zvuky  

## Zdroje zvuků  
- **Stažené z internetu** – Většina zvukových efektů pochází z volně dostupných knihoven.  
- **Licence** – Použité zvuky splňují podmínky pro použití v nezávislých hrách.  
- **Hudba** – Buď bude stažená, nebo využiju generátor hudby.  

---

## Typy zvuků ve hře  
- **Kroky** – Zvuky chůze na různých površích (tráva, dřevo, kámen).  
- **Boj** – Údery, zásahy a kouzla.  
- **UI efekty** – Otevření inventáře, výběr možnosti v menu.  
- **Prostředí** – Vítr, déšť, zvuky lesa pro lepší atmosféru.  
