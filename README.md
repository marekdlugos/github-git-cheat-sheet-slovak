# Git cheat sheet

## Translator notes

This file is an unofficial Slovak translation of Git Cheat Sheet from Github that you can find on [Github Resources page](https://services.github.com/resources/).

Slovak language is also very similar to Czech what means that now it's accessible to over 15 million Slovak & Czech people.

---

Git je open-source distribuovaný systém riadenia revízií, ktorému napomáhajú aktivity GitHubu na Vašom notebooku alebo stolnom počítači. Tento cheat sheet sumarizuje bežne používané Git príkazy pre rýchlu referenciu.

Git is the open source distributed version control system that facilitates GitHub activities on your laptop or desktop. This cheat sheet summarizes commonly used Git command line instructions for quick reference.

Inštalácia GITu
GitHub ponúka aplikačných klientov, ktorí môžu zahŕňať aj grafické rozhranie pre najbežnejšie operácie s repozitármi a automaticky aktualizujúci sa command line klient Gitu pre zložitejšie situácie.

Github pre Windows
https://windows.github.com

GitHub pre Mac
https://mac.github.com

Git distribúcie pre Linux a POSIX systémy sú dostupné na oficiálnych stránkach Git SCM.

Git pre všetky platformy
http://git-scm.com

## Konfigurácia
Nakonfigujte si používateľské informácie pre všetky lokálne repozitáre.

```
$ git config --global user.name "[name]"
```
Nastaví meno, ktoré chcete mať priradené k Vašim commitom

```
$ git config --global user.email "[email address]"
```
Nastaví e=mail, ktorý chcete mať priradený k Vašim commitom

```
$ git config --global color.ui auto
```
Umožní napomocné zvýrazňovanie výstupov z príkazového riadka

## Vytváranie repozitárov
Vytvorte nový repozitár alebo použite nejaký z existujúcej URL

```
$ git init [project-name]
```
Vytvorí nový lokálny repozitár s daným názvom

```
$ git clone [url]
```
Stiahne projekt spolu so všetkou históriou verzií

## Robenie zmien
Zrevidujte zmeny a pridajte tie Vaše

```
$ git status
```
Vráti zoznam všetkých nových alebo upravených súborov na commit

```
$ git diff
```
Ukáže rozdiely v súboroch, ktoré ešte neboli stage-nuté

```
$ git add [file]
```
Pridá súbor na prípravu pre versioning

```
$ git diff --staged
```
Ukáže rozdiely v súboroch medzi stage-nutou a poslednou verziou

```
$ git reset [file]
```
Unstage-ne súbor, ale zachová jeho obsah

```
$ git commit -m "[descriptive message]"
```
Zaznamená zmeny v súbore do histórie verzií permanentne

## Skupinové zmeny
Pomenujte sériu commitov a kombinujte Váš progres

```
$ git branch
```
Vráti zoznam všetkých lokálnych vetiev v repozitári

```
$ git branch [branch-name]
```
Vytvorí novú vetvu

```
$ git checkout [branch-name]
```
Zmení vetvu na tú, ktorej názov sme zadali a aktualizuje repozitárový priečinok

```
$ git merge [branch]
```
Zlúči históriu zadanej vetvy do súčasnej vetvy

```
$ git branch -d [branch-name]
```
Zmaže vetvu

## Refaktorizácia súborov
Premiestnenie alebo odstránenie verzovaných súborov

```
$ git rm [file]
```
Zmaže súbor z priečinka a zaznamená, že bol zmazaný

```
$ git rm --cached [file]
```
Odstráni súbor z verzovacieho systému ale zachová súbor lokálne

```
$ git mv [file-original] [file-renamed]
```
Zmení názov súboru a pripraví súbor na commit

## Zakázanie trackovania
Vynechanie dočasných súborov

```
*.log
build/
temp-*
```
Textový súbor nazvaný .gitignore zakáže nechcené verzovanie súborov, ktoré
A text file named .gitignore suppresses accidental versioning of files and paths matching the specified pa erns

```
$ git ls-files --other --ignored --exclude-standard
```
Lists all ignored files in this project

## Ukladanie fragmentov
Shelve and restore incomplete changes

```
$ git stash
```
Temporarily stores all modified tracked files

```
$ git stash pop
```
Restores the most recently stashed files

```
$ git stash list
```
Lists all stashed changesets

```
$ git stash drop
```
Discards the most recently stashed changeset

## Revidovanie histórie
Browse and inspect the evolution of project files

```
$ git log
```
Lists version history for the current branch

```
$ git log --follow [file]
```
Lists version history for a file, including renames

```
$ git diff [first-branch]...[second-branch]
```
Shows content differences between two branches

```
$ git show [commit]
```
Outputs metadata and content changes of the specified commit

## Vrátenie zmien
Zmazanie chýb a nahradenie histórie

```
$ git reset [commit]
```
Vráti všetky commity po [commit], zachovavajúc zmeny lokálne

```
$ git reset --hard [commit]
```
Zahodí všetkú históriu a zmeny až po daný [commit]

## Synchronizácia zmien
Register a repository bookmark and exchange version history

```
$ git fetch [bookmark]
```
Downloads all history from the repository bookmark

```
$ git merge [bookmark]/[branch]
```
Combines bookmark’s branch into current local branch

```
$ git push [alias] [branch]
```
Nahraje commity a zmeny do vetvy na Github

```
$ git pull
```
Stiahne k Vám všetky aktuálne zmeny a históriu

GitHub tréning
Získajte viac informácií o používaní GitHubu a Gitu. Napíšte email nášmu tréningovému tímu training@github.com alebo navštívte našu web stránku pre informácie o vzdelávacích podujatiach a dostupnosti sukromných lekcií.
