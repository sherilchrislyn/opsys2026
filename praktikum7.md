# Praktikum 7

Ülesanne 7-1

Uus ketas on tavaliselt tühi ja sellel puudub partitsioonitabel, mistõttu operatsioonisüsteem ei tea, kuidas kettaruumi partitsioonideks jagada. Lähtestamisel valitakse partitsioonitabeli tüüp (GPT või MBR), mis kirjeldab partitsioonide asukohti ja suurusi. Seejärel saab ketta jagada partitsioonideks ja luua neile failisüsteemid (nt NTFS), et andmeid oleks võimalik tavapäraselt salvestada ja hallata. Partitsioonitabeli valik mõjutab ka ketta maksimaalset kasutatavat mahtu: MBR toetab 512-baidiste sektorite korral kuni ligikaudu 2 TiB suurust ketast, mistõttu on 4 TB ketta puhul sobivam valik GPT.

Ülesanne 7-2

1. Suurem ketta- ja partitsioonimaht. MBR kasutab 32-bitiseid sektoriaadresse, mis piirab 512-baidiste sektorite korral ketta mahu ligikaudu 2 TiB-ni. GPT kasutab 64-bitiseid aadresse ja võimaldab kasutada palju suuremaid kettaid.

2. Rohkem partitsioone. MBR toetab kuni nelja primaarset partitsiooni. Rohkemate partitsioonide loomiseks tuleb kasutada laiendatud partitsiooni, mille sees on loogilised kettad. GPT võimaldab Windowsis tavaliselt luua kuni 128 partitsiooni ilma sellise lisalahenduseta.

3. Varukoopia ja veakontroll. GPT salvestab partitsioonitabeli päise ja kirjed nii ketta algusesse kui ka lõppu ning kaitseb neid CRC32 kontrollsummadega. Kui üks koopia riknebki, saab süsteem selle tuvastada ja taastada teisest koopiast. MBR-i partitsioonitabel on ainult ühes sektoris (esimeses) ning sellel pole kontrollsummat, nii et rikkumist on raske märgata ja tabel läheb kergesti kaduma.

4. Unikaalsed GUID-id. GPT määrab kettale ja igale partitsioonile unikaalse identifikaatori (GUID). See võimaldab partitsioone usaldusväärselt tuvastada ka siis, kui nende seadmenimed muutuvad. Linuxis saab partitsiooni tuvastamiseks kasutada näiteks PARTUUID-i. Partitsioonidele saab määrata ka nime, mis aitab neid eristada.

5.  UEFI tugi. Kaasaegne UEFI-püsivara käivitub GPT-kettalt loomulikult ja toetab Secure Boot’i. MBR on seotud vana BIOS-süsteemiga.

Ülesanne 7-3
https://kodu.ut.ee/~sherilchrislyn/opsys/hdd.png


