# Bspwm-elegant
BSPWM elegant. una manera elegante de gestionar tu bspwm

Este es una personalizacion propia para que ustedes puedan disfrutar de bspwm en la manera de que la he personalizado para ustedes

# Clona el repositorio
```
git clone https://github.com/fedohack1/bspwm-elegant.git
```

# Demo
Barra light mode

 ![alt text](https://raw.githubusercontent.com/fedohack1/bspwm-elegant/main/lightbar.png)

Barra dark mode
 ![alt text](https://raw.githubusercontent.com/fedohack1/bspwm-elegant/main/darkbar.png)
# Instalacion de recursos

Primero instalaremos lo necesario en el sistema operativo linux

 - Arch Linux --- usaremos el asistente de AUR yay
 ```
 yay -S polybar nitrogen sxhkd bspwm picom-git # no todo se es necesario instalar en yay puedes usar pacman menos en polybar y picom
 ```
 - Ubuntu
   
   Primero descarga las siguientes dependencias
  ```
  sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev        libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev 
  ```
  Luego clona el siguiente repositorio el cual tendra bspwm
  ```
  git clone https://github.com/baskerville/bspwm.git && cd bspwm && sudo make install
  ```
   Esto creara el paquete de bspwm para poder ejecutarlo
   creamos un directorio de configuracion y copiamos ciertos archivos
   ```
   mkdir -p ~/.config/bspwm
   cp bspwm-elegant/bspwmrc ~/.config/bspwmrc
   chmod +x ~/.config/bspwm/
   ```
   Despues instalaremos shxkd, primero clonamos en repositorio
   ```
   git clone https://github.com/baskerville/sxhkd.git
   ```
   Ahora lo compilaremos y crearemos los archivos correspondiente
   ```
   cd sxhkd
   make
   sudo make install
   mkdir ~/.config/shxkd
   cp -r bspwm-elegant/shxkdrc ~/.config/sxhkd/
   ```
   Puedes cambiar la terminal por defecto por que lleva solo alacritty
   
   Ahora iniciaremos con la instalacion de polybar descargando las dependenias correspondientes
   ```
   sudo apt install cmake cmake-data pkg-config python3-sphinx libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev
   ```
   Luego clonamos el reposiorio
   ```
    git clone --recursive https://github.com/polybar/polybar
   ```
   Instalamos y compilamos polybar y agregamos los archivos correspondientes
   ```
   cd polybar
   mkdir build
   cd build
   cmake ..
   make -j$(nproc)
   sudo make install
   mkdir ~/.config/polybar
   cp -r bspwm-elegant/config* ~/.config/polybar
   cp -r bspwm-elegant/launch.sh ~/.config/polybar
   chmod +x ~/.config/polybar/launch.sh
   ```
   Si quieres volver light o dark realiza el siguiente proceso, mientras creo un script que automatice todo
   ```
   cd ~/.config/polybar
   cp config-light config
   chmod +x config
   "Para el dark es viseversa"
   cp config-dark config
   ```
   # Primer boot
   Abriremos una terminal y escribiremos nitrogen
   Despues de esto elegirimos una de las rutas de imagenes
   puedes usar las imagenes que deje en el repositorio las cuales yo uso
   
   _Y a disfrutar_
   
   # Version 
   _ version 1.0_
   
   # Issues
   
  en caso de issues o errores dejarlo en comentarios
