# Universal-Bootloader
Universeller <b>Bootloader</b> für <b>BIOS</b> und <b>EFI</b>-Systeme auf Basis des <a href="https://www.gnu.org/software/grub/">GRUB Bootloaders</a>.

Zur Erstellung eines boot-fähigen USB-Sticks, der sowohl auf <b>BIOS</b>-Systemen als auch auf <b>EFI</b>-Systemen gleichermaßen startet.

Die komprimierte Image-Datei <a href="https://github.com/migacode/universal-bootloader/blob/main/universal-bootloader.img.gz"><strong>universal-bootloader.img.gz</strong></a> mit einem geeigneten Programm wie <b>Balena-Etcher</b> oder dem <b>Gnome-Disk-Utility</b> einfach auf einen USB-Stick brennen. Je nach verwendetem Brenn-Pogramm muss die Datei "<i>universal-bootloader.img</i>" vor dem Brennen noch aus der mit gzip gepackten Datei (.gz) extrahiert werden.

Das Image enthält lediglich den Bootloader selbst, sowie ein Menü mit Beispiel-Einträgen, welches mit einem Text-Editor auf die eigenen Anforderungen angepasst werden kann.
Nach dem Brennen des Images auf den USB-Stick enthält dieser zwei Partitionen:
- BOOTLOADER (Partition 1) mit den GRUB-Bootloadern für <b>BIOS</b> und <b>EFI</b>-Systeme.
- GRUB-MENU (Partition 2) mit einer Datei namens grub.cfg, welche nur das anpassbare Menü enthält.
Das Menü wird für sowohl für <b>BIOS</b>- als auch <b>EFI</b>-System gleichermaßen verwendet - bei Bedarf kann der jedoch der Hintergrund für beide Varianten individuell eingestellt werden.

Weitere Partitionen auf dem Stick für die Installation von Betriebssystemen und Vorhaltung von ISO-Dateien müssen nach eigenen Wünschen eingerichtet werden.
