# universal-bootloader
Universeller Boot-Loader für BIOS und EFI-Systeme auf Basis des <a href="https://www.gnu.org/software/grub/">GRUB Bootloaders</a>.

Zur Erstellung eines boot-fähigen USB-Sticks, der sowohl auf <b>BIOS</b>-Systemen als auch auf <b>EFI</b>-Systemen gleichermaßen startet.

Die komprimierte Image-Datei <a href="https://github.com/migacode/universal-bootloader/blob/main/universal-bootloader.img.gz"><strong>universal-bootloader.img.gz</strong></a> mit einem geeigneten Programm wie <b>Balena-Etcher</b> oder dem <b>Gnome-Disk-Utility</b> einfach auf einen USB-Stick brennen.

Das Image enthält lediglich den Bootloader selbst, sowie ein Menü mit Beispiel-Einträgen, welches mit einem Text-Editor auf die eigenen Anforderungen angepasst werden kann.
Das Menü wird sowohl nach dem Booten eines <b>BIOS</b>- als auch einem <b>EFI</b>-System gleichermaßen angezeigt.
Nach dem Brennen des Images auf den USB-Stick enthält dieser zwei Partitionen:
- BOOTLOADER (Partition 1) mit dem GRUB-Bootloader für <b>BIOS</b> und <b>EFI</b>-Systeme.
- GRUB-MENU (Partition 2) mit einer Datei namens grub.cfg, welche nur das anpassbare Menü enthält.
