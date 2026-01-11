![OWASP Logo](../assets/TOP_10_logo_Final_Logo_Colour.png)

# Deset nejkritičtějších bezpečnostních rizik webových aplikací

# Úvod

Vítejte u osmé vydání OWASP Top Ten!

Velké poděkování patří všem, kteří přispěli daty a svými pohledy v rámci průzkumu. Bez vás by toto vydání nebylo možné. **Děkujeme!**


## Představení OWASP Top 10:2025



* [A01:2025 - Nedostatečné řízení přístupu (Broken Access Control)](A01_2025-Broken_Access_Control.md)
* [A02:2025 - Chybná bezpečnostní konfigurace (Security Misconfiguration)](A02_2025-Security_Misconfiguration.md)
* [A03:2025 - Selhání dodavatelského řetězce softwaru (Software Supply Chain Failures)](A03_2025-Software_Supply_Chain_Failures.md)
* [A04:2025 - Kryptografická selhání (Cryptographic Failures)](A04_2025-Cryptographic_Failures.md)
* [A05:2025 - Injekce (Injection)](A05_2025-Injection.md)
* [A06:2025 - Nezabezpečený návrh (Insecure Design)](A06_2025-Insecure_Design.md)
* [A07:2025 - Selhání autentizace (Authentication Failures)](A07_2025-Authentication_Failures.md)
* [A08:2025 - Selhání integrity softwaru nebo dat (Software or Data Integrity Failures)](A08_2025-Software_or_Data_Integrity_Failures.md)
* [A09:2025 - Selhání bezpečnostního logování a alertingu (Security Logging & Alerting Failures)](A09_2025-Security_Logging_and_Alerting_Failures.md)
* [A10:2025 - Nesprávné zpracování výjimečných stavů (Mishandling of Exceptional Conditions)](A10_2025-Mishandling_of_Exceptional_Conditions.md)


## Co se změnilo v OWASP Top 10 pro rok 2025

V OWASP Top 10 pro rok 2025 se objevují dvě nové kategorie a jedno sloučení stávajících kategorií. Při tvorbě jsme se snažili co nejvíce zachovat zaměření na příčiny problémů, nikoli pouze na jejich projevy. Vzhledem ke složitosti softwarového inženýrství a bezpečnosti softwaru je však prakticky nemožné vytvořit deset kategorií bez určité míry překryvu.

![Mapping](../assets/2025-mappings.png)

* **[A01:2025 - Nedostatečné řízení přístupu (Broken Access Control)](A01_2025-Broken_Access_Control.md)** si zachovává #1 místo jako nejzávažnější bezpečnostní riziko aplikací; poskytnutá data ukazují, že v průměru 3,73 % testovaných aplikací mělo jednu nebo více z 40 CWE v této kategorii. Jak je naznačeno přerušovanou čarou na výše uvedeném obrázku, Server-Side Request Forgery (SSRF) bylo do této kategorie zařazeno.
* **[A02:2025 - Chybná bezpečnostní konfigurace (Security Misconfiguration)](A02_2025-Security_Misconfiguration.md)** se posunula z #5 místa v roce 2021 na #2 místo v roce 2025. Chybné konfigurace jsou v datech tohoto cyklu zastoupeny ve větší míře. 3,00 % testovaných aplikací mělo jednu nebo více z 16 CWE v této kategorii. To souvisí s tím, že chování aplikací je ve stále větší míře řízeno konfigurací.
* **[A03:2025 - Selhání dodavatelského řetězce softwaru (Software Supply Chain Failures)](A03_2025-Software_Supply_Chain_Failures.md)** představuje rozšíření položky [A06:2021-A06:2021 – Zranitelné a zastaralé komponenty](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/) a zahrnuje širší rozsah kompromitací, ke kterým dochází v rámci nebo napříč ekosystémem softwarových závislostí, build systémů a distribuční infrastruktury. Tato kategorie získala v komunitním průzkumu vysokou míru pozornosti. Obsahuje 5 CWE a má omezené zastoupení v nasbíraných datech. Tato kategorie má nejmenší počet výskytů, ale zároveň nejvyšší průměrné skóre zneužitelnosti a dopadu podle CVE.
* **[A04:2025 - Kryptografická selhání (Cryptographic Failures)](A04_2025-Cryptographic_Failures.md)** klesla v pořadí o dvě pozice z #2 místa na #4 místo. Poskytnutá data ukazují, že v průměru 3,80 % aplikací mělo jednu nebo více z 32 CWE v této kategorii. Tato kategorie často vede k úniku citlivých dat nebo ke kompromitaci systému.
* **[A05:2025 - Injekce (Injection)](A05_2025-Injection.md)** klesla o dvě pozice z #3 místa na #5 místo a zachovala si své relativní postavení vůči položkám Kryptografická selhání a Nezabezpečený návrh. Injekce patří mezi nejčastěji testované kategorie a je s nimi spojeno největší množství CVE, vztahujících se k 38 CWE v této kategorii. Zahrnují problémy od Cross-site Scripting (vysoká četnost / nízký dopad) po SQL Injection (nízká četnost / vysoký dopad).
* **[A06:2025 - Nezabezpečený návrh (Insecure Design)](A06_2025-Insecure_Design.md)** klesl v pořadí o dvě pozice z #4 místa na #6 místo, protože jej předstihly položky Chybná bezpečnostní konfigurace a Selhání dodavatelského řetězce softwaru. Tato kategorie byla zavedena v roce 2021 a v odvětví byly zaznamenány znatelné zlepšení v oblasti modelování hrozeb a větší důraz na bezpečný návrh.
* **[A07:2025 - Selhání autentizace (Authentication Failures)](A07_2025-Authentication_Failures.md)** si udržuje #7 místo s mírnou změnou názvu (dříve „Identification and Authentication Failures“), aby přesněji odpovídal 36 CWE zahrnutým v této kategorii. Tato kategorie zůstává významná, avšak zvýšené používání standardizovaných frameworků pro autentizaci se projevuje pozitivním dopadem na výskyt selhání autentizace.
* **[A08:2025 - Selhání integrity softwaru nebo dat (Software or Data Integrity Failures)](A08_2025-Software_or_Data_Integrity_Failures.md)** zůstává na #8 místě v seznamu. Tato kategorie se zaměřuje na selhání při zachování hranic důvěry a ověřování integrity softwaru, kódu a datových artefaktů, a to na nižší úrovni než Selhání dodavatelského řetězce softwaru. 
* **[A09:2025 - Selhání bezpečnostního logování a alertingu (Security Logging & Alerting Failures)](A09_2025-Security_Logging_and_Alerting_Failures.md)** si zachovává #9 místo. Tato kategorie má mírně upravený název (dříve „Security Logging and Monitoring Failures“), aby byl zdůrazněn význam funkce alertingu potřebné k vyvolání odpovídající reakce na relevantní logovací události. Kvalitní logování bez alertingu má jen omezenou hodnotu při identifikaci bezpečnostních incidentů. Tato kategorie je v datech trvale podreprezentována a její zařazení do seznamu bylo opět potvrzeno hlasováním účastníků komunitního průzkumu.
* **[A10:2025 - Nesprávné zpracování výjimečných stavů (Mishandling of Exceptional Conditions)](A10_2025-Mishandling_of_Exceptional_Conditions.md)** je nová kategorie pro 2025. Tato kategorie obsahuje 24 CWE a zaměřuje se na nesprávné zpracování chyb, logické chyby, selhání do otevřeného stavu (failing open) a další související scénáře vyplývající z abnormálních stavů, se kterými se systémy mohou setkat.


## Metodika

Toto vydání OWASP Top Ten je založené na datech, nikoli však bezvýhradně řízené daty. Na základě poskytnutých dat bylo seřazeno 12 kategorií a dvě z nich byly povýšeny nebo zvýrazněny na základě odpovědí z komunitního průzkumu. K tomuto postupu existuje základní důvod: analýza poskytnutých dat je v podstatě pohledem do minulosti. Výzkumníci v oblasti bezpečnosti aplikací věnují čas identifikaci nových zranitelností a vývoji nových testovacích metod. Začlenění těchto testů do nástrojů a procesů trvá týdny až roky. V době, kdy je možné určitou slabinu spolehlivě testovat ve velkém měřítku, již mohou uplynout roky. Existují také významná rizika, která nemusí být nikdy možné spolehlivě testovat, a proto se v datech nemusí objevit. Pro vyvážení tohoto pohledu se využívá komunitní průzkum, ve kterém jsou odborníci na bezpečnost aplikací a vývojáři dotazováni na rizika, která považují za zásadní, přestože mohou být v testovacích datech nedostatečně zastoupena.


## Jak jsou kategorie strukturovány

Některé kategorie se oproti předchozímu vydání OWASP Top Ten změnily. Níže je uveden přehled změn na vysoké úrovni.

V tomto vydání jsme si vyžádali data bez omezení na konkrétní CWEs, jak tomu bylo v edici 2021. Požadovali jsme počet aplikací testovaných v daném roce (počínaje rokem 2021) a počet aplikací, u nichž byla při testování nalezena alespoň jedna instance daného CWE. Tento formát nám umožňuje sledovat, jak rozšířené jsou jednotlivé CWEs v populaci aplikací. Frekvenci pro naše účely nezohledňujeme; ačkoli může být v jiných situacích užitečná, v tomto kontextu pouze zakrývá skutečnou míru výskytu v populaci aplikací. Zda má aplikace čtyři instance určitého CWE, nebo 4 000 instancí, není součástí výpočtu pro Top Ten. To je obzvláště důležité vzhledem k tomu, že manuální testeři mají tendenci uvádět zranitelnost pouze jednou bez ohledu na to, kolikrát se v aplikaci opakuje, zatímco automatizované testovací frameworky evidují každou instanci zranitelnosti jako samostatnou. Posunuli jsme se z přibližně 30 CWE v roce 2017, přes téměř 400 CWE v roce 2021, až na 589 CWE analyzovaných v tomto vydání datového souboru. Do budoucna plánujeme provést další datové analýzy jako doplněk. Tento výrazný nárůst počtu CWE si vyžádal změny ve způsobu strukturování kategorií.

Strávili jsme několik měsíců seskupováním a kategorizací CWE a mohli bychom v tom pokračovat i další měsíce. V určitém bodě jsme však museli proces ukončit. Existují CWE, které reprezentují základní příčiny (root cause), a CWE, které popisují projevy (symptomy). Příklady CWE typu základní příčina jsou „Cryptographic Failure“ nebo „Misconfiguration“, zatímco příklady symptomatických CWE jsou „Sensitive Data Exposure“ nebo „Denial of Service“. Rozhodli jsme se, kdykoli je to možné, zaměřit na základní příčinu, protože je to logičtější z hlediska identifikace problému a návrhu nápravných opatření. Zaměření na základní příčinu namísto symptomu není nový koncept; OWASP Top Ten vždy obsahoval kombinaci symptomů a základních příčin. Stejně tak samotné CWE představují kombinaci obou přístupů; v tomto vydání jsme pouze důslednější v jejich explicitním rozlišení. Průměrně připadá v tomto vydání přibližně 25 CWE na jednu kategorii, přičemž spodní hranice je 5 CWE u kategorií A03:2025 – Software Supply Chain Failures a A09:2025 – Security Logging and Alerting Failures, a horní hranice je 40 CWE u kategorie A01:2025 – Broken Access Control. Rozhodli jsme se stanovit horní limit počtu CWE v jedné kategorii na 40. Tato aktualizovaná struktura kategorií přináší další přínosy v oblasti školení, protože organizace se mohou zaměřit na CWE, které dávají smysl pro konkrétní programovací jazyk nebo framework. 

Byli jsme dotázáni, proč jsme nepřešli na seznam 10 konkrétních CWE jako Top Ten, podobně jako MITRE Top 25 Most Dangerous Software Weaknesses. Existují dva hlavní důvody, proč používáme v kategoriích více CWE. Zaprvé, ne všechny CWE existují ve všech programovacích jazycích nebo frameworkech. To způsobuje problémy u nástrojů a vzdělávacích či osvětových programů, protože část Top Ten by nemusela být použitelná. Druhým důvodem je skutečnost, že pro běžné typy zranitelností existuje více CWE. Například pro obecnou Injection, Command Injection, Cross-site Scripting, hardcoded passwords, nedostatečnou validaci, buffer overflow, ukládání citlivých informací v čitelné podobě a mnoho dalších existuje více samostatných CWE. V závislosti na organizaci nebo testerovi mohou být používány různé CWE. Použitím kategorií obsahujících více CWE pomáháme zvyšovat základní úroveň povědomí o různých typech slabin, které se mohou vyskytovat pod jedním společným názvem kategorie. V tomto vydání OWASP Top Ten 2025 je v deseti kategoriích celkem 248 CWE. V době vydání tohoto dokumentu obsahoval [stáhnutelný slovník CWE od MITRE](https://cwe.mitre.org) celkem 968 CWE.


## Jak se data používají pro výběr kategorií

Podobně jako ve vydání z roku 2021 jsme využili data CVE pro hodnocení *zneužitelnosti (Exploitability)* a *(technického) dopadu (Impact)*. Stáhli jsme OWASP Dependency Check a extrahovali skóre CVSS pro zneužitelnost a dopad, která jsme seskupili podle příslušných CWE uvedených u CVE. Tento proces vyžadoval značné množství výzkumu a úsilí, protože všechny CVE obsahují skóre CVSSv2, avšak CVSSv2 má nedostatky, které má řešit CVSSv3. Od určitého okamžiku jsou všem CVE přiřazována také skóre CVSSv3. Kromě toho byly mezi CVSSv2 a CVSSv3 upraveny rozsahy skórování i výpočetní vzorce.

V CVSSv2 mohly hodnoty Exploit i (Technical) Impact dosahovat až 10,0, avšak vzorec je následně snižoval na 60 % pro zneužitelnost a 40 % pro dopad. V CVSSv3 je teoretické maximum omezeno na 6,0 pro zneužitelnost a 4,0 pro dopad. Po zohlednění vážení se hodnocení dopadu v CVSSv3 posunulo výše, v průměru téměř o jeden a půl bodu, zatímco zneužitelnost se v průměru posunula téměř o půl bodu níže.

V National Vulnerability Database (NVD) se nachází přibližně 175 000 záznamů CVE mapovaných na CWE (nárůst ze 125 000 v roce 2021), extrahovaných z OWASP Dependency Check. Dále je zde 643 jedinečných CWE mapovaných na CVE (nárůst z 241 v roce 2021). Z téměř 220 000 extrahovaných CVE mělo 160 000 skóre CVSS v2, 156 000 skóre CVSS v3 a 6 000 skóre CVSS v4. Mnoho CVE má více skóre, což vysvětluje, proč celkový součet přesahuje 220 000.

Pro Top Ten 2025 jsme průměrná skóre zneužitelnosti a dopadu vypočítali následujícím způsobem. Všechny CVE se skóre CVSS byly seskupeny podle CWE a jak skóre zneužitelnosti, tak skóre dopadu byla vážena podle procentuálního zastoupení populace s CVSSv3, stejně jako podle zbývající populace se CVSSv2, aby bylo dosaženo celkového průměru. Tyto průměry byly následně přiřazeny k CWE v datové sadě a použity jako skóre zneužitelnosti a (technického) dopadu pro druhou polovinu rovnice rizika.

Proč nebylo použito CVSS v4.0? Důvodem je, že skórovací algoritmus byl zásadně změněn a již neposkytuje skóre zneužitelnosti nebo dopadu tak přímo, jako je tomu u CVSSv2 a CVSSv3. V budoucích vydáních Top Ten se pokusíme nalézt způsob, jak skórování CVSS v4.0 využít, avšak pro vydání 2025 se nepodařilo nalézt časově proveditelné řešení.


## Proč používáme komunitní průzkum

Výsledky v datech jsou z velké části omezeny na to, co je možné v odvětví testovat automatizovaným způsobem. Zkušený specialista v oblasti AppSec vám řekne o věcech, které nachází, a o trendech, které pozoruje, ale které se v datech zatím neobjevují. Vývoj testovacích metodik pro určité typy zranitelností vyžaduje čas a další čas je potřeba k automatizaci těchto testů a jejich spuštění nad velkou populací aplikací. Vše, co v datech nacházíme, se vztahuje k minulosti a může opomíjet trendy z posledního roku, které v datech nejsou obsaženy.

Z tohoto důvodu vybíráme pouze osm z deseti kategorií na základě dat, protože data nejsou úplná. Zbývající dvě kategorie pocházejí z komunitního průzkumu Top 10. Ten umožňuje praktikům hlasovat pro rizika, která považují za nejvyšší, a která nemusí být v datech obsažena (a nemusejí se v nich objevit nikdy).


## Poděkování poskytovatelům dat

Následující organizace (spolu s několika anonymními přispěvateli) laskavě poskytly data pro více než 2,8 milionu aplikací, čímž umožnily vznik největšího a nejkomplexnějšího datového souboru v oblasti bezpečnosti aplikací. Bez vás by to nebylo možné.

* Accenture (Prague)
* Anonymous (multiple)
* Bugcrowd
* Contrast Security
* CryptoNet Labs
* Intuitor SoftTech Services
* Orca Security
* Probely
* Semgrep
* Sonar
* usd AG
* Veracode
* Wallarm

## Hlavní autoři
* Andrew van der Stock - X: [@vanderaj](https://x.com/vanderaj)
* Brian Glas - X: [@infosecdad](https://x.com/infosecdad)
* Neil Smithline - X: [@appsecneil](https://x.com/appsecneil)
* Tanya Janca - X: [@shehackspurple](https://x.com/shehackspurple)
* Torsten Gigler - Mastodon: [@torsten_gigler@infosec.exchange](https://infosec.exchange/@torsten_gigler)

## Hlášení chyb a pull requesty

Prosíme, zaznamenávejte veškeré opravy nebo problémy:

### Project links:
* [Domovská stránka](https://owasp.org/www-project-top-ten/)
* [GitHub repozitář](https://github.com/OWASP/Top10)
