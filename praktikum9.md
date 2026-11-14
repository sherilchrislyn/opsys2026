## Praktikum 9

Ülesanne 9-1: 
/home/sheril

Ülesanne 9-2:
![Ülesanne 9-2](./Screenshot.png)

Ülesanne 9-3:
Eemaldasin Ubuntu virtuaalmasinast CUPS-i, sest see on mõeldud printerite ja printimistööde haldamiseks, kuld ma ei kasuta virtuaalmasinas printimist. Seega ei ole tarkvara mulle vajalik ning selle eemaldamisega sain vabastada 1577 kb kettaruumi.

![Ülesanne 9-3](Screenshot%202026-11-14%20at%2018.08.19.png)

Ülesanne 9-4:


![Ülesanne 9-4](Screenshot%202026-11-14%20at%2018.23.23.png)

Ülesanne 9-5:
Kui sama EXE-fail asub nii kasutaja kui ka süsteemi Path keskkonnamuutujas, käivitatakse see fail, mille kaust asub otsingujärjekorras eespool. Tavaliselt on selleks süsteemi Path kaustas olev fail.

Ülesanne 9-6:
Valisin teenuse Smart Card Device Enumeration Service, mis tegeleb kiipkaardilugejate tuvastamise ja haldamisega. Kuna ma ei kasuta oma Windowsi virtuaalmasinas kiipkaardilugejat, ei ole see teenus mulle vajalik ning selle võib  määrata olekusse disabled.

Ülesanne 9-7:

PS C:\Users\Sheril Chrislyn> Get-AppxPackage -Name "Microsoft.Todos" | select packageFullName

PackageFullName

---------------
Microsoft.Todos_0.179.8901.0_arm64__8wekyb3d8bbwe

PS C:\Users\Sheril Chrislyn> Get-AppxPackage -Name "Microsoft.Todos" | Remove-AppxPackage

PS C:\Users\Sheril Chrislyn> Get-AppxPackage -Name "Microsoft.Todos" | select packageFullName

Ülesanne 9-8:



