---
title: "Upozornění zabezpečení | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.codeanalysis.securityrules
helpviewer_keywords:
- security [Visual Studio ALM], Enterprise Templates
- security warnings
- managed code analysis warnings, security warnings
- warnings, security
ms.assetid: 60d4e8ea-230a-494f-aa6a-b91db77540e4
caps.latest.revision: "28"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 54b7a3a62c5940419b946b85424fa745298bb89b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2017
---
# <a name="security-warnings"></a>Upozornění zabezpečení
Upozornění zabezpečení podporují bezpečnější knihovny a aplikace. Tato upozornění pomáhají zabránit chybám zabezpečení v programu. Pokud některá z těchto upozornění zakážete, měli byste v kódu jasně označit důvod a také informovat bezpečnostního úředníka vývoje projektu.  
  
## <a name="in-this-section"></a>V tomto oddílu  
  
|Pravidlo|Popis|  
|----------|-----------------|  
|[CA2100: Revize dotazů SQL pro chyby zabezpečení](../code-quality/ca2100-review-sql-queries-for-security-vulnerabilities.md)|Metoda nastavuje vlastnost System.Data.IDbCommand.CommandText pomocí řetězce, který je sestaven z řetězcového argumentu k metodě. Toto pravidlo předpokládá, že řetězcový argument obsahuje vstup uživatele. Řetězec příkazu SQL sestavený ze vstupu uživatele je ohrožen útoky prostřednictvím injektáže SQL.|  
|[CA2102: Zachycujte výjimky bez CLSCompliant v obecné obslužné rutiny](../code-quality/ca2102-catch-non-clscompliant-exceptions-in-general-handlers.md)|Člen v sestavení, které není označeno pomocí atributu RuntimeCompatibilityAttribute nebo je označeno atributem RuntimeCompatibility(WrapNonExceptionThrows = false), obsahuje zachytávací blok, který zpracovává typ System.Exception a neobsahuje bezprostředně následující obecný zachytávací blok.|  
|[CA2103: Revize naléhavého zabezpečení](../code-quality/ca2103-review-imperative-security.md)|Metoda používá imperativní zabezpečení a může vytvářet oprávnění pomocí informací o stavu nebo návratových hodnot, které se mohou změnit, pokud je žádost aktivní. Používejte deklarativní zabezpečení vždy, když je to možné.|  
|[CA2104: Nedeklaruje čtení pouze proměnlivé odkazové typy](../code-quality/ca2104-do-not-declare-read-only-mutable-reference-types.md)|Externě viditelný typ obsahuje externě viditelné pole měnitelného referenčního typu, které je určeno jen pro čtení. Měnitelný typ je typ, jehož instanční data lze upravit.|  
|[CA2105: Pole polí by neměly být jen pro čtení](../code-quality/ca2105-array-fields-should-not-be-read-only.md)|Když použijete – modifikátor jen pro čtení (jen pro čtení v jazyce Visual Basic) pro pole, která obsahuje pole, pole nelze změnit tak, aby odkazovaly jiné pole. Avšak prvky pole, které jsou uloženy v poli určeném jen pro čtení, mohou být změněny.|  
|[CA2106: Zabezpečte vyhodnotí](../code-quality/ca2106-secure-asserts.md)|Metoda uplatňuje oprávnění a na volajícím nejsou vykonány žádné kontroly zabezpečení. Uplatnění oprávnění zabezpečení bez provedení jakékoliv kontroly zabezpečení může zanechat ve vašem kódu zneužitelné slabé stránky zabezpečení.|  
|[CA2107: Zkontrolujte použití Odepřít a pouze povolit](../code-quality/ca2107-review-deny-and-permit-only-usage.md)|Metoda PermitOnly a akce zabezpečení CodeAccessPermission.Deny by měly být používány pouze těmi, kdo mají pokročilé znalosti o zabezpečení rozhraní .NET Framework. Kód používající tyto bezpečnostní akce by měl být podroben revizi zabezpečení.|  
|[CA2108: Revize deklarativních zabezpečení u typů hodnot](../code-quality/ca2108-review-declarative-security-on-value-types.md)|Veřejný nebo chráněný hodnotový typ je zabezpečen pomocí přístupu k datům nebo požadavků propojení.|  
|[CA2109: Revize viditelných obslužných rutin událostí](../code-quality/ca2109-review-visible-event-handlers.md)|Byla zjištěna veřejná nebo chráněná metoda zpracování událostí. Metody zpracování událostí by neměly být vystaveny, pokud to není nezbytně nutné.|  
|[CA2111: Ukazatelé by neměli být viditelné](../code-quality/ca2111-pointers-should-not-be-visible.md)|Ukazatel není soukromý, interní nebo jen pro čtení. Škodlivý kód může změnit hodnotu ukazatele, což potenciálně umožňuje přístup do libovolného umístění v paměti nebo může způsobit selhání aplikace nebo systému.|  
|[CA2112: Zabezpečené typy by neměly vystavovat pole](../code-quality/ca2112-secured-types-should-not-expose-fields.md)|Veřejný nebo chráněný typ obsahuje veřejná pole a je zabezpečen pomocí požadavků propojení. Pokud má kód přístup k instanci typu, která je zabezpečena pomocí požadavku na propojení, nemusí kód vyhovět požadavku na propojení pro přístup k polím tohoto typu.|  
|[CA2114: Zabezpečení metody by měla být nadmnožinou typu](../code-quality/ca2114-method-security-should-be-a-superset-of-type.md)|Metoda by neměla mít pro stejnou akci deklarativní zabezpečení jak na úrovni metody, tak na úrovni typu.|  
|[CA2115: Volejte GC. KeepAlive při použití nativních zdrojů](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)|Toto pravidlo zjistí chyby, které mohou nastat, protože nespravovaný prostředek je finalizován v době, kdy je stále používán nespravovaným kódem.|  
|[CA2116: Metody APTCA by měly volat pouze metody APTCA](../code-quality/ca2116-aptca-methods-should-only-call-aptca-methods.md)|Když je atribut APTCA (AllowPartiallyTrustedCallers) uveden pro plně důvěryhodná sestavení a sestavení spustí kód v jiném sestavení, které nepovoluje částečně důvěryhodné volající, může se jednat o chybu v zabezpečení.|  
|[CA2117: Typy APTCA by měl rozšířit pouze základní typy APTCA](../code-quality/ca2117-aptca-types-should-only-extend-aptca-base-types.md)|Když je atribut APTCA (AllowPartiallyTrustedCallers) uveden pro plně důvěryhodná sestavení a typ v sestavení je odvozen z typu, který nepovoluje částečně důvěryhodné volající, může se jednat o chybu v zabezpečení.|  
|[CA2118: Revize použití SuppressUnmanagedCodeSecurityAttribute](../code-quality/ca2118-review-suppressunmanagedcodesecurityattribute-usage.md)|Atribut SuppressUnmanagedCodeSecurityAttribute mění výchozí chování zabezpečení systému pro členy vykonávající nespravovaný kód, který používá zprostředkovatele komunikace s objekty COM nebo vyvolání platformy. Tento atribut slouží především ke zvýšení výkonu, ačkoliv nárůst výkonu může být spojen s významnými riziky zabezpečení.|  
|[CA2119: Zapečeťte metody, které vyhovují privátním rozhraním](../code-quality/ca2119-seal-methods-that-satisfy-private-interfaces.md)|Zděditelné veřejného typu poskytuje implementaci přepisovatelné metody pro vnitřní rozhraní (Friend v jazyce Visual Basic). Chcete-li opravit porušení tohoto pravidla, zabraňte přepsání metody mimo sestavení.|  
|[CA2120: Zabezpečte Serializační konstruktory](../code-quality/ca2120-secure-serialization-constructors.md)|Tento typ má konstruktor, který přebírá objekt System.Runtime.Serialization.SerializationInfo a objekt System.Runtime.Serialization.StreamingContext (podpis serializace konstruktoru). Tento konstruktor není zabezpečen pomocí kontroly zabezpečení, ale jeden nebo více běžných konstruktorů tohoto typu je zabezpečených.|  
|[CA2121: Statické konstruktory by měly být privátní](../code-quality/ca2121-static-constructors-should-be-private.md)|Systém volá statický konstruktor před vytvořením první instance typu nebo předtím, než jsou odkazovány jakékoli statické členy. Pokud statický konstruktor není soukromý, může být volán jiným kódem než kódem systému. V závislosti na operacích, které jsou provedeny v konstruktoru, to může způsobit neočekávané chování.|  
|[CA2122: Nezveřejňují nepřímo metody s požadavky propojení](../code-quality/ca2122-do-not-indirectly-expose-methods-with-link-demands.md)|Veřejný nebo chráněný člen má požadavky propojení a je volán členem, který neprovádí žádné bezpečnostní kontroly. Požadavek propojení kontroluje pouze oprávnění bezprostředního volajícího.|  
|[CA2123: Požadavky na přepsání odkazu musí být identické s bází](../code-quality/ca2123-override-link-demands-should-be-identical-to-base.md)|Toto pravidlo přiřazuje metodu své základní metodě, kterou je buď rozhraní, nebo virtuální metoda jiného typu, a poté v obou metodách srovnává požadavky propojení. Je-li toto pravidlo porušeno, může chybný volající obejít požadavek propojení pouhým voláním nezabezpečené metody.|  
|[CA2124: Zabalte ohroženou finally do vnějšího bloku try](../code-quality/ca2124-wrap-vulnerable-finally-clauses-in-outer-try.md)|Veřejná nebo chráněná metoda obsahuje blok try/finally. Blok finally nejspíše obnovuje stav zabezpečení a sám není uzavřen v bloku finally.|  
|[CA2126: Požadavky propojení typů vyžadují dědičnost požadavků](../code-quality/ca2126-type-link-demands-require-inheritance-demands.md)|Veřejný nezapečetěný typ je chráněn pomocí požadavku propojení a má přepisovatelnou metodu. Tento typ ani tato metoda nejsou chráněny pomocí vyžádané dědičnosti.|  
|[CA2136: Členy nesmějí mít konfliktní poznámky transparentnosti](../code-quality/ca2136-members-should-not-have-conflicting-transparency-annotations.md)|Ve 100% transparentním sestavení nemůže nastat kritický kód. Toto pravidlo analyzuje 100% transparentní sestavení pro jakékoliv anotace SecurityCritical na úrovni typu, pole nebo metody.|  
|[CA2147: Transparentní metody nemusejí podporovat použití zabezpečení vyhodnotí](../code-quality/ca2147-transparent-methods-may-not-use-security-asserts.md)|Toto pravidlo analyzuje všechny metody a typy v sestavení, které je buď 100% transparentní, nebo smíšené transparentní/kritické, a označí všechny deklarativní nebo imperativní použití výrazu Assert.|  
|[CA2140: Transparentní kód nesmí odkazovat na položky kritické pro zabezpečení](../code-quality/ca2140-transparent-code-must-not-reference-security-critical-items.md)|Metody označené pomocí atributu SecurityTransparentAttribute volají neveřejné členy, které jsou označené jako SecurityCritical. Toto pravidlo analyzuje všechny metody a typy v sestavení, které je transparentní/kritické, a označí všechna volání z transparentního kódu do neveřejného kritického kódu, která nejsou označena jako SecurityTreatAsSafe.|  
  
|[CA2130: Konstanty kritické pro zabezpečení musejí být transparentní](../code-quality/ca2130-security-critical-constants-should-be-transparent.md)|Pro konstantní hodnoty není vynucována transparentnost, protože kompilátory vkládají konstantní hodnoty do kódu, aby za běhu programu nebylo zapotřebí žádné vyhledávání. Konstantní pole by měla být transparentní z pohledu zabezpečení, aby kontroloři kódu nepředpokládali, že transparentní kód nemůže ke konstantě přistoupit.|  
|-----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|[CA2131: Typy kritické pro zabezpečení nemusejí podporovat účast na ekvivalenci typů](../code-quality/ca2131-security-critical-types-may-not-participate-in-type-equivalence.md)|Typ se účastní porovnávání typů, přičemž typ samotný nebo jeho člen nebo pole je označen atributem SecurityCriticalAttribute. Toto pravidlo je vyvoláno pro všechny kritické typy nebo typy obsahující kritické metody nebo pole, která se účastní porovnávání typů. Zjistí-li modul CLR takový typ, jeho načtení za běhu se nezdaří a je vyvolána výjimka TypeLoadException. Obvykle ke spuštění tohoto pravidla dochází pouze v případě, že uživatel implementuje porovnávání typů ručně a nepřenechává porovnávání typů na nástroji tlbimp a kompilátorech.|  
|[CA2132: Výchozí konstruktory nesmějí být kritické jako výchozí konstruktory základního typu](../code-quality/ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)|Typy a členy, které mají atribut SecurityCriticalAttribute, nelze použít kódem aplikace Silverlight. Typy a členy kritické z hlediska zabezpečení lze použít pouze prostřednictvím důvěryhodného kódu v knihovně tříd rozhraní .NET Framework aplikace Silverlight. Protože veřejné nebo chráněné konstrukce v odvozené třídě musí mít stejnou nebo větší transparentnost než jejich základní třída, nelze třídu v aplikaci odvodit z třídy označené jako SecurityCritical.|  
|[CA2133: Delegáti musí vytvořit vazbu k metodám s konzistentní transparentností](../code-quality/ca2133-delegates-must-bind-to-methods-with-consistent-transparency.md)|Toto upozornění je vyvoláno na metodě, která vytvoří vazbu delegáta označeného atributem SecurityCriticalAttribute na transparentní metodu nebo metodu označenou atributem SecuritySafeCriticalAttribute. Upozornění je také vyvoláno na metodě, která vytvoří vazbu transparentního delegáta nebo bezpečně kritického delegáta na kritickou metodu.|  
|[CA2134: Metody musí zachovávat konzistentní transparentnost, při přepisování základních metod](../code-quality/ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Toto pravidlo je vyvoláno, když metoda označená atributem SecurityCriticalAttribute přepíše transparentní metodu nebo metodu označenou atributem SecuritySafeCriticalAttribute. Toto pravidlo je vyvoláno, když transparentní metoda nebo metoda označená atributem SecuritySafeCriticalAttribute přepíše metodu označenou atributem SecurityCriticalAttribute. Pravidlo je použito při přepisování virtuální metody nebo implementaci rozhraní.|  
|[CA2135: Sestavení úrovně 2 nesmějí obsahovat LinkDemands](../code-quality/ca2135-level-2-assemblies-should-not-contain-linkdemands.md)|Pravidla LinkDemand jsou v sadě pravidel zabezpečení úrovně 2 již zastaralá. Namísto použití pravidel LinkDemand k vynucení zabezpečení v době kompilace JIT označte metody, typy a pole pomocí atributu SecurityCriticalAttribute.|  
|[CA2136: Členy nesmějí mít konfliktní poznámky transparentnosti](../code-quality/ca2136-members-should-not-have-conflicting-transparency-annotations.md)|Atributy transparentnosti jsou použity z prvků kódu většího rozsahu na prvky menšího rozsahu. Atributy transparentnosti prvků kódu, které mají větší rozsah, mají přednost před atributy transparentnosti prvků kódu, které jsou obsaženy v prvním prvku. Například třída označená atributem SecurityCriticalAttribute nemůže obsahovat metodu, která je označena atributem SecuritySafeCriticalAttribute.|  
|[CA2137: Transparentní metody musejí obsahovat pouze ověřitelné IL](../code-quality/ca2137-transparent-methods-must-contain-only-verifiable-il.md)|Metoda obsahuje kód, který nelze ověřit, nebo vrací typ odkazem. Toto pravidlo je vyvoláno při pokusech transparentního kódu zabezpečení spustit jazyk MSIL (Microsoft Intermediate Language), který nelze ověřit. Pravidlo však neobsahuje úplný ověřovatel jazyka IL a místo toho k zachycení většiny porušení ověření jazyka MSIL používá heuristiky.|  
|[CA2138: Transparentní metody nesmějí volat metody s atributem suppressunmanagedcodesecurity](../code-quality/ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)|Transparentní metoda zabezpečení volá metodu, která je označena atributem SuppressUnmanagedCodeSecurityAttribute.|  
|[CA2139: Transparentní metody nemusejí podporovat použití atributu HandleProcessCorruptingExceptions](../code-quality/ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute.md)|Toto pravidlo je vyvoláno, je-li jakákoliv metoda transparentní a pokusí se zpracovat výjimku poškozující proces použitím atributu HandleProcessCorruptedStateExceptionsAttribute. Výjimka poškozující proces je klasifikace výjimek dle specifikace CLR verze 4.0, jako například výjimka AccessViolationException. Atribut HandleProcessCorruptedStateExceptionsAttribute lze použít pouze metodami kritickými pro bezpečnost a bude ignorován, je-li použit u transparentních metod.|  
|[CA2140: Transparentní kód nesmí odkazovat na položky kritické pro zabezpečení](../code-quality/ca2140-transparent-code-must-not-reference-security-critical-items.md)|Prvek kódu označený atributem SecurityCriticalAttribute je kritický pro zabezpečení. Transparentní metoda nemůže použít prvek kritický pro zabezpečení. Pokud se transparentní typ pokusí použít typ kritický pro zabezpečení, je vyvolána výjimka TypeAccessException, MethodAccessException nebo FieldAccessException.|  
|[CA2141: transparentní metody nesmějí vyhovovat LinkDemands](../code-quality/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Transparentní metoda (z hlediska zabezpečení) volá metodu v sestavení, které není označeno atributem AllowPartiallyTrustedCallersAttribute (APTCA), nebo transparentní metoda (z hlediska zabezpečení) splňuje pravidlo LinkDemand pro typ nebo metodu.|  
|[CA2142: Transparentní kód nemůže být chráněn pomocí LinkDemands](../code-quality/ca2142-transparent-code-should-not-be-protected-with-linkdemands.md)|Toto pravidlo je vyvoláno na transparentních metodách, které vyžadují pro přístup k nim pravidla LinkDemand. Kód transparentní z hlediska zabezpečení by neměl být odpovědný za ověření zabezpečení operace, a proto by neměl požadovat oprávnění.|  
|[CA2143: Transparentní metody nemohou používat požadavky zabezpečení](../code-quality/ca2143-transparent-methods-should-not-use-security-demands.md)|Kód transparentní z hlediska zabezpečení by neměl být odpovědný za ověření zabezpečení operace, a proto by neměl požadovat oprávnění. Kód transparentní z hlediska zabezpečení by měl k učinění rozhodnutí o zabezpečení používat úplné požadavky a bezpečně kritický kód by neměl spoléhat na to, že transparentní kód tyto úplné požadavky provede.|  
|[CA2144: Transparentní kód nesmí načítat sestavení z bajtových polí](../code-quality/ca2144-transparent-code-should-not-load-assemblies-from-byte-arrays.md)|Přezkoumání zabezpečení transparentního kódu není tak důsledné jako přezkoumání zabezpečení kritického kódu, protože transparentní kód nemůže provádět akce citlivé na zabezpečení. Sestavení, která jsou načtena z pole bajtů, nemusí být v transparentním kódu zaznamenána a takové pole bajtů může obsahovat kritický nebo důležitější bezpečně kritický kód, který musí být auditován.|  
|[CA2145: Transparentní metody nesmějí být doplněny pomocí SuppressUnmanagedCodeSecurityAttribute](../code-quality/ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute.md)|Metody označené atributem SuppressUnmanagedCodeSecurityAttribute mají implicitní pravidlo LinkDemand umístěné na jakoukoli metodu, která je volá. Tento LinkDemand vyžaduje, aby byl volající kód kritický z hlediska zabezpečení. Označení metody, která používá SuppressUnmanagedCodeSecurity, atributem SecurityCriticalAttribute zviditelňuje tento požadavek pro volající metody.|  
|[CA2146: Typy musí být alespoň tak kritické, jako jejich základní typy a rozhraní](../code-quality/ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Toto pravidlo je vyvoláno, když má odvozený typ atribut transparentnosti zabezpečení, který není tak kritický jako jeho základní typ nebo implementované rozhraní. Pouze kritické typy lze odvodit z kritických základních typů nebo mohou implementovat kritická rozhraní a pouze kritické typy nebo bezpečně kritické typy mohou být odvozeny ze základních bezpečně kritických typů nebo mohou implementovat bezpečně kritická rozhraní.|  
|[CA2147: Transparentní metody nemusejí podporovat použití zabezpečení vyhodnotí](../code-quality/ca2147-transparent-methods-may-not-use-security-asserts.md)|U kódu označeného atributem SecurityTransparentAttribute není uděleno dostatečné oprávnění k vyhodnocení.|  
|[CA2149: Transparentní metody nesmějí provádět volání do nativního kódu](../code-quality/ca2149-transparent-methods-must-not-call-into-native-code.md)|Toto pravidlo je vyvoláno na jakékoli transparentní metodě, která přímo volá nativní kód, například prostřednictvím P/Invoke. Porušení tohoto pravidla vede k vyvolání výjimky MethodAccessException v modelu transparentnosti úrovně 2 a k úplnému požadavku na nespravovaný kód v modelu transparentnosti úrovně 1.|  
|[CA2151: Pole s kritickými typy by měla být kritické pro zabezpečení](../code-quality/ca2151-fields-with-critical-types-should-be-security-critical.md)|Chcete-li používat typy kritické z hlediska zabezpečení, musí být kód, který odkazuje na typ, buď kritický z hlediska zabezpečení, nebo bezpečně kritický z hlediska zabezpečení. To platí i v případě, že je odkaz nepřímý. Proto je existence transparentního pole kritického z hlediska zabezpečení nebo transparentního pole bezpečně kritického z hlediska zabezpečení zavádějící, jelikož transparentní kód nebude mít k poli přístup.|  
|[CA5122 P/Invoke deklarace nesmí být kritické](../code-quality/ca5122-p-invoke-declarations-should-not-be-safe-critical.md)|Metody jsou při provádění operace citlivé na zabezpečení označeny jako SecuritySafeCritical, ale lze je také bezpečně použít transparentním kódem. Transparentní kód nesmí nikdy přímo volat nativní kód prostřednictvím P/Invoke. Proto označení P/Invoke jako bezpečně kritické z hlediska zabezpečení neumožní transparentnímu kódu vyvolat je a je zavádějící pro analýzu zabezpečení.|  
|[CA2153: Vyhněte se zpracování poškozená stavu výjimek](../code-quality/ca2153-avoid-handling-corrupted-state-exceptions.md)|[Poškozený stav výjimky (rozšíření na straně klienta)](https://msdn.microsoft.com/en-us/magazine/dd419661.aspx) znamenat, že paměť poškození existuje v procesu. Zachytávání tyto než umožní procesu havárií může vést k ohrožení zabezpečení, pokud útočník můžete umístit zneužití do oblasti poškozená paměti.|  
|[CA3075: Zpracování nezabezpečené DTD](../code-quality/ca3075-insecure-dtd-processing.md)|Pokud používáte nezabezpečené DTDProcessing instance nebo odkazovat na externí entity zdroje, analyzátor může přijmout nedůvěryhodné vstup a prozrazeny citlivé informace útočníci.|  
|[CA3076: Spuštění skriptu nezabezpečené XSLT](../code-quality/ca3076-insecure-xslt-script-execution.md)|Pokud spustíte předlohy se styly transformace XSLT (Extensible Language) v aplikacích .NET nezabezpečeným, procesor může vyřešit nedůvěryhodné odkazy na identifikátor URI, které by mohly prozrazeny citlivé informace útočníci, což Denial of Service a webů útoky.|  
|[CA3077: Nezabezpečené zpracování v návrhu rozhraní API, dokumentu XML a čtečku textu XML](../code-quality/ca3077-insecure-processing-in-api-design-xml-document-and-xml-text-reader.md)|Při navrhování rozhraní API odvozená od třídou XMLDocument nastavenou na a XMLTextReader, mělo pamatovat DtdProcessing.  Pomocí nezabezpečené instancí DTDProcessing při odkazování na externí entity zdroje řešení nebo nastavení nezabezpečené hodnot v souboru XML může způsobit zpřístupnění informací.|