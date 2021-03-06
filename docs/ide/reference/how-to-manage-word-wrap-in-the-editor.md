---
title: 'Postupy: Správa zalamování řádků v editoru'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- word wrap
- editors, text viewing
- Code Editor, word wrap
ms.assetid: 442f33ef-9f52-4515-b55f-fb816d664645
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8a1419a473bc0edc9fbc68ab978feb776ed63636
ms.sourcegitcommit: a6734c4d76dae3d21b55b10f3bc618dfa6b62dea
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2018
ms.locfileid: "42624144"
---
# <a name="how-to-manage-word-wrap-in-the-editor"></a>Postupy: Správa zalamování řádků v editoru

Můžete nastavit a zrušit **zalamování** možnost. Když nastavíte tuto možnost, zobrazí se na další řádek část dlouhý řádek, který přesahuje aktuální šířku okna editoru kódu. Pokud tato možnost vybrána, například pro usnadnění použití číslování řádků, můžete posouvat doprava a zobrazit konce dlouhé řádky.

## <a name="to-set-word-wrap-preferences"></a>Nastavení aplikace word wrap předvoleb

1.  Na **nástroje** nabídce vyberte možnost **možnosti**.

2.  V **textový Editor** složky, zvolte **Obecné** možnosti **všechny jazyky** podsložky globální nastavení této možnosti.

     – nebo –

     Zvolte **Obecné** možnosti v podsložce pro jazyk, ve kterém jsou programování.

3.  V části **nastavení**zaškrtněte nebo zrušte **zalamování** možnost.

     Když **zalamování řádků** je vybraná možnost, **brazit piktogramy pro zalamování řádků** je povolená možnost.

4.  Vyberte **brazit piktogramy pro zalamování** možnost, pokud chcete zobrazit indikátor vrátit šipku, kde dlouhý řádek zalamuje na další řádek. Pokud nechcete zobrazovat indikátor šipky, zrušte zaškrtnutí tohoto políčka.

    > [!NOTE]
    > Tyto šipky připomenutí nejsou přidány do kódu; jsou pouze pro účely zobrazení.

## <a name="known-issues"></a>Známé problémy

Pokud jste obeznámeni s zalamování řádků v poznámkovém bloku ++, Sublime Text nebo Visual Studio Code, mějte na paměti následující problémy, kde sady Visual Studio se chová jinak než ostatní editory:

* [Klikněte na tři nevybere celý řádek](https://developercommunity.visualstudio.com/content/problem/268989/triple-click-doesnt-select-whole-line-when-word-wr.html)
* [Příkazy Vyjmout nedojde k odstranění celý řádek](https://developercommunity.visualstudio.com/content/problem/138259/cut-command-should-delete-logical-line.html)
* [Klíč ukončení stiskněte dvakrát nepřesouvá kurzoru na konec řádku](https://developercommunity.visualstudio.com/content/problem/138274/pressing-end-key-twice-should-move-cursor-to-end-o.html)

## <a name="see-also"></a>Viz také:

- [Vlastní nastavení editoru](../../ide/customizing-the-editor.md)
- [Textový editor, dialogové okno Možnosti](../../ide/reference/text-editor-options-dialog-box.md)
- [Funkce editoru kódu](../../ide/writing-code-in-the-code-and-text-editor.md)
