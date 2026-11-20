# Publishing an update

Mira Updater reads `ota/<device>.json` from the `main` branch of
[MIRACLO-Project/MIRACLO](https://github.com/MIRACLO-Project/MIRACLO). A device can point
elsewhere with `ro.miraclo.ota.url` (a folder URL ending in `/`).

1. Build the signed OTA zip (the `otapackage` target) and upload it as a release asset.
2. On the server, from the source tree:

   ```
   MIRACLO_VERSION=1.1 MIRACLO_CODENAME=Aurora \
     python3 vendor/mira/packages/MiraUpdater/make-ota-json.py \
     out/target/product/marble/miraclo_marble-ota.zip \
     https://github.com/MIRACLO-Project/MIRACLO/releases/download/1.1/miraclo_marble-ota.zip \
     "First change" "Second change" > marble.json
   ```

3. Commit `marble.json` to `ota/` in MIRACLO-Project/MIRACLO.

Phones on an older build see the update the next time they check (daily, or from
Settings › Software update). The update streams straight into the inactive slot, so the zip must
stay downloadable while people update.
