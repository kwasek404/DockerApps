## Docker isolation for desktop
Run typical desktop apps in isolated container. Support for X11 and pulseaudio.
1. Build docker container (argv is directory name)
```bash
./build docker-firefox
```
2. Create start script and menu entry in gnome
```bash
./deploy docker-firefox
```
3. Start application from console or menu
```bash
docker-firefox
```
