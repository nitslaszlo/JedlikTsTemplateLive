# VS Code +  TypeScript + Live Server + TSLint
## A.  Fejlesztői környezet telepítése, beállítása
1.  Node.js letöltése, telepítése:<br>
    https://nodejs.org/en/download/
2.  Node.js command prompt, globális Node.js csomagok telepítése:<br>
    "npm install -g typescript"<br>
    "npm install -g tslint"<br>
    parancsokkal
3.  Git for windows telepítése (opcionális lépés Git-hez):<br>
    https://git-for-windows.github.io/
4.  Visual Studio Code (továbbiakban VSCode) telepítése<br>
    https://code.visualstudio.com/docs/setup/setup-overview
5.  VSCode futtatása, Visual Studio Extensions telepítése: Ctrl-Shift-X<br>
    Kiterjesztés keresése, telepítés:<br>
     - Debugger for Chrome 4.1.0
     - TSLint 1.0.24
     - Live Server 3.1.0
     - vscode-pdf<br>
     (opcionális: további kiterjesztések telepítése igény szerint)
6. Billentyűkombinációk beállítása:<br>
    File\Preferences\Keyboard Shortcuts menüvel, vagy Ctrl-K majd Ctrl-S<br>
    Parancs keresése: gépeléssel<br>
    Hozzárendelés, módosítás: "ceruza" ikonra kattíntással, törlés: Del bill.<br>
    - gépel: "delete" > parancs: "Delete Line" > hozzárendel: Ctrl-L
    - opcionális: további billentyűkombinációk hozzárendelése tetszés szerint
7. Opcionális: VSCode beállítása: lsd. az oldal végén

B.  Projekt előkészítése (inicializálása)
=========================================
1.  https://github.com/nitslaszlo/JedlikTsTemplateLive.git<br>
    JedlikTsTemplateLive-master.zip letöltése, kicsomagolása<br>
    vagy:<br>
    CMD ablak<br>
    "cd projekt_szülőmappa"<br>
    "git clone https://github.com/nitslaszlo/JedlikTsTemplateLive.git"
2.  JedlikTsTemplateLive-master mappa átnevezése tetszőlegesen<br>
    .git mappa törlése, ha clone-al töltötted le és nem vagy társszerző (collaborator)<br>
    Átnevezett mappa helyi menüből: Open with Code,<br>
    vagy a VSCode indítása után File/Open Folder... menüpontba a project mappa megnyitása

## C.  Fejlesztés, tesztelés, kilépés
1.  VSCode indítása (utoljára megnyitott projektet visszatölti), vagy<br>
    Project mappa helyi menüből: Open with Code, vagy<br>
    VSCode indítása után File/Open Folder... menüpontba a project mappa megnyitása
2.  Ctrl-Shift-B => TypeScript források átalakítása JavaScript-re (ts\*.ts => wwwroot/js/game.js)<br>
    (watch üzemmód, az első fordítás után már automatikus a fordítás)<br>
    (amíg aktív a task, addig nem kell (lehet) újraindítani)
3.  Live Server webszerver indítása/megállítása alul az ikonnal<br>
    (változásnál újratölti az oldalt automatikusan)
4.  ts mappában typescript források létrehozása, meglévők szerkesztése<br>
5.  Futtatás: Chrome: http://localhost:8080/<br>
    vagy tesztelés debug üzemmódban: F5 -el
6.  goto 4.pont :-)

## D. Verziók lekérdezése terminálablakból:
TypeScript: tsc -v<br>
Node.js: node -v<br>
git: git --version<br>
npm: npm -v

## E. Komponensek frissítése
VSCode: Automatikus, balra lent a fogaskeréken jelzi, ha új verzió jön ki<br>
VSCode kiterjesztések: Automatikus, balra az Extensions ikon jelzi, ha új verzió jön ki<br>
TypeScript: npm update -g typescript<br>
Node.js: npm install --save-dev @types/node

## F. Hasznos linkek:
http://pgl.ilinov.eu/<br>
https://git-scm.com/book/en/v2<br>
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf<br>
https://fonts.google.com/

## G. Verziókezelés Git-el VS Code-ban (nagyon alap, opcionális):
1. Github account létrehozása:<br>
   https://github.com/<br>
   (nitslaszlo az account név a példában)
2. Git repository létrehozása:<br>
   pl.: GitHub asztali alkalmazással vagy github.com-on<br>
   (JedlikTsTemplateLive a repository neve a példában)
3. Visual Studio Code indítása - project betöltése
4. Git inicializálása a 3. ("Y") ikonnal vagy Ctrl-Shift-G<br>
   majd "Initialize Repository"-ra kattint (felül)
5. Remote repository megadása új terminál ablakból (Ctr-Shift-ö)<br>
   "git remote add origin https://github.com/nitslaszlo/JedlikTsTemplateLive.git"
6. ".gitignore" fájl létrehozása (opcionális):<br>
   Ctrl-N -el új fájl létrehozása<br>
   A fájl tartalma: node_modules<br>
   (További mappák és fájlok megadhatóak, melyek nem kerülnek "feltöltésre")<br>
   Ctrl-S -> .gitignore néven menteni a projekt főkönyvtárába
7. Ctrl-Shift-G -> Commit message megadása, majd commit Ctrl-Enter -el
8. Változások szinkronizálása ("feltöltés")<br>
   Alul a státus sorban balra "Synchronize Changes" -ra kattínt

   
## H. VS Code editor beállítása:
1. Ctrl-Shift-P vagy F1
2. "Preferen..." gépelése
3. Preferences: "Open Workplace Settings" a projektben tárolt beállításokhoz (ez az erősebb) vagy<br>
   Preferences: "Open User Settings" a felasználónált tárolt beállításokhoz<br>
   Konfig fájl workspace: projekt/.vscode/settings.json<br>
   Konfig fájl user: c:/Users/UserName/AppData/Roaming/Code/User/settings.json 