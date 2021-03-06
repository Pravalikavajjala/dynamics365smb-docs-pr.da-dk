---
title: Administrere, slette eller komprimere dokumenter | Microsoft Docs
description: Beholde dine historiske data eller slette dem.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 10524be6bcfdc99672496b54903e4f04c33108ce
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="manage-documents"></a>Administrere dokumenter
En central rolle, f.eks. som programadministrator, skal regelmæssigt håndtere store mængder akkumulerede oversigtsdokumenter, der skal slettes eller komprimeres.  

## <a name="delete-documents"></a>Slet dokumenter
Du kan i visse situationer have behov for at slette fakturaer. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om de slettede købsordrer er fuldt faktureret. Du kan kun slette ordrer, hvis de er blevet fuldt faktureret og modtaget.  

Returvareordrer slettes normalt, når de er faktureret. Når en faktura bogføres, overføres den til vinduet **Bogført købskreditnota**. Hvis afkrydsningsfeltet **Returvarekvit. på kreditnota** er markeret i vinduet **Købsopsætning**, overføres fakturaen til vinduet **Bogført returvareleverance**. Du kan slette dokumenter ved hjælp af kørslen **Slet fakt. købsreturvareordrer**. Før du sletter, kontrollerer kørslen, om købsreturvareordreordrer er fuldt leveret og faktureret.  

Rammekøbsordrer slettes ikke, når du har behandlet og faktureret alle relaterede købsordrer. Du kan slette rammeordrer med kørslen **Slet fak. rammekøbsordrer**.  

Fakturerede serviceordrer slettes som regel automatisk, når de er faktureret fuldt ud. Når en faktura bogføres, oprettes der en tilsvarende post i vinduet **Bogførte servicefakturaer**. Det bogførte dokument kan ses i vinduet **Bogført servicefaktura**.  

Serviceordrer slettes ikke automatisk i programmet, men hvis det samlede antal i ordren er bogført, ikke fra selve serviceordren, men fra vinduet **Servicefaktura**. Det kan i så fald være nødvendigt at slette fakturerede ordrer, der ikke er slettet. Det kan du gøre ved at aktivere kørslen **Slet fakturerede serviceordrer**.  

## <a name="see-also"></a>Se også  
[Opsætning og administration til Dynamics 365 for Financials](admin-setup-and-administration.md)  

