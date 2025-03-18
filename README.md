# Screen saver for Debain OS and running Xorg server with own images

## Environment preparation for Debain OS and running Xorg server

```bash
sudo apt-get update
```
```bash
sudo apt-get install xscreensaver xscreensaver-gl-extra xscreensaver-data-extra
```
**Create folder for images**
```bash
sudo mkdir -p /opt/screensaver
```
place to /opt/screensaver your images

**Set owner for folder /opt/screensaver for non root user**
```bash
sudo chown -R dietpi:dietpi /opt/screensaver
```


## Creating configuration
**This configuration is preset to display images in the /opt/screensaver folder 2 minutes after the last activity.**
```bash
nano /home/dietpi/.xscreensaver
```
```bash
timeout:	0:02:00 # Screen saver startup time after last activity ( Hours : minutes : seconds )
cycle:		0:10:00
lock:		False
lockTimeout:	0:00:00
passwdTimeout:	0:00:30
visualID:	default
installColormap:    True
verbose:	False
splash:		True
splashDuration:	0:00:05
demoCommand:	xscreensaver-settings
nice:		10
fade:		True
unfade:		True
fadeSeconds:	0:00:02
ignoreUninstalledPrograms:False
dpmsEnabled:	False
dpmsQuickOff:	False
dpmsStandby:	2:00:00
dpmsSuspend:	2:00:00
dpmsOff:	4:00:00
grabDesktopImages:  False
grabVideoFrames:    False
chooseRandomImages: True
imageDirectory:	/opt/screensaver/ # Directory with saved images

mode:		one
selected:	144

textMode:	url
textLiteral:	XScreenSaver
textFile:	
textProgram:	fortune
textURL:	https://planet.debian.org/rss20.xml
dialogTheme:	borderless
settingsGeom:	-439,35 315,52

programs:								      \
				maze --root				    \n\
  GL: 				superquadrics --root			    \n\
				attraction --root			    \n\
				blitspin --root				    \n\
				greynetic --root			    \n\
				helix --root				    \n\
				hopalong --root				    \n\
				imsmap --root				    \n\
-				noseguy --root				    \n\
-				pyro --root				    \n\
				qix --root				    \n\
-				rocks --root				    \n\
				rorschach --root			    \n\
				decayscreen --root			    \n\
				flame --root				    \n\
				halo --root				    \n\
				slidescreen --root			    \n\
				pedal --root				    \n\
				bouboule --root				    \n\
-				braid --root				    \n\
				coral --root				    \n\
				deco --root				    \n\
				drift --root				    \n\
-				fadeplot --root				    \n\
				galaxy --root				    \n\
				goop --root				    \n\
				grav --root				    \n\
				ifs --root				    \n\
				unicode --root				    \n\
  GL: 				jigsaw --root				    \n\
				julia --root				    \n\
-				kaleidescope --root			    \n\
  GL: 				moebius --root				    \n\
				moire --root				    \n\
  GL: 				morph3d --root				    \n\
				mountain --root				    \n\
				munch --root				    \n\
				penrose --root				    \n\
  GL: 				pipes --root				    \n\
				rdbomb --root				    \n\
  GL: 				rubik --root				    \n\
-				sierpinski --root			    \n\
				slip --root				    \n\
  GL: 				sproingies --root			    \n\
				starfish --root				    \n\
				strange --root				    \n\
				swirl --root				    \n\
				triangle --root				    \n\
				xjack --root				    \n\
				xlyap --root				    \n\
  GL: 				atlantis --root				    \n\
				bsod --root				    \n\
  GL: 				bubble3d --root				    \n\
  GL: 				cage --root				    \n\
-				crystal --root				    \n\
				cynosure --root				    \n\
				discrete --root				    \n\
				distort --root				    \n\
				epicycle --root				    \n\
				flow --root				    \n\
  GL: 				glplanet --root				    \n\
				interference --root			    \n\
				kumppa --root				    \n\
  GL: 				lament --root				    \n\
				moire2 --root				    \n\
  GL: 				sonar --root				    \n\
  GL: 				stairs --root				    \n\
				truchet --root				    \n\
-				vidwhacker --root			    \n\
-				webcollage --root			    \n\
				blaster --root				    \n\
				bumps --root				    \n\
				ccurve --root				    \n\
				compass --root				    \n\
				deluxe --root				    \n\
-				demon --root				    \n\
  GL: 				extrusion --root			    \n\
-				loop --root				    \n\
				penetrate --root			    \n\
				petri --root				    \n\
				phosphor --root				    \n\
  GL: 				pulsar --root				    \n\
				ripples --root				    \n\
				shadebobs --root			    \n\
  GL: 				sierpinski3d --root			    \n\
				spotlight --root			    \n\
				squiral --root				    \n\
				wander --root				    \n\
				xflame --root				    \n\
				xmatrix --root				    \n\
  GL: 				gflux --root				    \n\
-				nerverot --root				    \n\
				xrayswarm --root			    \n\
				xspirograph --root			    \n\
  GL: 				circuit --root				    \n\
  GL: 				dangerball --root			    \n\
- GL: 				dnalogo --root				    \n\
  GL: 				engine --root				    \n\
  GL: 				flipscreen3d --root			    \n\
  GL: 				gltext --root				    \n\
  GL: 				menger --root				    \n\
  GL: 				molecule --root				    \n\
				rotzoomer --root			    \n\
				scooter --root				    \n\
				speedmine --root			    \n\
  GL: 				starwars --root				    \n\
  GL: 				stonerview --root			    \n\
				vermiculate --root			    \n\
				whirlwindwarp --root			    \n\
				zoom --root				    \n\
				anemone --root				    \n\
				apollonian --root			    \n\
  GL: 				boxed --root				    \n\
  GL: 				cubenetic --root			    \n\
  GL: 				endgame --root				    \n\
				euler2d --root				    \n\
				fluidballs --root			    \n\
  GL: 				flurry --root				    \n\
- GL: 				glblur --root				    \n\
  GL: 				glsnake --root				    \n\
				halftone --root				    \n\
  GL: 				juggler3d --root			    \n\
  GL: 				lavalite --root				    \n\
-				polyominoes --root			    \n\
  GL: 				queens --root				    \n\
- GL: 				sballs --root				    \n\
  GL: 				spheremonics --root			    \n\
				twang --root				    \n\
- GL: 				antspotlight --root			    \n\
				apple2 --root				    \n\
  GL: 				atunnel --root				    \n\
				barcode --root				    \n\
  GL: 				blinkbox --root				    \n\
  GL: 				blocktube --root			    \n\
  GL: 				bouncingcow --root			    \n\
				cloudlife --root			    \n\
  GL: 				cubestorm --root			    \n\
				eruption --root				    \n\
  GL: 				flipflop --root				    \n\
  GL: 				flyingtoasters --root			    \n\
				fontglide --root			    \n\
  GL: 				gleidescope --root			    \n\
  GL: 				glknots --root				    \n\
  GL: 				glmatrix --root				    \n\
- GL: 				glslideshow --root --zoom 100 --fade 0	    \n\
  GL: 				hypertorus --root			    \n\
- GL: 				jigglypuff --root			    \n\
				metaballs --root			    \n\
  GL: 				mirrorblob --root			    \n\
				piecewise --root			    \n\
  GL: 				polytopes --root			    \n\
				pong --root				    \n\
				popsquares --root			    \n\
  GL: 				surfaces --root				    \n\
				xanalogtv --root			    \n\
				abstractile --root			    \n\
				anemotaxis --root			    \n\
- GL: 				antinspect --root			    \n\
				fireworkx --root			    \n\
				fuzzyflakes --root			    \n\
				interaggregate --root			    \n\
				intermomentary --root			    \n\
				memscroller --root			    \n\
  GL: 				noof --root				    \n\
				pacman --root				    \n\
  GL: 				pinion --root				    \n\
  GL: 				polyhedra --root			    \n\
- GL: 				providence --root			    \n\
				substrate --root			    \n\
				wormhole --root				    \n\
- GL: 				antmaze --root				    \n\
  GL: 				boing --root				    \n\
				boxfit --root				    \n\
  GL: 				carousel --root				    \n\
				celtic --root				    \n\
  GL: 				crackberg --root			    \n\
  GL: 				cube21 --root				    \n\
				fiberlamp --root			    \n\
  GL: 				fliptext --root				    \n\
  GL: 				glhanoi --root				    \n\
  GL: 				tangram --root				    \n\
  GL: 				timetunnel --root			    \n\
  GL: 				glschool --root				    \n\
  GL: 				topblock --root				    \n\
  GL: 				cubicgrid --root			    \n\
				cwaves --root				    \n\
  GL: 				gears --root				    \n\
  GL: 				glcells --root				    \n\
  GL: 				lockward --root				    \n\
				m6502 --root				    \n\
  GL: 				moebiusgears --root			    \n\
  GL: 				voronoi --root				    \n\
  GL: 				hypnowheel --root			    \n\
  GL: 				klein --root				    \n\
-				lcdscrub --root				    \n\
  GL: 				photopile --root			    \n\
  GL: 				skytentacles --root			    \n\
  GL: 				rubikblocks --root			    \n\
  GL: 				companioncube --root			    \n\
  GL: 				hilbert --root				    \n\
  GL: 				tronbit --root				    \n\
  GL: 				geodesic --root				    \n\
				hexadrop --root				    \n\
  GL: 				kaleidocycle --root			    \n\
  GL: 				quasicrystal --root			    \n\
  GL: 				unknownpleasures --root			    \n\
				binaryring --root			    \n\
  GL: 				cityflow --root				    \n\
  GL: 				geodesicgears --root			    \n\
  GL: 				projectiveplane --root			    \n\
  GL: 				romanboy --root				    \n\
				tessellimage --root			    \n\
  GL: 				winduprobot --root			    \n\
  GL: 				splitflap --root			    \n\
  GL: 				cubestack --root			    \n\
  GL: 				cubetwist --root			    \n\
  GL: 				discoball --root			    \n\
  GL: 				dymaxionmap --root			    \n\
  GL: 				energystream --root			    \n\
  GL: 				hexstrut --root				    \n\
  GL: 				hydrostat --root			    \n\
  GL: 				raverhoop --root			    \n\
  GL: 				splodesic --root			    \n\
  GL: 				unicrud --root				    \n\
  GL: 				esper --root				    \n\
  GL: 				vigilance --root			    \n\
  GL: 				crumbler --root				    \n\
				filmleader --root			    \n\
				glitchpeg --root			    \n\
  GL: 				handsy --root				    \n\
  GL: 				maze3d --root				    \n\
  GL: 				peepers --root				    \n\
  GL: 				razzledazzle --root			    \n\
				vfeedback --root			    \n\
  GL: 				deepstars --root			    \n\
  GL: 				gravitywell --root			    \n\
  GL: 				beats --root				    \n\
  GL: 				covid19 --root				    \n\
  GL: 				etruscanvenus --root			    \n\
  GL: 				gibson --root				    \n\
  GL: 				headroom --root				    \n\
  GL: 				sphereeversion --root			    \n\
				binaryhorizon --root			    \n\
				marbling --root				    \n\
  GL: 				chompytower --root			    \n\
  GL: 				hextrail --root				    \n\
  GL: 				mapscroller --root			    \n\
  GL: 				nakagin --root				    \n\
  GL: 				squirtorus --root			    \n\


pointerHysteresis:  10
authWarningSlack:   20
```



## Creating service
```bash
sudo nano /etc/systemd/system/xscreensaver.service
```
```bash
[Unit]
Description=XScreenSaver Service
After=graphical.target network-online.target
Requires=graphical.target

[Service]
User=dietpi # Do not run as ROOT!
Environment=DISPLAY=:0
ExecStart=/usr/bin/xscreensaver -nosplash
Restart=always
RestartSec=10
ExecStartPre=/bin/sleep 10

[Install]
WantedBy=graphical.target
```
```bash
sudo systemctl daemon-reexec
```
```bash
sudo systemctl enable xscreensaver.service
```

```bash
sudo systemctl start xscreensaver.service
```

check status:
```bash
sudo systemctl status xscreensaver.service
```
