# ABAS – Accelerator Based Alarm System

ABAS är ett enkelt och energieffektivt larmsystem byggt med Adafruit Feather RP2040, en MSA311-accelerometer, tre knappar, tre LED-lampor och en piezo-buzzer. Systemet aktiveras och avaktiveras med en kod och använder accelerometern för att upptäcka rörelse.

## Funktioner
- Kodstyrd aktivering och avaktivering
- 30 sekunders fördröjning innan bevakningen startar
- Rörelsedetektering med accelerometer
- 15 sekunders tidsfönster för att avaktivera efter rörelse
- Full larmsignal (buzzer + blinkande LED)
- LED-lampor släcks automatiskt efter 30 sekunder för att spara energi
- Tillståndsmaskin för stabil och tydlig logik

## Hårdvara
- Adafruit Feather RP2040
- Adafruit MSA311 accelerometer
- 3 knappar (keypad)
- 3 LED (grön, gul, röd)
- Piezo-buzzer
- Kopplingskablar

## Kopplingar
- Accelerometern ansluts via I2C (SDA och SCL)
- LED ansluts till A0 (grön), A1 (gul), A2 (röd)
- Knappar ansluts till D10, D11 och D12
- Buzzer ansluts till D9 (PWM)
- Se projektets kopplingsschema för detaljer

## Installation
1. Installera CircuitPython på Adafruit Feather RP2040.
2. Kopiera MSA311-biblioteket till mappen `lib` på enheten.
3. Lägg `code.py` i rotmappen på enheten.

## Användning
### Aktivera larm
1. Mata in rätt kod.
2. Gul LED tänds.
3. Användaren har 30 sekunder på sig att lämna området.

### Avaktivera larm
1. Mata in rätt kod igen.
2. Grön LED tänds och larmet avaktiveras.

## Kodstruktur
code.py       - huvudprogram  
README.md     - dokumentation  
lib/          - nödvändiga bibliotek  

---

# English Version

## ABAS – Accelerator Based Alarm System

ABAS is a simple and energy-efficient alarm system built with the Adafruit Feather RP2040, an MSA311 accelerometer, three buttons, three LEDs and a piezo buzzer. The system is activated and deactivated using a short code and uses the accelerometer to detect movement.

## Features
- Code-controlled activation and deactivation
- 30-second delay before monitoring starts
- Motion detection using the accelerometer
- 15-second window to enter the code after movement
- Full alarm (buzzer + blinking LED)
- LEDs automatically turn off after 30 seconds to save energy
- State machine for stable and clear logic

## Hardware
- Adafruit Feather RP2040
- Adafruit MSA311 accelerometer
- 3 buttons
- 3 LEDs (green, yellow, red)
- Piezo buzzer
- Jumper wires

## Wiring
- Accelerometer connected via I2C (SDA and SCL)
- LEDs on A0 (green), A1 (yellow), A2 (red)
- Buttons on D10, D11 and D12
- Buzzer on D9 (PWM)
- See wiring diagram for full layout

## Installation
1. Install CircuitPython on the Feather RP2040.
2. Copy the MSA311 library to the `lib` folder.
3. Place `code.py` in the device root directory.

## Usage
### Activate alarm
1. Enter the correct code.
2. Yellow LED lights up.
3. You have 30 seconds to leave the monitored area.

### Deactivate alarm
1. Enter the code again.
2. Green LED lights up and the system is deactivated.

## File Structure
code.py       - main program  
README.md     - documentation  
lib/          - required libraries  

## License
MIT License (you may change this if needed)
