# Git cheat sheet

## Translator notes

> This is a Slovak translation of Git Cheat Sheet from Github that you can find on [Github Resources page](https://services.github.com/resources/).

> Slovak language is also very similar to Czech what means that now it's accessible to over **15 million Slovak & Czech people**.

## Začiatky s Gitom

Git je open-source distribuovaný systém riadenia revízií. Github je služba, na ktorej je možné tieto revízie (repozitáre, projekty) hostovať. Tento cheat sheet sumarizuje bežne používané Git príkazy pre rýchlu referenciu.

## Inštalácia GITu
GitHub ponúka aplikácie pre najbežnejšie operácie s repozitármi alebo rozhranie v príkazovom riadku pre zložitejšie situácie.

Github pre Windows
https://windows.github.com

GitHub pre Mac
https://mac.github.com

Git distribúcie pre Linux a POSIX systémy sú dostupné na oficiálnych stránkach Git SCM.

Git pre všetky platformy
http://git-scm.com

## Konfigurácia
Konfigurácia používateľských informácií na zariadení.

```
$ git config --global user.name "[name]"
```
Nastaví meno, ktoré bude priradené ku commitom

```
$ git config --global user.email "[email address]"
```
Nastaví e-mail, ktorý bude priradený ku commitom

```
$ git config --global color.ui auto
```
Umožní farebné zvýrazňovanie výstupov z príkazového riadku

## Vytváranie repozitárov
Vytváranie nového repozitára alebo používanie už existujúceho

```
$ git init [project-name]
```
Vytvorí nový lokálny repozitár s daným názvom

```
$ git clone [url]
```
Stiahne celý repozitár z danej URL

## Robenie zmien
Zrevidovanie zmien a robenie ďalších

```
$ git status
```
Vráti zoznam všetkých nových alebo upravených súborov

```
$ git diff
```
Ukáže rozdiely v súboroch, ktoré ešte neboli stage-nuté

```
$ git add [file]
```
Pridá súbor do "poolu" pre nový commit

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
Vytvorí commita pridá k nemu správu s opisom zmien, ktoré boli urobené

## Skupinové zmeny
Pomenovanie série commitov a kombinovanie progresu

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
Prepne nás do danej vetvy a aktualizuje súbory

```
$ git merge [branch]
```
Zlúči históriu danej vetvy do súčasnej vetvy

```
$ git branch -d [branch-name]
```
Zmaže vetvu

## Premiestňovanie súborov
Premiestnenie alebo zmazanie verzovaných súborov

```
$ git rm [file]
```
Zmaže súbor z priečinka a zaznamená, že bol zmazaný

```
$ git rm --cached [file]
```
Odstráni súbor z verzovacieho systému, ale zachová súbor lokálne

```
$ git mv [file-original] [file-renamed]
```
Zmení názov súboru a pripraví súbor na commit

## Zakázanie verzovania
Vynechanie súborov, ktoré nechceme verzovať alebo dočasných súborov

```
*.log
build/
temp-*
```
Textový súbor nazvaný .gitignore zakáže verzovanie nechcených súborov alebo priečinkov (väčšinou napr. súbory IDE, heslá).

```
$ git ls-files --other --ignored --exclude-standard
```
Vráti zoznam všetkých ignorovaných súborov v projekte

## Ukladanie menších zmien
Uloženie a obnovenie nedokončených zmien

```
$ git stash
```
Dočasne uloží všetky zmenené súbory

```
$ git stash pop
```
Obnoví posledne stashnuté (uložené) súbory

```
$ git stash list
```
Vráti zoznam všetkých stashnutých (uložených) zmien

```
$ git stash drop
```
Zahodí posledne stashnuté (uložené) zmeny

## Revidovanie histórie
Listovanie a kontrola vývoja súborov

```
$ git log
```
Vráti zoznam commitov v aktuálnej vetve

```
$ git log --follow [file]
```
Vráti zoznam zmien pre daný súbor (zahŕňajúc premenovávania)

```
$ git diff [first-branch]...[second-branch]
```
Zobrazí rozdiely medzi dvoma vetvami

```
$ git show [commit]
```
Vráti metadata a obsah zmien daného commitu

## Vrátenie zmien
Napravenie chýb a nahradenie histórie

```
$ git reset [commit]
```
Vráti všetky urobené zmeny až po daný commit, zachovajúc lokálne zmeny

```
$ git reset --hard [commit]
```
Zahodí všetky urobené zmeny až po daný commit

## Synchronizácia zmien
Zapísanie zmien a stiahnutie alebo nahratie zmien

```
$ git fetch [bookmark]
```
Stiahne všetky zmeny zo vzdialeného do lokálneho repozitára

```
$ git merge [bookmark]/[branch]
```
Zlúči danú vetvu do súčasnej

```
$ git push [alias] [branch]
```
Nahraje commity a zmeny do danej vetvy na Github

```
$ git pull
```
Stiahne k Vám všetky aktuálne zmeny a históriu kódu

---

## GitHub tréning

Získajte viac informácií o používaní GitHubu a Gitu. Napíšte email nášmu tréningovému tímu training@github.com alebo navštívte našu web stránku pre informácie o vzdelávacích podujatiach a dostupnosti sukromných lekcií.
