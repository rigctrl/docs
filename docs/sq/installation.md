### Lidhe RigCtrl ne WiFi

!!! attention ""
    Paisjes i nevojiten disa minuta për t'u ngritur për herë të parë!

1. Nga mobili apo kompjuteri lidhu ne wireless me emrin **RigCtrlSetup**
2. Ne mobil kliko mbi njoftimin **Sign In to network** nëse paraqitet
4. Nëse nuk pranoni njoftimin hapeni [http://192.168.4.1](http://192.168.4.1?target=_blank) në Chrome, Safari apo ndonje tjetër browser
5. Shëno një emër (që do të përdorni me vonë për të marr IP adresën lokale nga  [ip.rigctrl.com](https://ip.rigctrl.com?target=_blank))
6. Zgjidh Wireless e juaj nga lista dhe shëno fjalëkalimin

!!! note ""
    Keni durim deri sa RigCtrl të paraqitet në lidhje

!!! error "Nëse RigCtrlSetup wireless-i del prap online, zakonisht do të thotë që fjalëkalimi që keni shënuar është i gabuar. Përsërit hapat nga hapi 1."
7. Vizito [ip.rigctrl.com](https://ip.rigctrl.com?target=_blank) dhe shëno emrin që keni shënuar ne hapin 5. _Mund të merr 1-2 minuta deri sa IP adresa të paraqitet_
8. Kliko mbi IP adresën për të vazhduar konfigurimin e RigCtrl

### Konfiguro dhe update

1. Krijo përdoruesin
2. Identifikohu
3. Shëno kuleten
4. Nëse keni abonim Premium, shëno email adresën dhe regjistrohu në Viber për të pranuar njoftimet
5. Kliko në linkun për të marr kodin për Viber
6. Shëno informatat për Windows dhe Claymore
7. Ruaj

!!! note ""
    Merr update dhe përmirësimet më të reja duke klikuar ne Updates nga menyja

!!! attention "Pasi të ruani konfigurimin dhe keni bërë uodate, RigCtrl do të filloj të skanoj rrjetën për rig-a. Ky operacion zgjat disa minuta para se rig-at të paraqiten në listë."

### Konfigurimin i Windows

_Që RigCtrl të mund të instaloj dhe konfiguroj Claymore, ndryshoj kuletat, ristartoj Claymore në mënyre optiomale, fik ose ristartoj Windows, Windows-i duhet të konfigurohet si më poshtë:_

1. Merr këtë file **[config.zip](https://rigctrl.com/dl/config.zip?target=_blank)** dhe vendose në secilin rig
3. Nga dritarja e re e hapur, kliko me tastin e djathtë te config.bat dhe zgjedh Run as administrator
4. Shëno informatat e kërkuara nga skripta
5. Në RigCtrl, shëno User dhe Password të Windows-it
    - Meny - Konfigurimet - Konfigurimi i Windows dhe ruaj ndryshimet

!!! important
    Username dhe Password i Windows-it duhet të jetë i njejtë në të gjitha rig-at!

### Konfigurimin i Claymore

!!! note ""
    Nëse keni përfunduar [konfigurimin e Windows](/sq/installation#konfigurimin-i-windows) dhe keni instaluar Claymore nëpërmjet RigCtrl, atëhere mund të tejkaloni këtë pjesë.

Në mënyrë që RigCtrl të kryej veprimet automatike, Claymore duhet të konfigurohet me këto parametra:

- Shto `-mport 3333` në start.bat apo config.txt
- Mund të vendosni fjalëkalimi për Claymore duke shtuar `-mpsw password`
- Shto `-r -1` për ndaluar ristartimet nga Claymore që të mos ndeshën me RigCtrl

!!! important
    Claymore port-a dhe fjalëkalimi duhet të jetë i njejtë në të gjitha rig-at!

!!! attention ""
    Nëse keni vendosur portë ndryshe nga `3333` apo fjalëkalim, ju duhet të vendosni ato parametra në RigCtrl - Konfigurimet - Konfigurimi i Claymore dhe të ruani ndryshimet.

### Konfigurimin i SimpleMining

1. Identifikohu në SimpleMining.net
2. Kliko në **RigList** -> **OPTIONS: wallets** -> Vendos kuletën në **Ethereum address ($walletETH)** -> ruaj duke klikuar në **Save all options and reload all rigs**
3. Kliko në Rig Groups
4. Shto një grup duke klikuar në Add group
5. Zgjidh Claymore (rekomandohet verzioni i fundit) duke klikuar në Select miner
6. Shëno një emër në Group name, psh `RigCtrlGroup`
7. Në Miner OPTIONS vendos konfigurimet e juaja dhe ndyrsho ose shto `-mport 3333`
    - Mund të vendosni fjalëkalim nëse deshironi `-mpsw password`
    - Psh: `epool eu1.ethermine.org:4444 -ewal $walletETH.$rigName -esm 0 -epsw x -allpools 1 -mport 3333`
8. Nëse keni vendosur kuletën si në hapin 2. atëherë mos ndrysho `$walletETH` sepse kuleta vjen automatikisht nga hapi 2.
9. Kliko në RigList
10. Zgjidh të gjitha rig-at
11. Kliko ASSIGN GROUP
12. Zgjidh RigCtrlGroup (apo emrin që ju keni vendosur në hapin 6.) dhe kliko Save

!!! attention ""
    Shëno portën dhe fjalëkalimin nëse e keni përcaktuar në RigCtrl - Konfigurimet - Konfigurimet e Claymore dhe ruaj ndryshimet!