Till att börja med kan använda GitHubs webgui eller använda `GitHub Desktop` för att gära ändringar.  

WebGUI:t finns i två varianter:

* Edit in Place
* github.dev

![](./images/2023-07-10-11-25-00.png)

`github.dev` är en komplett webversion av `VS Code`, men den saknar stöd för många Extensions.

För mer omfattande ändringar med full kontroll är det bäst att arbeta med en lokal klon och ett rent Git-verktyg.  

Men `GitHub Desktop` bör fungera bra för ditt behov.

#### 3.1 Ladda ner repot

Om du inte ingår i DJI Swedens wiki-team måste du skapa en `Fork` till ditt eget GitHub-konto med `Fork - + Create a new fork`

![Create a new fork](./images/2023-07-06-15-57-24.png)

Sedan kopierar du ner hela wiki-repot till din egen maskin med kommandot

`git clone https://GitHub.com/DJI-Sweden/wiki_repo.git`

Byt ut URL mot din egen `fork` om du använder en sådan.

#### 3.2 Skapa en lokal arbetsyta

Eftersom huvudspåret `master` är uppsatt på GitHub med krav på granskning kan du inte skicka upp ändringar du gjort lokalt direkt. Du måste istället skapa en egen arbetsyta (branch).

Innan du skapar en ny arbetsyta måste du försäkra dig om att ditt lokala repo är upp to date med kommandot

`git pull`

Sedan kan du skapa din arbetsyta

`git checkout -b <arbetsnamn>`

Synka sedan upp din arbetsyta till GitHub

`git push --set-upstream origin <arbetsnamn>`

#### 3.3 Skapa återställningspunkter

Du kan spara din status i din lokala arbetsyta genom att göra `commits`.

`git add .`  
`git commit -m'<beskriv typ av ändring>'`

#### 3.4 Synka din arbetsyta med GitHub

Din arbetsarea synkar du sedan till GitHub med

`git push`

Ta som vana att göra detta direkt efter du sparat status för din Git (`commit`) så har du alltid en aktuell version på GitHub.

Synken tar bara med det som du gjort `commit` på.