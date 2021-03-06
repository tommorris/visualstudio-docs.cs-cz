---
title: Analýza kódu pro spravovaný kód v sadě Visual Studio
ms.date: 03/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.projectpropertypages.codeanalysis
helpviewer_keywords:
- code analysis, managed code
- managed code, code analysis
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: ad1b093c224e37ce53dc77472518d03f2dc8093b
ms.sourcegitcommit: 28909340cd0a0d7cb5e1fd29cbd37e726d832631
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2018
ms.locfileid: "44320810"
---
# <a name="overview-of-code-analysis-for-managed-code"></a>Přehled analýzy kódu pro spravovaný kód

Visual Studio 2017 analyzuje spravovaný kód dvěma způsoby: pomocí starší verze *FxCop* statické analýzy spravovaných sestavení a s .NET Compiler Platform *analyzátory*. Toto téma popisuje FxCop statickou analýzu kódu. Další informace o analýze kódu s použitím .NET Compiler Platform analyzátory, najdete v článku [analyzátory Roslyn přehled](../code-quality/roslyn-analyzers-overview.md).

Analýza kódu pro spravovaný kód analyzuje spravovaná sestavení a hlásí informace o sestaveních, jako jsou porušení programování a návrhu pravidel stanoví pokyny pro návrh rozhraní Microsoft .NET Framework.

Analytický nástroj představuje kontroly, které provádí během analýzy jako upozornění. Upozornění identifikují jakékoli relevantní problémy programování a návrhu a kdy je možné, poskytují informace o tom, jak tento problém vyřešit.

> [!NOTE]
> Analýza statického kódu není podporována pro projekty .NET Core a .NET Standard v sadě Visual Studio. Pokud spuštění analýzy kódu pro projekt .NET Core nebo .NET Standard v rámci nástroje msbuild zobrazí zpráva podobná **Chyba: CA0055: neidentifikoval platformu pro \<your.dll >**. Chcete-li provést analýzu kódu v projektech .NET Core nebo .NET Standard, použijte [analyzátory Roslyn](../code-quality/roslyn-analyzers-overview.md) místo.

## <a name="ide-integrated-development-environment-integration"></a>Integrace integrovaného vývojového prostředí (IDE)

Analýza kódu na svůj projekt můžete spustit ručně nebo automaticky.

Chcete-li spustit analýzu kódu při každém sestavení projektu, vyberte **povolit analýzu kódu na sestavení** na stránce vlastností projektu. Další informace najdete v tématu [postupy: povolení a zakázání automatické analýzy kódu](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md).

Chcete-li ruční spuštění analýzy kódu na projektu, na panelu nabídek zvolte **analyzovat** > **spustit analýzu kódu** > **spustit analýzu kódu na \<projektu >**.

## <a name="rule-sets"></a>Sady pravidel

Pravidla analýzy kódu pro spravovaný kód jsou seskupena do [sad pravidel](../code-quality/using-rule-sets-to-group-code-analysis-rules.md). Můžete použít jednu ze sad standardních pravidel společnosti Microsoft, nebo se dají [vytvoření vlastní sady pravidel](../code-quality/how-to-create-a-custom-rule-set.md) ke splnění specifickým požadavkům.

## <a name="suppress-warnings"></a>Potlačení upozornění

Často je užitečné označit, že varování není použitelné. To upozorní vývojáře a ostatní uživatele, kteří později, může zkontrolovat kód, že upozornění byla prozkoumat a potlačeno nebo ignorováno.

Je-source potlačení varování implementováno skrze vlastní atributy. Pro potlačení varování je zapotřebí, přidejte atribut `SuppressMessage` ke zdrojovému kódu, jak je znázorněno v následujícím příkladu:

```csharp
[System.Diagnosis.CodeAnalysis.SuppressMessage("Microsoft.Design", "CA1039:ListsAreStrongTyped")]
Public class MyClass
{
   // code
}
```

Další informace najdete v tématu [potlačit upozornění](../code-quality/in-source-suppression-overview.md).

> [!NOTE]
> Pokud provádíte migraci projekt do sady Visual Studio 2017, může vás prudce potýkají s velký počet upozornění analýzy kódu. Pokud nejste připravení upozornění, a chcete být tak produktivní okamžitě, můžete si *směrného plánu* analýzu stavu projektu. Z **analyzovat** nabídce vyberte možnost **spustit analýzu kódu a potlačit aktivních problémů**.

## <a name="run-code-analysis-as-part-of-check-in-policy"></a>Spustit analýzu kódu jako součást zásady vrácení se změnami

Jako organizace můžete vyžadovat, aby všechna vrácení se změnami splňovala určitá kritéria. Zejména budete chtít Ujistěte se, že jsou dodržovány tyto zásady:

- V kódu se změnami nejsou žádné chyby buildu.

- Spuštění analýzy kódu jako součást nejnovějšího sestavení.

Toho lze dosáhnout zadáním zásad vrácení se změnami. Další informace najdete v tématu [zlepšení kvality kódu pomocí zásady vracení se změnami projektu](../code-quality/enhancing-code-quality-with-team-project-check-in-policies.md).

## <a name="team-build-integration"></a>Integrace týmového sestavení

Chcete-li spustit nástroj pro analýzu jako součást procesu sestavení můžete použít integrované funkce systému sestavení. Další informace najdete v tématu [kanály Azure](/azure/devops/pipelines/index?view=vsts).

## <a name="see-also"></a>Viz také:

- [Přehled analyzátory Roslyn](../code-quality/roslyn-analyzers-overview.md)
- [Použití sad pravidel k seskupování pravidel analýzy kódu](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)
- [Postupy: Povolení a zakázání automatické analýzy kódu](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md)
