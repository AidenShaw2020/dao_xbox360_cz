# Dragon Age: Origins – česká lokalizace včetně DLC pro Xbox 360

Tento návod popisuje instalaci české lokalizace pro **Dragon Age: Origins** na konzolích Xbox 360 s RGH/JTAG.

Lokalizace je určena pro:

* základní hru Dragon Age: Origins,
* podporovaná rozšíření a DLC,
* herní menu,
* dialogy a dialogové volby,
* deník úkolů,
* kodex,
* popisy předmětů, schopností a kouzel,
* titulky a další herní texty.

Součástí projektu je také volitelný nástroj pro počeštění názvů DLC zobrazovaných v herních nabídkách.

Instalace nevyžaduje přepisování rozbalených souborů základní hry ani úpravu `default.xex`. Lokalizace se instaluje jako samostatný obsah společně s odpovídajícím Title Update.

## Podporovaná verze

| Položka                         | Hodnota                                            |
| ------------------------------- | -------------------------------------------------- |
| Platforma                       | Xbox 360 RGH/JTAG                                  |
| Title ID                        | `454108C0`                                         |
| Lokalizační balíček             | `A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2`         |
| Požadovaný Title Update         | `TU_12K2260_0000004000000.0000000000391`           |
| Cílový adresář DLC a lokalizace | `Hdd1:\Content\0000000000000000\454108C0\00000002` |
| Cílový adresář Title Update     | `Hdd1:\Cache`                                      |

Použitá verze hry musí být kompatibilní s přiloženým Title Update. Jiná regionální nebo mediální verze hry nemusí lokalizaci správně načíst.

Před instalací doporučujeme zazálohovat původní soubory, DLC a případný dříve používaný Title Update.

## Obsah projektu

| Soubor                                     | Účel                                      |
| ------------------------------------------ | ----------------------------------------- |
| `A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2` | Hlavní balíček české lokalizace           |
| `TU_12K2260_0000004000000.0000000000391`   | Požadovaný Title Update                   |
| `DAO_CZ_DLC_Metadata_Local_Patcher_v1.zip` | Volitelný nástroj pro počeštění názvů DLC |

## Co budete potřebovat

1. Xbox 360 s RGH nebo JTAG.

2. Funkční instalaci Dragon Age: Origins.

3. Správce souborů, například:

   * Aurora File Manager,
   * XeXMenu,
   * FTP přístup ke konzoli.

4. Hlavní lokalizační balíček:

   ```text
   A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
   ```

5. Odpovídající Title Update:

   ```text
   TU_12K2260_0000004000000.0000000000391
   ```

6. Pro volitelné počeštění názvů DLC počítač se systémem Windows a balíček:

   ```text
   DAO_CZ_DLC_Metadata_Local_Patcher_v1.zip
   ```

## Instalace české lokalizace

### 1. Záloha původních souborů

Před instalací zazálohujte:

* původní DLC,
* dříve používaný Title Update,
* případnou předchozí verzi české lokalizace.

DLC a lokalizační balíčky se nacházejí v:

```text
Hdd1:\Content\0000000000000000\454108C0\00000002
```

Title Updates uložené v systémové cache se nacházejí v:

```text
Hdd1:\Cache
```

Neodstraňujte celý obsah složky `Cache`. Odstraňte pouze starší Title Update určený pro Dragon Age: Origins.

### 2. Instalace Title Update

Odstraňte předchozí Title Update pro Dragon Age: Origins ze složky:

```text
Hdd1:\Cache
```

Poté do stejné složky zkopírujte:

```text
TU_12K2260_0000004000000.0000000000391
```

Ve složce `Hdd1:\Cache` ponechte pro Dragon Age: Origins pouze jeden aktivní Title Update.

Více různých Title Updates pro stejnou hru může způsobit:

* nenačtení češtiny,
* použití nesprávné verze hry,
* pád při spuštění,
* problémy s DLC.

### 3. Instalace lokalizačního balíčku

Soubor:

```text
A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
```

zkopírujte do:

```text
Hdd1:\Content\0000000000000000\454108C0\00000002
```

Výsledná cesta musí být:

```text
Hdd1:\Content\0000000000000000\454108C0\00000002\A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
```

Soubor nepřejmenovávejte a nevkládejte jej do další podsložky.

### 4. Obnovení databáze v Auroře

V Auroře:

1. obnovte seznam herního obsahu a DLC,
2. obnovte seznam Title Updates,
3. vyberte Dragon Age: Origins,
4. ověřte, že je nový Title Update nalezen,
5. nový Title Update aktivujte.

Pokud Aurora stále zobrazuje starý Title Update, odstraňte jej ze seznamu, znovu proveďte skenování a ověřte obsah složky `Hdd1:\Cache`.

### 5. Restart konzole

Po dokončení instalace konzoli úplně vypněte.

Nepoužívejte pouze návrat do dashboardu nebo rychlý restart aplikace. Proveďte úplné vypnutí a následné zapnutí konzole.

## Výsledná struktura na Xboxu

Po instalaci by měly být důležité soubory umístěny přibližně takto:

```text
Hdd1:\
├── Cache\
│   └── TU_12K2260_0000004000000.0000000000391
└── Content\
    └── 0000000000000000\
        └── 454108C0\
            └── 00000002\
                ├── A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
                ├── <DLC soubor 1>
                ├── <DLC soubor 2>
                └── ...
```

Soubory DLC jsou STFS kontejnery a obvykle nemají příponu.

## Volitelné počeštění názvů DLC

Hlavní lokalizační balíček zajišťuje české texty ve hře. Názvy některých DLC však mohou být v nabídkách Xboxu nebo hry stále zobrazeny anglicky.

Pro jejich úpravu lze použít:

```text
DAO_CZ_DLC_Metadata_Local_Patcher_v1.zip
```

Tento krok je volitelný a není nutný pro samotné fungování české lokalizace.

### Příprava patcheru

Rozbalte ZIP archiv do samostatného pracovního adresáře.

V jednom adresáři musí být následující soubory:

```text
patch_dao_dlc_packages_local.py
run_patch_dao_dlc_packages_local.bat
patched_dlc_metadata.zip
```

Ve stejném adresáři vytvořte podsložku:

```text
DLC
```

Výsledná struktura bude:

```text
DAO_CZ_DLC_Metadata_Local_Patcher_v1\
├── patch_dao_dlc_packages_local.py
├── run_patch_dao_dlc_packages_local.bat
├── patched_dlc_metadata.zip
└── DLC\
```

### Kopírování DLC z Xboxu

Do podsložky `DLC` zkopírujte DLC soubory z:

```text
Hdd1:\Content\0000000000000000\454108C0\00000002
```

Kopírujte samotné soubory DLC, nikoli celý adresář `00000002`.

Před úpravou doporučujeme vytvořit další samostatnou zálohu původních DLC.

### Spuštění patcheru

Spusťte:

```text
run_patch_dao_dlc_packages_local.bat
```

Skript zpracuje rozpoznané DLC a vytvoří upravené soubory v adresáři:

```text
patched_dlc_packages
```

Pokud některý DLC soubor není podporován nebo rozpoznán, neměl by být použit jeho neúplný nebo chybový výstup.

### Nahrání upravených DLC do Xboxu

1. Zazálohujte původní DLC soubory na Xboxu.

2. Otevřete adresář:

   ```text
   patched_dlc_packages
   ```

3. Nahraďte pouze ty DLC soubory, které skript skutečně vytvořil.

4. Zachovejte stejné názvy souborů.

5. Soubory nahrajte zpět do:

   ```text
   Hdd1:\Content\0000000000000000\454108C0\00000002
   ```

6. Ve složce `00000002` nenechávejte současně původní i upravenou variantu stejného DLC.

7. Konzoli úplně vypněte a znovu zapněte.

## Title Update

Tato lokalizace vyžaduje přiložený Title Update:

```text
TU_12K2260_0000004000000.0000000000391
```

Bez správně aktivovaného Title Update nemusí být český lokalizační balíček načten.

Pro Dragon Age: Origins mějte aktivní pouze jeden Title Update. Nepoužívejte současně jiný TU stažený Aurorou nebo získaný z jiné verze hry.

Pokud potřebujete Title Update změnit:

1. deaktivujte stávající TU v Auroře,
2. odstraňte jeho soubor z `Hdd1:\Cache`,
3. nahrajte správnou verzi,
4. obnovte seznam Title Updates,
5. správný TU aktivujte,
6. úplně restartujte konzoli.

## Ověření ve hře

Po spuštění zkontrolujte:

1. české hlavní menu,
2. české titulky a dialogové volby,
3. český deník úkolů,
4. český kodex,
5. české názvy a popisy předmětů, schopností a kouzel,
6. správné načtení uložené pozice,
7. viditelnost nainstalovaných DLC,
8. spuštění DLC bez pádu hry.

Po volitelné úpravě metadat ověřte také nabídky:

* **Nová hra**
* **Obsah ke stažení**

Názvy podporovaných DLC by se zde měly zobrazovat česky.

První test doporučujeme provést také v nové hře. Tím lze odlišit problém lokalizace od problému konkrétní starší uložené pozice.

## Řešení problémů

### Hra zůstává v angličtině

Zkontrolujte:

* zda je lokalizační soubor ve správném adresáři,
* zda nebyl při kopírování přejmenován,
* zda se nenachází v další podsložce,
* zda je aktivní správný Title Update,
* zda konzole po instalaci prošla úplným restartem.

Správná cesta lokalizačního souboru je:

```text
Hdd1:\Content\0000000000000000\454108C0\00000002\A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
```

### Aurora Title Update nevidí

Zkontrolujte, zda je soubor:

```text
TU_12K2260_0000004000000.0000000000391
```

uložen přímo v:

```text
Hdd1:\Cache
```

Poté obnovte seznam Title Updates v Auroře.

Pokud jej Aurora stále nevidí, ověřte:

* úplnost názvu souboru,
* zda při přenosu nevznikla přípona,
* zda se soubor nenachází v podsložce,
* zda byl FTP přenos dokončen bez chyby.

### Title Update je vidět, ale čeština nefunguje

Ověřte, že je Title Update skutečně aktivní.

Odstraňte nebo deaktivujte ostatní Title Updates pro Dragon Age: Origins a ponechte pouze:

```text
TU_12K2260_0000004000000.0000000000391
```

Poté konzoli úplně restartujte.

### Hra po instalaci spadne

Nejčastější příčiny jsou:

* nekompatibilní verze hry,
* nesprávný Title Update,
* více současně aktivních Title Updates,
* poškozený nebo neúplně přenesený lokalizační soubor,
* poškozené DLC,
* současná přítomnost více variant stejného DLC.

Vraťte zálohu původních souborů a instalaci proveďte znovu.

Nepoužívejte `force` režimy FTP klienta, které mohou přeskočit nebo předčasně ukončit přenos velkých souborů.

### DLC není ve hře vidět

Zkontrolujte:

* správný Title ID `454108C0`,
* správnou složku `00000002`,
* že soubor DLC nemá přidanou příponu,
* že se soubor nenachází v podsložce,
* že ve složce není více variant stejného DLC.

Správný adresář je:

```text
Hdd1:\Content\0000000000000000\454108C0\00000002
```

Po změně DLC obnovte obsah v Auroře a konzoli restartujte.

### Názvy DLC zůstávají anglicky

Ověřte, že jste na Xbox nahráli soubory vytvořené v:

```text
patched_dlc_packages
```

a nikoli původní vstupní soubory z adresáře:

```text
DLC
```

Současně zkontrolujte, že jste zachovali původní názvy souborů a původní cílovou cestu.

### Patcher se nespustí

Pokud se okno ihned zavře nebo se zobrazí chyba týkající se Pythonu, nainstalujte Python 3 a během instalace aktivujte:

```text
Add Python to PATH
```

Poté zavřete a znovu otevřete příkazový řádek a patcher spusťte znovu.

### Patcher nevytvořil některé DLC

Zkontrolujte, zda jste do adresáře `DLC` vložili skutečné STFS soubory DLC, nikoli:

* ZIP archiv,
* složku s rozbaleným obsahem,
* zástupce,
* soubory z jiného Title ID,
* již poškozenou nebo neúplnou kopii.

Neupravujte ručně soubory, které patcher nerozpoznal.

## Aktualizace lokalizace

Při přechodu na novější vydání:

1. zazálohujte současnou funkční instalaci,
2. odstraňte starý lokalizační balíček,
3. odstraňte nebo deaktivujte starý Title Update,
4. nahrajte nové soubory,
5. obnovte seznam DLC a Title Updates,
6. aktivujte nový Title Update,
7. konzoli úplně restartujte.

Nemíchejte soubory z různých vydání lokalizace.

## Obnova původní verze

Pro návrat k původní anglické verzi:

1. odstraňte lokalizační soubor:

   ```text
   A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
   ```

2. vraťte zálohy původních DLC, pokud jste upravovali jejich metadata,

3. deaktivujte nebo odstraňte přiložený Title Update, pokud jej již nechcete používat,

4. obnovte seznam obsahu v Auroře,

5. konzoli úplně restartujte.

Bez zálohy původních DLC nemusí být možné bezpečně obnovit jejich původní anglické názvy.

## Doporučená struktura repozitáře

Soubory projektu mohou být v repozitáři uspořádány následovně:

```text
dao_xbox360_cz/
├── README.md
├── A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD2
├── TU_12K2260_0000004000000.0000000000391
└── DAO_CZ_DLC_Metadata_Local_Patcher_v1.zip
```

Archiv patcheru po rozbalení obsahuje:

```text
DAO_CZ_DLC_Metadata_Local_Patcher_v1/
├── patch_dao_dlc_packages_local.py
├── run_patch_dao_dlc_packages_local.bat
├── patched_dlc_metadata.zip
└── DLC/
```

## Doporučení pro FTP přenos

Po nahrání větších souborů ověřte jejich velikost na Xboxu a porovnejte ji s velikostí původního souboru na počítači.

Při přenosu:

* nepřerušujte spojení,
* nepoužívejte automatické přejmenování,
* nepřidávejte přípony,
* nepřenášejte soubory v textovém režimu,
* po dokončení nechte FTP klienta dokončit frontu.

Neúplný přenos může způsobit, že Aurora soubor zobrazí, ale hra jej nedokáže načíst.

## Právní poznámka

Projekt je určen pro uživatele, kteří vlastní originální kopii Dragon Age: Origins a příslušná DLC.

Českou lokalizaci a upravená metadata používejte pouze s vlastní legálně získanou kopií hry a v souladu s licencí hry a právními předpisy ve vaší zemi.

Projekt nenahrazuje původní hru ani příslušná DLC.
