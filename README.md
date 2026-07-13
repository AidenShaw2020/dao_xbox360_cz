# Čeština pro Dragon Age: Origins + DLC

## Xbox 360 RGH/JTAG

## Instalace češtiny

1. Odstraňte předchozí Title Update pro **Dragon Age: Origins** ze složky:

   ```text
   Hdd1:\Cache
   ```

2. Do stejné složky zkopírujte nový Title Update:

   ```text
   TU_12K2260_0000004000000.0000000000391
   ```

3. Ve složce `Hdd1:\Cache` ponechte pouze **jeden Title Update** pro Dragon Age: Origins.

4. Soubor:

   ```text
   A8EC5967AE2BB73FED98BD4FD23521ECC8DE4FD21
   ```

   zkopírujte do složky:

   ```text
   Hdd1:\Content\0000000000000000\454108C0\00000002
   ```

5. V Auroře nebo jiném používaném dashboardu:

   * obnovte seznam DLC,
   * obnovte seznam Title Updates,
   * aktivujte nový Title Update pro hru.

6. Konzoli úplně restartujte.

---

## Volitelné: počeštění názvů DLC

Tento postup upraví názvy DLC zobrazované v nabídce hry.

### Příprava

1. Vytvořte si na počítači pracovní složku.

2. Do této složky vložte následující soubory:

   ```text
   patch_dao_dlc_packages_local.py
   run_patch_dao_dlc_packages_local.bat
   patched_dlc_metadata.zip
   ```

3. Ve stejné složce vytvořte podsložku:

   ```text
   DLC
   ```

4. Do podsložky `DLC` zkopírujte DLC soubory z Xboxu umístěné v:

   ```text
   Hdd1:\Content\0000000000000000\454108C0\00000002
   ```

### Úprava DLC

1. Spusťte soubor:

   ```text
   run_patch_dao_dlc_packages_local.bat
   ```

2. Skript vytvoří upravené DLC soubory ve složce:

   ```text
   patched_dlc_packages
   ```

### Nahrání do Xboxu

1. Zálohujte původní DLC soubory z Xboxu.

2. Nahraďte pouze ty soubory, které skript vytvořil ve složce `patched_dlc_packages`.

3. Zachovejte:

   * stejné názvy souborů,
   * stejnou cílovou složku:

   ```text
   Hdd1:\Content\0000000000000000\454108C0\00000002
   ```

4. Konzoli úplně restartujte.
