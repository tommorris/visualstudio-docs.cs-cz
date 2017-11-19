---
title: "Jak ClickOnce provádí aktualizaci aplikací | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-deployment
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- updates, ClickOnce
- ClickOnce deployment, updates
- deploying applications [ClickOnce], application updates
ms.assetid: d54313c2-cf0c-420d-b151-99953a95f0bb
caps.latest.revision: "9"
author: stevehoag
ms.author: shoag
manager: wpickett
ms.openlocfilehash: 32e0b56ab5d4507c971948b98c8f7660650e70cc
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2017
---
# <a name="how-clickonce-performs-application-updates"></a>Jak ClickOnce provádí aktualizaci aplikací
ClickOnce používá informace o verzi souboru zadané v manifestu nasazení aplikace se rozhodnout, zda se má aktualizovat soubory aplikace. Po začátku aktualizace ClickOnce využívá techniku, nazývá *opravy souborů* předejdete redundantní stahování souborů aplikace.  
  
## <a name="file-patching"></a>Soubor opravy  
 Při aktualizaci aplikace, ClickOnce nestahuje všechny soubory pro novou verzi aplikace, pokud soubory se změnily. Místo toho porovná podpisy hodnoty hash soubory zadané v manifestu aplikace pro aktuální aplikaci proti podpisů v manifestu pro novou verzi. Pokud soubory podpisů liší, ClickOnce stáhne na novou verzi. Pokud se podpisů shodují, soubor nebyl změněn z jedné verze na další. V takovém případě ClickOnce zkopíruje existující soubor a používá je v nové verzi aplikace. Tento přístup zabraňuje ClickOnce stáhnout znovu, bude celá aplikace i v případě, že pouze jeden nebo dva soubory se změnily.  
  
 Soubor opravy funguje i pro sestavení, které jsou staženy na vyžádání pomocí <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroup%2A> a <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroupAsync%2A> metody.  
  
 Pokud používáte Visual Studio kompilace aplikace, vygeneruje vždy, když celý projekt znovu sestavte nový podpisy hodnoty hash pro všechny soubory. V takovém případě ve všech sestaveních bude stažen do klienta, i když pouze několik sestavení se mohl změnit.  
  
 Oprava souborů pro soubory, které jsou označeny jako data a uložené v adresáři data nefunguje. Tyto budou staženy vždy bez ohledu na podpis hodnoty hash souboru. Další informace o do adresáře dat najdete v tématu [přístup k místním a vzdáleným datům v aplikacích ClickOnce](../deployment/accessing-local-and-remote-data-in-clickonce-applications.md).  
  
## <a name="see-also"></a>Viz také  
 [Výběr strategie aktualizace ClickOnce](../deployment/choosing-a-clickonce-update-strategy.md)   
 [Výběr strategie nasazení ClickOnce](../deployment/choosing-a-clickonce-deployment-strategy.md)