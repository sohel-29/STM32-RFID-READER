# STM32-RFID-READER
STM32-based RFID reader using MFRC522 with SPI communication and UART serial output for UID detection.


# STM32 RFID Card Reader

A simple RFID card reader project using STM32 and MFRC522.

This project reads the UID of RFID cards through SPI and prints the card UID over UART. It is a basic embedded systems project useful for learning SPI communication, RFID interfacing, and UART debugging with STM32.

## Features

- MFRC522 RFID reader interfaced with STM32
- Reads RFID card UID
- Prints UID on serial terminal using UART
- Built with STM32CubeIDE and HAL drivers

## Hardware Used

- STM32 development board
- MFRC522 RFID module
- RFID cards / tags
- Jumper wires
- 3.3V power supply

## Communication Used

- SPI for communication between STM32 and MFRC522
- UART for printing card UID to serial monitor

## Working

When an RFID card is tapped near the MFRC522 reader, the STM32 reads the UID and sends it over UART.

Example output:

``text
Card UID: 69 EA 70 06
Card UID: 97 C1 EF 05
``

## How to Run

1. Open the project in STM32CubeIDE.
2. Make sure SPI and UART are configured correctly.
3. Build the project.
4. Flash the code to the STM32 board.
5. Open a serial terminal (Cool Term).
6. Tap an RFID card near the reader.
7. Check the UID printed in UART output.

## Notes

- MFRC522 should be powered with **3.3V**.
- Check SPI wiring carefully if the card is not detected.
- Some MFRC522 modules may show version `0xB2`, and they can still work normally for UID reading.

## Future Improvements

- Add LED indication for authorized card
- Add buzzer for unauthorized card
- Store authorized UIDs
- Build a door access system

## Author

Mohammed Sohel
