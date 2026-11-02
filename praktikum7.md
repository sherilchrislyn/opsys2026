# Praktikum 7

Ülesanne 7-1

Uus ketas on tavaliselt tühi ja sellel puudub partitsioonitabel, mistõttu operatsioonisüsteem ei tea, kuidas kettaruumi partitsioonideks jagada. Lähtestamisel valitakse partitsioonitabeli tüüp (GPT või MBR), mis kirjeldab partitsioonide asukohti ja suurusi. Seejärel saab ketta jagada partitsioonideks ja luua neile failisüsteemid (nt NTFS), et andmeid oleks võimalik tavapäraselt salvestada ja hallata. Partitsioonitabeli valik mõjutab ka ketta maksimaalset kasutatavat mahtu: MBR toetab 512-baidiste sektorite korral kuni ligikaudu 2 TiB suurust ketast, mistõttu on 4 TB ketta puhul sobivam valik GPT.

Ülesanne 7-2

1. Suurem ketta- ja partitsioonimaht. MBR kasutab 32-bitiseid sektoriaadresse, mis piirab 512-baidiste sektorite korral ketta mahu ligikaudu 2 TiB-ni. GPT kasutab 64-bitiseid aadresse ja võimaldab kasutada palju suuremaid kettaid.

2. Rohkem partitsioone. MBR toetab kuni nelja primaarset partitsiooni. Rohkemate partitsioonide loomiseks tuleb kasutada laiendatud partitsiooni, mille sees on loogilised kettad. GPT võimaldab Windowsis tavaliselt luua kuni 128 partitsiooni ilma sellise lisalahenduseta.
   
3. Varukoopia ja veakontroll. GPT hoiab partitsioonitabeli koopiat nii ketta alguses kui lõpus ja kontrollib neid kontrollsummaga (CRC32). Kui üks koopia läheb vigaseks, saab selle teisest taastada. MBR-i tabel on ainult ühes kohas ja ilma kontrollsummata, nii et rikkumist on raske märgata.

5. Unikaalsed GUID-id. GPT annab igale kettale ja partitsioonile oma unikaalse ID, mille järgi saab partitsiooni ära tunda ka siis, kui seadmete nimed muutuvad.

6.  UEFI tugi. Kaasaegne UEFI-püsivara käivitub GPT-kettalt loomulikult ja toetab Secure Boot’i. MBR on seotud vana BIOS-süsteemiga.

Ülesanne 7-3
https://kodu.ut.ee/~sherilchrislyn/opsys/hdd.png

Ülesanne 7-4
(Jätsin vahele, kuna SSH-ühendus adalbergiga andis veateate Permission denied (publickey) ka VPN-iga.)

Ülesanne 7-5

Käsuga -o ro haagitakse failisüsteem ainult lugemiseks, nii et faile saab vaadata ja kopeerida, aga mitte muuta ega kustutada. Käsuga -t auto tuvastab süsteem failisüsteemi tüübi ise, seda ei pea käsitsi ette andma.

Ülesanne 7-6

Mount käsu väljundis asendus auto väärtusega vfat. Mälupulka mul ei olnud, seega tegin katse pildifailiga usb.img. Sellepärast on väljundis allikaks /home/sheril/usb.img, mitte /dev/sdX1 nagu mälupulgal.

Ülesanne 7-7<img width="1710" height="1107" alt="Screenshot 2026-11-02 at 23 03 34" src="https://github.com/user-attachments/assets/95619da1-3623-40fc-a79f-7dbac9108e21" />


