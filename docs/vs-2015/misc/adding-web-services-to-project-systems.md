---
title: Přidání webové služby do systémů projektů | Dokumentace Microsoftu
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- project systems, adding Web services
- Web services, adding to VSPackage project systems
ms.assetid: 8efa078b-68b2-45a2-9be2-44f807bc0d7f
caps.latest.revision: 8
manager: douge
ms.openlocfilehash: 80de75b1b10a761e88b86c0982c0dc925c6eeeb4
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2018
ms.locfileid: "42669414"
---
# <a name="adding-web-services-to-project-systems"></a>Přidání webové služby do systémů projektů
Webové služby XML jsou obecně platí, adresa URL bajtově adresovatelného prostředky, které vracejí prostřednictvím kódu programu informace k systému projektů pomocí protokolu SOAP (Simple Object Access Protocol). Webové služby můžete integrovat do vašeho systému projektu VSPackage pomocí <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddProjectItemDlg2> rozhraní.  
  
### <a name="to-add-a-web-service-to-your-project-system"></a>Chcete-li přidat webovou službu v systému projektu  
  
1.  Volání `QueryService` pro <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddProjectItemDlg2> rozhraní prostřednictvím <xref:Microsoft.VisualStudio.Shell.Interop.SVsAddWebReferenceDlg> služby.  
  
2.  Volání <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2.AddWebReferenceDlg%2A> metody. Pokud předáte v `pDiscoverySession` parametr `NULL`, je pro vás vytvořením relace zjišťování a relace se ukládá do mezipaměti tak, aby byly k dispozici pro následné použití <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2> rozhraní. <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2.AddWebReferenceDlg%2A> metoda vrací ukazatel na <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult2>.  
  
3.  Volání <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult.AddWebReference%2A> metody. Předat objekt automatizace pro složku webových odkazů služby, jako `pUnkWebReferenceFolder` parametru. Prostředí sady Visual Studio pak ověří, zda webová služba již existuje. Pokud webová služba není k dispozici, prostředí se stáhne a přidá webovou službu do složky a další soubory (například soubory WSDL) do složky podřízené uzly.  
  
## <a name="see-also"></a>Viz také  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoverySession>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsDiscoveryService>