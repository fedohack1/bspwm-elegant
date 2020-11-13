# bspwm-elegant
BSPWM elegant. una manera elegante de gestionar tu bspwm

Este es una personalizacion propia para que ustedes puedan disfrutar de bspwm en la manera de que la he personalizado para ustedes

# Clona el repositorio
```
git clone https://github.com/fedohack1/bspwm-elegant
```

# Instalacion de polybar

Primero instalaremos lo necesario en el sistema operativo linux

 - Arch Linux --- usaremos el asistente de AUR yay
 ```
 yay -S polybar nitrogen sxhkd bspwm # no todo se es necesario instalar en yay puedes usar pacman menos en polybar
 ```
 - Ubuntu
   
   Primero descarga las siguientes dependencias
  ```
  sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev        libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev 
  ```
  luego clona el siguiente repositorio el cual tendra bspwm
  ```
  git clone https://github.com/baskerville/bspwm.git && cd bspwm && sudo make install
  ```
   esto creara el paquete de bspwm para poder ejecutarlo
   creamos un directorio de configuracion y copiamos ciertos archivos
   ```
   mkdir -p ~/.config/bspwm
   cp bspwm-elegant/bspwmrc ~/.config/bspwmrc
   chmod +x ~/.config/bspwm/bspwmrc
   ```
