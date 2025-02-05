# universal-bootloader
Universeller Boot-Loader für BIOS und EFI-Systeme auf Basis des <a href="https://www.gnu.org/software/grub/">GRUB Bootloaders</a>.

Zur Erstellung eines boot-fähigen USB-Sticks, der sowohl auf BIOS-Systemen als auch auf EFI-Systemen gleichermaßen startet.

Die Image-Datei <b>universal-bootloader.img.gz</b> mit einem geeigneten Programm wie balena-etcher oder einfach auf einen USB-Stick brennen.
Der USB-Stick muss dazu mindesten 64 MB groß sein. 

Das Image enthält lediglich den Boot-Loader selbst sowie ein Menu mit Beispiel-Einträgen, welches auf die eigenen Anforderungen angepasst werden muss.
Nach dem Brennen des IMages auf den USB-Stick enthält dieser zwei Partitionen:
- BOOTLOADER (Partition 1) mit dem GRUB-Bootloader für BIOS <u>und</u> EFI-Systeme.
- GRUB-MENU (Partition 2) mit einer Datei namens grub.cfg, welche nur das anpassbare Menü enthält.
Das Menü wird sowohl nach dem Booten eines BIOS- als auch einem EFI-System gleichermaßen angezeigt.

<b>Download</b> Universal-Bootloader&nbsp;&raquo;&nbsp;<a href="https://github.com/migacode/home-assistant/blob/main/universal-bootloader/universal-bootloader.img.gz"><strong>universal-bootloader.img.gz</strong></a><br />
