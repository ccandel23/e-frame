# E-Frame — Estado del proyecto

**Última actualización:** 23 de octubre de 2026

## 1. Objetivo

Construir un marco fotográfico digital con pantalla e-paper a color, controlado por un ESP32.

Las fotografías se transferirán desde un teléfono Android mediante Bluetooth, sin utilizar Wi-Fi.

**Meta:** prototipo funcional antes de finalizar 2026, si es técnicamente viable.

## 2. Componentes

| Componente | Estado |
|---|---|
| Good Display GDEP073E01 (7.3", color) | Recibido |
| Good Display DESPI-C73 HAT | Recibido |
| ESP32-WROOM-32D HW-394 | Dañado; no utilizar |
| ESP32-S3 con 8 MB Flash y 8 MB PSRAM | En evaluación |

## 3. Diagnóstico del ESP32 original

Mediciones realizadas:

- VIN–GND: aproximadamente 4.5 V.
- 3V3–GND: 0 V.
- Resistencia entre 3V3 y GND: inferior a 1 Ω.
- Calentamiento cerca del conector USB-C.

Conclusión: placa dañada, probablemente con un cortocircuito en la línea de 3.3 V.

**Decisión:** reemplazar la placa.

## 4. Decisiones técnicas

- Framework principal: ESP-IDF.
- Lenguaje de programación: C.
- Entorno: Pop!_OS, terminal y Vim.
- Comunicación inalámbrica: Bluetooth.
- Wi-Fi: no se utilizará.
- Se evaluará el uso de almacenamiento microSD.

## 5. Etapa actual

Selección del microcontrolador de reemplazo.

Criterios:

- Compatibilidad eléctrica con el HAT.
- Memoria suficiente para procesar fotografías.
- Soporte Bluetooth adecuado.
- Compatibilidad con ESP-IDF.
- Coste y disponibilidad.

## 6. Próximos pasos

- [ ] Seleccionar y adquirir el ESP32 de reemplazo.
- [ ] Verificar especificaciones y pinout de la nueva placa.
- [ ] Estudiar las conexiones del HAT DESPI-C73.
- [ ] Diseñar y verificar el esquema de conexiones.
- [ ] Realizar una primera prueba de comunicación SPI.
- [ ] Probar la actualización de la pantalla.
- [ ] Diseñar la transferencia de imágenes mediante Bluetooth.

## 7. Registro de pruebas

Pendiente de iniciar con el nuevo microcontrolador.

## 8. Preguntas técnicas pendientes

- ¿Cuánta memoria necesitamos para procesar una fotografía?
- ¿Conviene utilizar PSRAM para el framebuffer?
- ¿Necesitaremos almacenamiento microSD?
- ¿Qué protocolo de transferencia mediante Bluetooth será más adecuado?
- ¿Cómo adaptaremos las fotografías al formato de la pantalla?