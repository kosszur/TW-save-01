
# [GitHub Pages documentation](https://docs.github.com/en/pages)

Ismerje meg, hogyan hozhat létre webhelyet közvetlenül a GitHub.com tárhelyéből. Fedezze fel a webhely-építő eszközöket, például a Jekyll-t, és oldja meg a GitHub Pages webhelyével kapcsolatos problémákat.

## [Quickstart for GitHub Pages](https://docs.github.com/en/pages/quickstart)

A GitHub Pages nyilvános tárolókban érhető el a GitHub Free és a GitHub Free szolgáltatásokkal a szervezetek számára, valamint nyilvános és privát tárolókban a GitHub Pro, a GitHub Team, a GitHub Enterprise Cloud és a GitHub Enterprise Server szolgáltatással.

### Bevezetés

A GitHub oldalak a GitHubon keresztül tárolt és közzétett nyilvános weboldalak. A leggyorsabb módja annak, hogy elinduljon és elinduljon, ha a Jekyll témaválasztót használja egy előre elkészített téma betöltéséhez. Ezután módosíthatja a GitHub-oldalak tartalmát és stílusát.

Ez az útmutató végigvezeti Önt egy felhasználói webhely létrehozásán a username.github.io címen.

### [Creating your website](https://docs.github.com/en/pages/quickstart#creating-your-website)

- Bármely oldal jobb felső sarkában használja a legördülő menüt, és válassza az `New repository` lehetőséget.
- Adja meg a `username.github.io` repo neveként. 
- A lerakat neve alatt kattintson a `Settings` lehetőségre. (Ha nem látod ... menüt nyomd meg.)
- `Pages` > `Deploy from a branch` > Branch legördülőben 
- tartalomnak mindenképpen lennie kell az oldalon. Akár egy readme.md, ekkor abból generál oldalt.
- Látogassa meg a username.github.io webhelyet az új webhely megtekintéséhez. Ne feledje, hogy **akár 10 percig is eltarthat**, amíg a webhelyen végrehajtott módosítások közzétételre kerülnek, miután a módosításokat átküldte a GitHubra.

### [Cím és leírás módosítása](https://docs.github.com/en/pages/quickstart#changing-the-title-and-description)

`_config.yml` fájlban

```
theme: jekyll-theme-minimal
title: Octocat's homepage
description: Bookmark this to keep an eye on my project updates!
```

## [About GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)

### [About GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#about-github-pages)

A GitHub Pages egy statikus webhely-tárhelyszolgáltatás, amely a HTML-, CSS- és JavaScript-fájlokat közvetlenül a GitHubon található tárolóból veszi, opcionálisan futtatja a fájlokat egy összeállítási folyamaton keresztül, és közzétesz egy webhelyet. A GitHub Pages-webhelyekre példákat láthat a [GitHub-oldalak példagyűjteményében](https://github.com/collections/github-pages-examples)

### [A GitHub Pages webhelyek típusai](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites)

Háromféle GitHub Pages-webhely létezik: projekt, a felhasználó és szervezet.

- A projektoldalak egy adott GitHubon tárolt projekthez kapcsolódnak, például egy JavaScript-könyvtárhoz vagy egy receptgyűjteményhez.
   - `http(s)://<username>.github.io/<repository>` vagy `http(s)://<organization>.github.io/<repository>`
- A felhasználói és szervezeti webhelyek egy adott fiókhoz kapcsolódnak a GitHub.com webhelyen.
  - `<username>.github.io` repóból: `http(s)://<username>.github.io`
  - `<organization>.github.io` repóból: `http(s)://<organization>.github.io`

További információért arról, hogy az egyéni domainek hogyan befolyásolják webhelye URL-címét, olvassa el az „[Az egyéni domainekről és a GitHub-oldalakról](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)” című részt.

GitHubon minden fiókhoz csak egy felhasználót vagy szervezeti webhelyet hozhat létre. A projektoldalak száma korlátlan, akár szervezet tulajdonában, akár személyes fiókban van.


### [Közzétételi források a GitHub Pages webhelyekhez](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#publishing-sources-for-github-pages-sites)

**Figyelmeztetés: A GitHub Pages webhelyei nyilvánosan elérhetők az interneten, még akkor is, ha a webhely tárolója privát.**

A webhelyet közzéteheti, amikor a módosítások egy adott ágba kerülnek, vagy írhat egy GitHub Actions munkafolyamatot a webhely közzétételéhez.

Ha nincs szüksége a webhely felépítési folyamatának ellenőrzésére, javasoljuk, hogy tegye közzé webhelyét, amikor a módosítások egy adott branch-be kerülnek. Megadhatja, hogy melyik branch és mappát használja közzétételi forrásként. A forrás ág a repó bármely branch-e lehet, a forrásmappa pedig lehet a repo gyökere (`/`) a forráságon, vagy egy `/docs` mappa a forráságon. 
Amikor a módosításokat a forrás branch-be küldi, a forrásmappában végrehajtott módosítások megjelennek a GitHub Pages webhelyén.

Ha a Jekylltől eltérő összeállítási folyamatot szeretne használni, vagy nem szeretné, hogy egy dedikált branch tárolja a lefordított statikus fájlokat, javasoljuk, hogy írjon egy GitHub Actions munkafolyamatot a webhely közzétételéhez. A GitHub kezdő munkafolyamatokat biztosít a gyakori közzétételi forgatókönyvekhez, hogy segítse a munkafolyamat megírását.

További információért lásd: [„Közzétételi forrás konfigurálása a GitHub Pages-webhelyhez](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)”.

### [Static site generators](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#static-site-generators)

A GitHub Pages közzétesz minden statikus fájlt, amelyet Ön a tárhelyre küld. Létrehozhatja saját statikus fájljait, vagy statikus webhelygenerátort használhat a webhely létrehozásához. Személyre szabhatja saját összeállítási folyamatát helyileg vagy egy másik szerveren.

Ha egyéni összeállítási folyamatot vagy a Jekylltől eltérő statikus webhelygenerátort használ, írhat egy GitHub-műveletet a webhely felépítéséhez és közzétételéhez. A GitHub indító munkafolyamatokat biztosít számos statikus helygenerátor számára. További információért lásd: „Közzétételi forrás konfigurálása a GitHub Pages-webhelyhez”.

Ha webhelyét egy forráságból teszi közzé, a GitHub Pages alapértelmezés szerint a Jekyll segítségével hozza létre webhelyét. Ha a Jekylltől eltérő statikus webhelygenerátort szeretne használni, javasoljuk, hogy írjon egy GitHub-műveletet a webhely létrehozásához és közzétételéhez. Ellenkező esetben tiltsa le a Jekyll összeállítási folyamatot egy `.nojekyll` nevű üres fájl létrehozásával a közzétételi forrás gyökerében, majd kövesse a statikus webhelygenerátor utasításait a webhely helyi felépítéséhez.

A GitHub Pages nem támogatja az olyan szerveroldali nyelveket, mint a PHP, Ruby vagy Python.

### [Limits on use of GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#limits-on-use-of-github-pages)

#### [Tiltott felhasználások](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#prohibited-uses)

A GitHub Pages nem használható ingyenes webtárhely-szolgáltatásként, illetve nem engedélyezett az online üzlet, az e-kereskedelmi webhely vagy bármely más olyan webhely működtetéséhez, amely elsősorban kereskedelmi tranzakciók elősegítésére vagy kereskedelmi szoftverek szolgáltatásként való biztosítására irányul ( SaaS). A GitHub Pages webhelyeit nem szabad kényes tranzakciókra, például jelszavak vagy hitelkártyaszámok küldésére használni.

Ezenkívül a GitHub-oldalak használatára a GitHub Általános Szerződési Feltételei vonatkoznak, beleértve a gyors gazdagodási tervekre, a szexuálisan obszcén tartalmakra, valamint az erőszakos vagy fenyegető tartalomra vagy tevékenységre vonatkozó korlátozásokat.

#### [Usage limits](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#usage-limits)

A GitHub Pages webhelyekre a következő használati korlátozások vonatkoznak:

- A GitHub Pages forrástárolóinak ajánlott korlátja 1 GB. További információért lásd: „A nagy fájlok a GitHubon”
- A közzétett GitHub-oldalak mérete nem haladhatja meg az 1 GB-ot.
- A GitHub Pages üzembe helyezései időtúllépnek, ha 10 percnél tovább tartanak.
- A GitHub Pages webhelyeken havi 100 GB-os lágy sávszélességkorlát van.
- A GitHub Pages-webhelyeken óránként 10 felépítésre van korlátozva. Ez a korlátozás nem érvényes, ha webhelyét egyéni GitHub-műveletek munkafolyamattal hozza létre és teszi közzé
- Annak érdekében, hogy az összes GitHub-oldalon a szolgáltatás minősége egyenletes legyen, díjkorlátok vonatkozhatnak. Ezek a sebességkorlátok nem akadályozzák a GitHub-oldalak jogszerű használatát. Ha a kérése sebességkorlátozást vált ki, megfelelő választ kap 429-es HTTP-állapotkóddal, valamint egy informatív HTML törzset.

#### [MIME types on GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

A MIME-típus egy fejléc, amelyet a kiszolgáló küld a böngészőnek, és információt ad a böngésző által kért fájlok természetéről és formátumáról. A GitHub Pages több mint 750 MIME-típust támogat több ezer fájlkiterjesztésen keresztül. A támogatott MIME-típusok listája a [mime-db](https://github.com/jshttp/mime-db) projektből jön létre.

Further reading

- [GitHub Pages](https://github.com/skills/github-pages) on GitHub Skills
- "[Repositories](https://docs.github.com/en/rest/repos#pages)"


### [Creating a GitHub Pages site](https://docs.github.com/en/pages/quickstart#creating-your-website)

#### [Creating a repository for your site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site)

Létrehozhat egy repot, vagy választhat egy meglévő repot a webhelyéhez.

Ha GitHub Pages-webhelyet szeretne létrehozni egy olyan repóhoz, ahol a repóban lévő összes fájl nem kapcsolódik a webhelyhez, akkor konfigurálhat egy közzétételi forrást a webhelyéhez. Például rendelkezhet egy dedikált ággal és mappával a webhely forrásfájljainak tárolására, vagy használhat egyéni GitHub Actions munkafolyamatot a webhely forrásfájljainak létrehozásához és üzembe helyezéséhez.

Ha a repót birtokló fiók a GitHub Free vagy a GitHub Free szervezeteket használja, akkor a tárhelynek nyilvánosnak kell lennie.

Ha egy meglévő tárhelyen szeretne webhelyet létrehozni, ugorjon a [„Webhely létrehozása](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site)” szakaszra.

- jobb felső sarokban legördülő menüben `New repository`
- repo név: `<user>.github.io` (kisbetűket kell használnod)
- hozz létre README fájlt

#### [Webhely létrehozása](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site)

Mielőtt létrehozná webhelyét, rendelkeznie kell egy repoval a GitHubon. Ha nem egy meglévő repoba hozza létre webhelyét, olvassa el a [„Leraktár létrehozása a webhelyhez](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site)” című részt.

**Figyelmeztetés: A GitHub Pages webhelyei nyilvánosan elérhetők az interneten, még akkor is, ha a webhely tárolója privát.**

- A GitHubon navigáljon webhelye repójához.
- Döntse el, melyik közzétételi forrást szeretné használni. További információért lásd: [„Közzétételi forrás konfigurálása a GitHub Pages-webhelyhez”](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
- Hozzon létre belépési fájlt a webhelyéhez. A GitHub Pages egy index.html, index.md vagy README.md fájlt keres a webhely belépési fájljaként.
  - Ha a közzétételi forrás egy branch és egy mappa, a bejegyzésfájlnak a forrásmappa legfelső szintjén kell lennie a forráságon. Ha például a közzétételi forrás a `docs` mappa a `main` ágon, akkor a belépési fájlnak a `main` nevű branch `/docs` mappájában kell lennie.
  - Ha a közzétételi forrás egy GitHub Actions-munkafolyamat, akkor a telepített mellékterméknek tartalmaznia kell a bejegyzés legfelső szintjén lévő fájlt. Ahelyett, hogy hozzáadná a bejegyzési fájlt a repóhoz, dönthet úgy, hogy a GitHub Actions munkafolyamat létrehozza a belépési fájlt a munkafolyamat futásakor.

- Konfigurálja a közzétételi forrást. További információért lásd: [„Közzétételi forrás konfigurálása a GitHub Pages-webhelyhez”](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
- A repó neve alatt kattintson a `Settings` lehetőségre. (Ha nem látja, akkor előtte a ...-re.) > `Pages` > `Visit site`

Megjegyzés: Akár 10 percig is eltarthat, amíg a webhelyen végrehajtott módosítások közzétételre kerülnek, miután a módosításokat átküldte a GitHubra. Ha egy óra elteltével sem látja a GitHub Pages-webhely módosításait, olvassa el „A GitHub Pages-webhelyek Jekyll-összeállítási hibáiról” című részt.

- Az Ön GitHub Pages-webhelye egy GitHub Actions munkafolyamattal készült és kerül bevezetésre. További információért lásd a [„Munkafolyamat futási előzményeinek megtekintése”](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/viewing-workflow-run-history) című részt.

Megjegyzés: A GitHub Actions ingyenes a nyilvános adattárak számára. Használati díjak vonatkoznak a privát és belső tárhelyekre, amelyek túllépik a havi ingyenes perceket. További információkért lásd a „Használati korlátok, számlázás és adminisztráció” című részt.

Megjegyzések:

- Ha branch-ből tesz közzé, és webhelye nem jelent meg automatikusan, győződjön meg arról, hogy valaki rendszergazdai jogosultságokkal és ellenőrzött e-mail-címmel rendelkezik a közzétételi forráshoz.

- A `GITHUB_TOKEN`-t használó GitHub Actions munkafolyamat által végrehajtott véglegesítések nem indítanak el GitHub Pages-összeállítást.

#### [Next steps](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#next-steps)

További új fájl létrehozásával további oldalakat is hozzáadhat webhelyéhez. Minden egyes fájl elérhető lesz a webhelyén a közzétételi forrással azonos könyvtárstruktúrában. Például, ha a projekt webhelyének közzétételi forrása a `gh-pages` branch, és létrehoz egy új fájlt `/about/contact-us.md` néven a `gh-pages` ágban, akkor a fájl elérhető lesz a `https://<user>.github.io/<repository>/about/contact-us.html` címen

Témát is hozzáadhat webhelye megjelenésének és hangulatának testreszabásához. További információért olvassa el a [„Téma hozzáadása a GitHub Pages webhelyéhez a Jekyll segítségével”](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll) című részt.

Ha még jobban testre szeretné szabni webhelyét, használhatja a Jekyll-t, egy statikus webhelygenerátort, amely beépített támogatással rendelkezik a GitHub Pages számára. További információért lásd: [„A GitHub oldalakról és a Jekyllről”](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).


Further reading

- ["Troubleshooting Jekyll build errors for GitHub Pages sites"](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites)
- ["Creating and deleting branches within your repository"](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository)
- ["Creating new files"](https://docs.github.com/en/repositories/working-with-files/managing-files/creating-new-files)
- ["Troubleshooting 404 errors for GitHub Pages sites"](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)


## [Egyéni munkafolyamatok használata a GitHub oldalakkal](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)

Kihasználhatja a GitHub Actions és GitHub Pages előnyeit egy munkafolyamat-fájl létrehozásával vagy az előre meghatározott munkafolyamatok kiválasztásával.

...

## [Közzétételi forrás konfigurálása a GitHub Pages webhelyhez](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

Beállíthatja a GitHub Pages-webhelyet úgy, hogy közzétegye, amikor a módosítások egy adott ágba kerülnek, vagy írhat egy GitHub-műveletek munkafolyamatot a webhely közzétételéhez.

>**Ki használhatja ezt a funkciót**
>
>Egy adattárhoz rendszergazdai vagy karbantartói jogosultsággal rendelkező személyek konfigurálhatnak közzétételi forrást a GitHub Pages-webhelyekhez.

### [A források publikálásáról](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#about-publishing-sources)

....

### [Branchből publikálás](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-from-a-branch)

...

#### [Fióktelepről történő közzététel hibaelhárítása](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#troubleshooting-publishing-from-a-branch)

Megjegyzés: Ha a tárhely **szimbolikus hivatkozásokat** tartalmaz, közzé kell tennie webhelyét egy GitHub Actions munkafolyamat segítségével. A GitHub-műveletekkel kapcsolatos további információkért lásd a [„GitHub Actions dokumentációját”](https://docs.github.com/en/actions).

Ha meg szeretné találni a felépítéssel vagy a telepítéssel kapcsolatos lehetséges hibákat, ellenőrizze a GitHub Pages-webhelyen futó munkafolyamatot a lerakat munkafolyamat-futtatásainak áttekintésével. További információért lásd: „A [munkafolyamat futási előzményeinek megtekintése”](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/viewing-workflow-run-history). A munkafolyamat hiba esetén történő újrafuttatásával kapcsolatos további információkért tekintse meg a [„Munkafolyamatok és feladatok újrafuttatása”](https://docs.github.com/en/actions/managing-workflow-runs/re-running-workflows-and-jobs) című részt.

### [Közzététel egyéni GitHub Actions munkafolyamattal](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow)







https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages

