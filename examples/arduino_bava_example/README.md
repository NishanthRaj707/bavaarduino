# BAVA Protocol Arduino IDE Example

This directory contains a complete, production-ready Arduino IDE sketch demonstrating how to integrate the zero-allocation **BAVA Protocol** on Arduino boards (UNO, Mega, Nano, ESP8266, ESP32 Arduino Core, STM32duino, Teensy).

---

## Key Features

1. **Hardware Serial Abstraction**: Connects BAVA's `bava_tx_cb_t` callback to `Serial.write()`.
2. **Byte-by-Byte RX Stream**: Reads non-blocking incoming bytes from `Serial.available()` / `Serial.read()` into `bava_process_byte()`.
3. **System Tick Timer**: Uses standard Arduino `millis()` for `bava_tick()`.
4. **Dictionary Variable Binding**: Registers `sys_telemetry` (`uint8_t`, ID `0x01`) and streams periodic updates every 50ms (20Hz).

---

## How to Run in Arduino IDE

1. Open **Arduino IDE**.
2. Open `arduino_bava_example.ino`.
3. Include the BAVA protocol header files (`bava.h`, `bava_tx.h`) and source files in your project or library folder.
4. Select your target Arduino board and port.
5. Click **Upload**.
