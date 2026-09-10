# shiro-grub

Tema de GRUB del escritorio Shiro. Forma parte de
[shiro-theme](https://github.com/eusp/shiro-theme): el fondo, `theme.txt` y las imágenes de
selección (`select_*.png`) los genera `builders/grub.js` con los colores del tema activo, así
que no conviene editarlos a mano.

Proyectos Shiro: [shiro-theme](https://github.com/eusp/shiro-theme) ·
[shiro-ags](https://github.com/eusp/shiro-ags) ·
[shiro-hyprland](https://github.com/eusp/shiro-hyprland) ·
[shiro-sddm](https://github.com/eusp/shiro-sddm) ·
**shiro-grub**

## Instalación

El repo vive en `~/.config/shiro-grub` (lo clona `install.sh` de shiro-theme). Para aplicarlo:

```bash
sudo node ~/.config/shiro-theme/build-grub.js
```

Eso regenera los archivos, copia el tema a `/boot/grub/themes/shiro-grub` (o `/boot/grub2/...`
en Fedora), apunta `GRUB_THEME` en `/etc/default/grub` y corre `grub-mkconfig`.

Solo sirve si el sistema arranca con GRUB. CachyOS instala Limine por defecto: hay que elegir
GRUB en el instalador (ver `CACHYOS.md` en shiro-theme). Sin GRUB, el builder se omite solo.

## Archivos

```
theme.txt                 Layout del menú (generado)
background.png            Fondo (copia del wallpaper del tema)
select_c/e/w.png          Resaltado del elemento seleccionado (generado)
icons/                    Iconos de las entradas del menú
terminus-14.pf2           Fuente de la terminal
unifont-16.pf2            Fuente del menú
```
