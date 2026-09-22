# cardputer-terrarium-es
Un terrario de cristal sellado que vive en un M5Stack Cardputer ADV. Musgo, helechos, fittonias e hiedra crecen; colémbolos y cochinillas limpian; mosquitos de hongos y pulgones causan problemas; una araña saltarina y una mariquita los controlan. Funciona en tiempo real y los sensores de la placa lo ajustan suavemente.
<img width="960" height="540" alt="0ey3o6ryutqh1" src="https://github.com/user-attachments/assets/d02948af-baa4-4011-b323-d797e36a79f4" /><img width="960" height="540" alt="7nunf6ryutqh1" src="https://github.com/user-attachments/assets/1a436e09-bbb5-43aa-97a4-c264c683dcdb" />
<img width="960" height="540" alt="701vl9ryutqh1" src="https://github.com/user-attachments/assets/8c7e6eaa-e7e9-4043-a668-0b2370408d73" />
<img width="960" height="540" alt="se72e8ryutqh1" src="https://github.com/user-attachments/assets/3bf1f8e7-0ad1-4459-998f-40c7b58ddec0" /><img width="960" height="540" alt="oivzi8ryutqh1" src="https://github.com/user-attachments/assets/d2502008-c133-4e86-aa85-0d82c29f9a71" />

Lo que ves

Un terrario del tamano de una pecera visto por el cristal frontal: una barra de luz de cultivo arriba, grava de drenaje, una barrera de malla, una capa de carbon, tierra y hojarasca debajo, una rama de madera con musgo y una piedra. La luz sigue un ciclo dia/noche y todo se oscurece cuando esta apagada. Se forma condensacion en el cristal cuando hay humedad.

Plantas: musgo de almohadilla y de alfombra, helechos, fittonia (venas rosas y rojas), pilea, peperomia, lagrimas de bebe, selaginella e hiedra rastrera por el cristal.

Criaturas: colembolos, cochinillas (grises, naranjas y dalmata), mosquitos de los hongos y sus larvas, pulgones, una mariquita, una arana saltarina, moho y pequenas setas.

Paginas y teclas

Cada tecla es una pulsacion.

| **Tecla**       | **Accion**                                                              |
| --------------- | ----------------------------------------------------------------------- |
| `1` `2` `3` `4` | Tanque / Resumen / Diario / Senales                                     |
| `,` `/`         | Pagina anterior / siguiente                                             |
| `;` `.`         | Desplazar el Diario                                                     |
| `m`             | Rocio (sube humedad y humedad de la tierra)                             |
| `s`             | Plantar una semilla en el hueco mas debil                               |
| `p`             | Podar la planta mas alta                                                |
| `l`             | Encender la luz unas horas, incluso de noche                            |
| `r`             | Escanear el aire (WiFi + BLE) ahora                                     |
| `f`             | Velocidad: 1x → 60x → 600x → 3600x                                      |
| `[` `]`         | Ajustar reloj −/+ 1 hora (no hay RTC)                                   |
| `0` `0`         | Nuevo tanque (pulsa dos veces en 3 s)                                   |
| `h`             | Abrir / cerrar la ayuda del dispositivo (`,` `/` cambian sus 3 paginas) |

Resumen — salud general, barra, flecha de tendencia y grafica de 30 dias por especie.

Diario — los ultimos 32 eventos: floraciones, bajadas y recuperaciones, primeros mosquitos, periodos frios/calidos/secos, temblores, "tormentas de radio" y tus acciones.

Senales — datos de sensores en vivo, hash de entropia, memoria libre durante cada escaneo y version del firmware + commit de git en la ultima linea (terrarium v1.0.1 468d397; -dirty si se compilo con cambios sin guardar).

La pantalla se oscurece tras 30 s sin uso y se apaga despues de 3 min; el tanque sigue funcionando. La primera pulsacion despues de apagarse solo lo activa.
