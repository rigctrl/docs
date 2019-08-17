### Menaxhimi i grupeve për instalimin dhe konfigurimin automatik të Claymore

!!! info ""
    Veprimet me Claymore mund të bëhen vetëm nëse keni konfiguruar Windows-in si më lartë

Zakonisht rigat shumicën e parametrave të claymore e kanë të përbashkët si psh kuleta, shpejtësia e ventilatorëve, etj. Ato parametra mund të vendosen në grupe dhe përdoren për disa apo gjithë rigat.

_Me RigCtrl vie një group që quhet `global` dhe sa për fillim ka një komandë të paracaktuar që të gjithë rigat e kanë fillimisht._

Për të shtuar një grup kliko ne **+**

1. Shëno emrin e grupit

    !!! info "Shembull"
        Mund të jetë grup për një lloj të kartelave grafike me emrin `RX580-8GB` ose `RX570-4GBSapphire`

2. Kuleta shënohet vetëm nëse është ndryshe nga kuleta që keni plotësuar më lartë apo dëshironi që grupi të minoj për tjetër kuletë

3. Në Claymore komandën shëno komandën e plotë (përveq kuletës). Për opsionet mundshme shikoni **[dokumentacionin e Claymore](https://www.rigctrl.com/dl/readme.txt?target=_blank)**.

!!! info ""
    Komanda që vie me RigCtrl `-epool eu1.ethermine.org:4444 -cvddc 900 -cclock 1150 -mclock 2000 -tstop 85 -tt 60 -fanmin 35 -fanmax 100 -r -1 -mport 3333`

Nëse ndonjë rig ka mclock, cclock ose cvddc ndryshe nga të tjerët në të njejtin grup, ato mund të vendosen te fushat përkatëse në rig listë më poshtë.

Nëse ndonjë rig ka nevoj të ketë parametra ndryshe nga grupi i përbashkët atëhere ju mund të krijoni një grup të veqantë vetëm për atë rig.

### Menaxhimi i rig-av

1. Në meny kliko te Rig/Grup lista
2. Mund të shtoni një rig duke klikuar **+** ose largoni duke klikuar ne **X**
3. Ndryshoni emrat nëse ka nevojë për identifikim më të lehtë
4. Rregullo ose shëno Min hashrate

    !!! attention ""
        Hashrate-i minimal (Min hashrate) do të thotë që nëse hashrate i rigut bie nër min hashrate atëhere RigCtrl reagon dhe ristarton Claymore, Windows apo reseton rigun që të kthehet në gjendje optimale.

        Është me rëndësi që min hashrate të plotësohet saktë në mënyre që RigCtrl të ju ndihmojë sa më mirë.

5. Zgjidh Portën ku rigu është i lidhur në paisje. Nëse rigu nuk ka portë të zgjedhur atëhere nuk mund të resetohet.
6. Zgjidh grupin përkatës
7. Monitoro
    - Nëse rig-u ka të zgjedhur Monitoro - RigCtrl reagon automatikisht nëse rig-u nuk punon si duhet me veprime si ristartim te Claymore/Windows apo resetim fizik.
    - Nëse doni që një rig të mos monitorohet nga RigCtrl atëherë hiq Monitoro.
    - Monitorimi mund të vendoset apo hiqet edhe nga faqja e parë duke klikuar në menynë e rig-ut.
    - Pavarësisht Monitorimit, veprimet ndaj rigut mund të kryhen manualisht nga faqja e parë.


### Instalimi dhe konfigurimi invdividual i Claymore

1. Vendos parametrat `cvddc`, `mclock` dhe `cclock` të Claymore që janë specifik për një rig në fushat përkatëse të rigut në listë

    !!! info "Example"
        Një rig ka kartela të ndryshme dhe ato kërkojnë cvddc, mclock ose cclock ndryshe nga parametrat që janë në grup. Vendosim në fusha:

        cvddc: 950

        cclock: 1150,1150,1130,1120,1140,1050

        mclock: 2050,2050,2000,1900,2040,2050

    !!! attention ""
        Komanda përfundimtare do të jetë ajo e grupit me përjashtim të këtyre parametrave që janë të vendosura ne rig.

2. Kliko ikonën për të instaluar apo bërë update Claymore
    - Ky veprim instalon/update, kombinon Claymore parametrat në grup me ato individual, konfiguron Claymore në rig dhe e vendosë në startup që Claymore të starton automatikisht kur ngritet Windows
    - Verzioni i Claymore është gjithmonë i fundit
3. Kliko refresh ikonën për të vendosur konfigurimin e ri në rig nëse keni ndryshuar ndonjë prej parametrave
    - Ky veprim ndërron vetëm komanden e Claymore

!!! Warning
    Mos harroni të ruani ndryshimet para se të ekzekutoni ndonjëren prej komandave

### Menaxhimi i rigav nga faqja e pare

Në faqe të parë secili rig ka menynë e vet ku mund ta menaxhoni dhe të merrni veprime të ndryshme

- Kliko more_vert për të hapur listën me veprime
    - Modifiko rigun - Nga kjo dritare mund të ndryshoni të dhënat e rigut si dhe të merrni veprime të ndryshme
    - Teamviewer ID - shfaqet vetëm nëse TeamViewer është i instaluar në rig (kliko për ta kopjuar ID)
    - Ristarto Claymore
    - Monitoro On/Off
    - Ristarto Windows-in
    - Fik Windows-in

    _Komandat më poshtë janë të mundura vetëm për rigat që janë të lidhur në RigCtrl Reset dhe kanë portë të përcaktuar_
    - Reseto - Fik dhe starton rigun fizikisht
    - Fik rrymën
    - Starto - Starton nëse rigu është i fikur
