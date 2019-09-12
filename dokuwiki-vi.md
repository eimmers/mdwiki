####  edit content in VI ####

## Linux ##
```
Voor Chrome had je de plugin wasavi die vi emuleert voor browserpagina's met tekstinvoer (geen idee of die nog bestaat/werkt)
Plugins die een extern programma openen worden door geen enkele browser meer toegestaan, dat moet nu indirect door een combinatie van een plugin die weer een andere actie aanstuurt en daar later een resultaat van terugkrijgt:
withExtEditor is zo'n plugin die voor meerdere browsers bestaat:
Deze plugin start withExtEditorHost
De laatste start dan een de eigenlijke editor met de te bewerken tekst en geeft na opslaan het resultaat terug waarna dat weer in de browser geladen moet worden
Deze oplossing is wat langzamer en foutgevoeliger dan vroegere volledig browsergebaseerde oplossingen, ook is de “reload-knop” van de plugin soms niet voldoende na een configuratiewijziging en moet je de browser herstarten
Algemeen
Installeer de extensie in je browser, bijvoorbeeld Firefox 57+
Download de software voor je OS van de Releases pagina op GitHub (voor source heb je Node.js ≥ 8.9.0 nodig)
maak bijvoorbeeld ~/bin aan voor het uitpakken van dit bestand en je eigen script
pak daar den de “download” uit en draai de installer
de rest van de stappen hangt van je OS af
Gebruik van withExtEditor op Linux met een terminalvenster en vim:
Download en pak uit
Installeer xterm (instructie voor EL 8 als je dat nog niet gedaan hebt):
# dnf -y install xterm
Configureer de software
$ mkdir ~/bin; cd ~/bin/
$ unzip -q ~/Downloads/linux-x86_64.zip index
$ chmod u+x index 
$ ./index setup
[1] firefox
...
Select a browser. [1...5 / 0]: 1
Input editor path: /usr/bin/xterm
Input command line options: -e /usr/bin/vi
..
Created: ~/.config/withexeditorhost/config/firefox/editorconfig.json
Opmerking: gebruik -e /usr/bin/vim als je dat liever hebt

In je browser open je nu de add-ons page, selecteer withExEditor en druk op de [Reload] in de configuratiepagina
Je kan je de host-configuratie aanpassen n:
~/.config/withexeditorhost/config/
of op een Mac in ~/Library/Application Support/withexeditorhost/config/
Opmerkingen:
/usr/bin/gnome-terminal accepteerde het tijdelijke bestand niet als argument bij de laatste test …
You kan een groter xterm-venster configureren:
De executable wordt aangeroepen door shell script ( ~/.config/withexeditorhost/config/firefox/withexeditorhost.sh)
Als je brouwser de gewijzigde temporary files niet meer oppikt, herstart Firefox
Bewaart de temporary files in /tmp/withExEditor/<PID>/tmpfiles/#/##/<site>/name.txt (PID van de index executable), dus in het uiterste geval vind je daar je “verlogen werk” terug!

```

## MAcosx ##
```
Gebruik het zelfde script als voor It's all text:
#!/bin/sh
# open your faviorite editor and save the file to: $HOME/bin/alltext.sh
# http://blog.asyd.net/2009/09/using-its-all-text-on-mac-os-x/
# http://www.macosxhints.com/article.php?story=20040617170055379

if [ -z $1 ]; then
echo "No filename was given as args."
exit;
fi

exec /usr/bin/osascript $HOME/bin/vim-terminal.scpt "$1"
osascript
#!/usr/bin/osascript
# save to $HOME/bin/vim-terminal.scpt
##on run argv
### from http://superuser.com/questions/299482/how-do-i-set-up-an-applescript-to-open-a-new-iterm2-tab-and-change-the-directory
##tell application "iTerm"
##make new terminal
##tell the current terminal
##activate current session
##launch session “Default Session”
##tell the last session
##set filename to item 1 of argv
##write text "vim" & quoted form of filename & "; exit"
##end tell
##end tell
##end tell
##end run
# Terminal equivalent:
# http://apple.stackexchange.com/questions/115994/terminal-app-equivalent-of-xterm-e-cmd
on run argv
  set filename to item 1 of argv
  tell application "Terminal"
    activate
    do script ("/usr/bin/vi" & " " & quoted form of filename  & "; exit")
  end tell
end run
    #do script ("/usr/bin/vi" & quoted form of filename  & "; exit")
    #write text "/usr/bin/vi" & quoted form of filename  & "; exit"
Configureer de “host”
$ cd ~/bin/
$ mkdir withextedit; cd withextedit
$ unzip -q ~/Downloads/macos.zip
$ chmod u+x index 
$ ./index setup
Enter which browser you would like to set up the host for:
[firefox chrome chromium vivaldi]
firefox
Enter editor path:
/Users/joachim/bin/alltext.sh
Enter command line options:
 
Created: /Users/joachim/Library/Application Support/withexeditorhost/config/firefox/editorconfig.json
Ga naar de “Add-Ons pagina in Firefox, selecteer de extensie en klik ”[Reload]“
De tijdelijke bestanden staan ergens onder /var/folders in een sub-directory van withExEditor
```


