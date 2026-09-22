# Terrarium for the Cardputer ADV ES

Un terrario de cristal sellado que vive en un [M5Stack Cardputer ADV](https://docs.m5stack.com/en/core/Cardputer-Adv). Crecen musgos, helechos, fittonias y hiedra rastrera; los colémbolos y las cochinillas se encargan de limpiar; los mosquitos del sustrato y los pulgones causan problemas; y una araña saltarina y una mariquita ayudan a mantenerlos bajo control. Funciona en tiempo real en el dispositivo, y los propios sensores de la placa influyen en el ecosistema de forma sutil.


<img width="960" height="540" alt="0ey3o6ryutqh1" src="https://github.com/user-attachments/assets/25566aca-42c7-4281-adc3-5744b67a0d4e" /><img width="960" height="540" alt="oivzi8ryutqh1" src="https://github.com/user-attachments/assets/a8a93ac6-67f6-4bd1-8fdc-1f705206fb44" />
<img width="960" height="540" alt="7nunf6ryutqh1" src="https://github.com/user-attachments/assets/d735252e-c0a7-436e-970f-7bac6c39bd01" />
<img width="960" height="540" alt="701vl9ryutqh1" src="https://github.com/user-attachments/assets/67e5eb16-1df0-4a5d-ba18-ef42bdd95de8" />
<img width="960" height="540" alt="se72e8ryutqh1" src="https://github.com/user-attachments/assets/e7be3126-7016-4ece-8651-82ab8fc86f48" />



## Instalacion (sin necesidad de herramientas)

Descargar desde el [latest release](../../releases/latest) :

| Ruta | Archivo | Mantiene tus otras aplicaciones? |
|---|---|---|
| **M5Launcher** (SD card) | `terrarium-adv-vX.Y.Z-app.bin` | Si |


**M5Launcher:** copia el archivo `…-app.bin` a la tarjeta SD, mete la tarjeta en el Cardputer, abre el explorador SD del Launcher e instalalo. La app ocupa unos 1,1 MB y cabe en el espacio para aplicaciones del Launcher.


> aplicaciones instaladas**. Usa la opcion de la tarjeta SD si quieres conservarlas.

La linea de comandos y la compilacion desde el codigo fuente estan mas abajo.

## Lo que ves

Un terrario del tamano de una pecera visto a traves del cristal frontal: una barra de luz de cultivo en la parte superior, grava de drenaje, una barrera de malla, una capa de carbon vegetal, tierra y hojarasca debajo, una rama de madera cubierta de musgo y una piedra. La luz de cultivo sigue un ciclo de dia y noche y todo el terrario se oscurece cuando esta apagada. Se forma condensacion en el cristal cuando el aire esta humedo.


**Plantas** (cada una de las 16 ranuras desarrolla su propia biomasa; todas son plantas normales de terrario cerrado): musgo de cojin y musgo tapizante, helechos button y lemon-button, fittonia (con nervaduras rosas y rojas), pilea, peperomia, lagrimas de bebe, selaginella y ficus rastrero trepando por el cristal.


**Criaturas** colémbolos, cochinillas (grises, naranjas y dalmata), mosquitos del sustrato y sus larvas, pulgones, una mariquita, una araña saltarina, ademas de moho y pequenas setas.

## Teclas y Acciones

Cada tecla se pulsa una sola vez.

| Teclas | Accion |
|---|---|
| `1` `2` `3` `4` | Terrario / Resumen / Diario / Senales |
| `,` `/` | Pagina anterior / siguiente |
| `;` `.` | Desplazar el diario |
| `m` | Rociar (sube la humedad y la humedad del suelo) |
| `s` | Planta una semilla en la ranura mas debil |
| `p` | Poda la planta mas alta |
| `l` | Luz de cultivo encendida durante unas horas, incluso por la noche |
| `r` | Escanear el aire (WiFi + BLE) ahora |
| `f` | Velocidad de simulacion: 1x → 60x → 600x → 3600x |
| `[` `]` | Ajustar el reloj −/+ 1 hora (no hay RTC) |
| `0` `0` |Nuevo terrario (pulsa dos veces en 3 s)|
| `h` | Abrir / cerrar la ayuda del dispositivo (, / cambian entre sus 3 paginas) |

* **Resumen** — salud general, seguida de una barra, una flecha de tendencia y una grafica de los ultimos 30 dias para cada especie.
* **Diario** — los ultimos 32 eventos: floraciones, descensos y recuperaciones, primeros mosquitos, frio/calor/sequedad, hechizos, temblores, "tormentas de radio" y lo que hiciste.
* **Señales** — todos los valores de los sensores en tiempo real, el hash de entropia, la memoria heap libre alrededor de cada escaneo y la version del firmware + commit de Git en la ultima linea (terrarium v1.0.1 468d397; -dirty si se ha compilado con cambios sin confirmar), para que puedas saber que version esta ejecutandose.

La pantalla baja el brillo despues de 30 s de inactividad y se apaga despues de 3 min; el terrario sigue funcionando. La primera pulsacion despues de apagarse solo sirve para despertarla.

## Como jugar

La ayuda del dispositivo (`h`) tiene el mismo texto, en letra pequena:

Un terrario sellado se cuida practicamente solo; tu solo tienes que intervenir de vez en cuando.

- **Observa** Terrario muestra las plantas, los insectos y el ciclo dia/noche. Resumen muestra quien esta prosperando: una barra, una flecha de tendencia y una grafica de 30 dias por especie, ademas de un % de salud general. Diario registra lo que ha ocurrido y cuando.
- **Rocia** (m) cuando el Diario indique que ha habido un periodo seco o las plantas parezcan marchitas. No lo inundes: la tierra mojada tarda en secarse.
- **Sembrar** (s) cuando las plantas se vean escasas.
- **Podar** (p) cuando haya demasiadas; los restos se convierten en materia organica que alimenta a las cochinillas y los colembolos.
- **Luz de cultivo** (l) ilumina el terrario durante unas horas, incluso por la noche. La luz incorporada ya sigue el ciclo dia/noche, asi que rara vez la necesitaras.
- **Plagas** (pulgones, mosquitos del sustrato) aumentan y disminuyen por si solas; la mariquita y la arana se encargan de mantenerlas bajo control. No hay nada que "ganar": ninguna especie puede desaparecer por completo.
- **Agitalo, hablale, camina a su alrededor** El IMU, el microfono y el trafico WiFi/Bluetooth a tu alrededor anaden pequenos cambios aleatorios. Palabras del Diario: Tremor = lo has agitado, Radio storm = el trafico WiFi/BLE ha aumentado, cold / warm / dry spell = clima poco habitual, boomed / crashed / recovering = una poblacion ha aumentado, disminuido o se esta recuperando.
- **f** acelera el tiempo (60x, 600x, 3600x) para que puedas ver pasar los dias.

## Como influyen los sensores

La aleatoriedad viene de todo lo que la placa puede medir: movimientos bruscos del IMU, nivel del microfono, bateria, temperatura del chip y del IMU, y el **numero, intensidad de senal y cambios de las redes WiFi y dispositivos Bluetooth cercanos.** Todo se reduce a unas pocas entradas normalizadas, junto con un hash de entropia de 32 bits que mezcla el generador aleatorio de la simulacion.

El terrario esta *sellado*, por lo que el efecto es deliberadamente debil y limitado: la condensacion regula la humedad, la temperatura varia unos pocos grados y los eventos poco frecuentes y limitados (ola de frio, periodo de calor, periodo de sequedad) afectan a una poblacion sin llegar a eliminarla.

| Entrada | Efecto |
|---|---|
| Agitar / inclinar (IMU) | la tierra se remueve; las cochinillas y los colembolos se alteran |
| Nivel de sonido | ligero parpadeo de luz, evaporacion mas rapida |
| Variacion de la temperatura del chip, bateria baja | variacion lenta de la temperatura |
| cambio en WiFi / BLE entre escaneos | pequenas variaciones de humedad, dispersion de esporas/semillas |
| Everything, hashed | seeds the RNG, so events differ run to run |

## The ecology

Plants are eaten by aphids and gnat larvae. Ladybugs eat aphids; a territorial jumping spider
eats gnats and the occasional springtail. Isopods, springtails and mold break down dead matter
and return nutrients to the soil, and springtails also graze the mold. Species have small refuge
floors (dormant eggs, spores, seeds) so a population can crash but not vanish.

Identifiers in `sim/terrarium.h` predate the tank redesign; the mapping is documented there
(e.g. `SP_CATERPILLAR` = gnat larvae, `SP_WORM` = isopods).

### Stability is tested, not eyeballed

`sim/` is portable C++ with no Arduino dependencies. The host harness builds the *same*
`sim/terrarium.cpp` the firmware uses and runs 200 seeds × 90 days at four input levels
(quiet, mild, strong, and a worst case that pins every sensor to its rail with the temperature
drift flipping sign), asserting that no species dies out and every jar variable stays in range.
It also checks that the fast-forward path lands near a step-by-step run.

```sh
make test      # ~2 s, prints per-species min/mean/max and PASS/FAIL
./harness -v 3 # one seed's population curve and journal
```

## Hardware notes

- ESP32-S3, no PSRAM. Free heap is ~225 KB after boot; a WiFi+BLE scan burst dips to ~157 KB
  and returns to ~204 KB, flat across repeated scans. The 240×135 sprite is 16-bit (65 KB).
- **No RTC** on the ADV, so the clock is software (starts near the build time; trim with `[` `]`).
  The sim therefore cannot catch up on time spent powered off; it resumes where it stopped.
- Scans run every 5 minutes as short sequential bursts (WiFi, then BLE), then the radio stack is
  torn down. WiFi uses the raw ESP-IDF `esp_wifi_scan_start` plus the scan-done event, because
  Arduino's async `scanNetworks()` failed intermittently on this board. Results must be freed
  with `WiFi.scanDelete()` or each scan leaks ~650 bytes.
- The keyboard's `isChange()` is a destructive latch, so it is polled on every loop, releases
  included.

## Prebuilt firmware

Each [release](../../releases) carries two images, both built from this source:

| File | Flash at | Use |
|---|---|---|
| `terrarium-adv-vX.Y.Z-factory.bin` | `0x0` | bootloader + partition table + app, one step; **replaces the whole layout** (including an M5Launcher install) |
| `terrarium-adv-vX.Y.Z-app.bin` | `0x10000` | app only, when this project's partition table is already on the board (keeps saved tank) |

```sh
# native USB: no download-mode button needed. --no-stub matters on this board.
esptool.py --chip esp32s3 --no-stub -p <your serial port> --before default_reset --after hard_reset \
  write_flash 0x0 terrarium-adv-v1.0.0-factory.bin
```

Check the download against `SHA256SUMS` first. The images contain no credentials or keys.
The web installer flashes the same `factory.bin` from the latest release.

## Build and flash

Requires [PlatformIO](https://platformio.org/). The serial port is auto-detected; set
`TERRARIUM_PORT=/dev/ttyACM0` (or your port) for `tools/flash.sh` and `tools/ser.py` to override it.

```sh
pio run                 # build
pio run -t upload       # FIRST flash: writes bootloader + partition table + app
tools/flash.sh          # afterwards: app-only write at 0x10000 (fast, keeps NVS)
```

> **Heads up:** the first upload replaces the partition table, which erases an M5Launcher
> layout and the apps installed in its slots. Back up what you need first.

The Cardputer's USB is native USB-Serial/JTAG, so esptool resets the chip itself — no
download-mode button. `tools/flash.sh` uses `--no-stub` because `pio run -t upload` proved
flaky here after the serial port had been used.

## Serial debug channel

Open the port with DTR asserted and RTS low (other combinations can drop the chip into download
mode) — `tools/ser.py` does this. It needs pyserial, which PlatformIO's Python already has:

```sh
~/.platformio/penv/bin/python tools/ser.py s        # status: jar, populations, sensors, heap
~/.platformio/penv/bin/python tools/ser.py k2       # inject keys (as if typed)
~/.platformio/penv/bin/python tools/ser.py --shot a.png   # screenshot the panel, 4x PNG
```

| Command | Effect |
|---|---|
| `h` | help |
| `s` | full status |
| `j` | dump the journal |
| `P` | dump the framebuffer (used by `--shot`) |
| `k<keys>` | inject key presses |
| `w` | scan now |
| `f` | cycle speed |
| `v` | save now |
| `x<days>` | fast-forward the sim (debug; not logged as an absence) |
| `z<seed>` | new tank with a seed |
| `T<HHMM>` | set the clock |
| `G<n>` | show page *n* (`kh` opens the help) |

The screenshots in this README were taken this way.

## Layout

```
sim/terrarium.{h,cpp}   portable simulation core (host-tested)
src/main.cpp            loop, keys, serial channel, save/restore, sim clock
src/signals.{h,cpp}     sensors, WiFi/BLE bursts, entropy
src/scene.cpp           the tank drawing
src/view.{h,cpp}        Summary / Journal / Signals / Help pages, HUD
src/help_text.h         every key and the how-to-play text (single source for the on-device help)
tools/harness.cpp       stability gate
tools/ser.py            serial helper + screenshots
tools/flash.sh          app-only flash
lib/M5Cardputer/        vendored M5Cardputer keyboard library (MIT, M5Stack)
```

## Privacy

The firmware never connects to any network and has no credentials, accounts or telemetry. Wi-Fi
and Bluetooth are used only for short *passive scans*; each nearby device's address and signal
strength is folded into a hash and a few counts in RAM. Addresses and names are not saved to
flash, printed, or sent anywhere. Only the tank state (populations, journal, clock trim) is saved.

## Persistence

The tank is saved to NVS every 10 minutes and on request (`v`). A version number guards the
format; on mismatch a new tank is started.

## License

MIT, see [LICENSE](LICENSE). The vendored `lib/M5Cardputer/` keeps its own MIT / SPDX headers
(M5Stack; the bundled `Adafruit_TCA8418` driver is Adafruit's, BSD).

## Credits

Keyboard support uses M5Stack's `M5Cardputer` library (MIT, vendored in `lib/`). Graphics and
hardware access use [M5Unified](https://github.com/m5stack/M5Unified) and
[M5GFX](https://github.com/m5stack/M5GFX); BLE scanning uses
[NimBLE-Arduino](https://github.com/h2zero/NimBLE-Arduino).
