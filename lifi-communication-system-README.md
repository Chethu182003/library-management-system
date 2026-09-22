# 💡 Li-Fi Communication System

A hardware-software project that demonstrates **Light Fidelity (Li-Fi)** — transmitting data wirelessly using visible light instead of radio waves. Built as a proof-of-concept system using LEDs and photodetectors, programmed in C/C++.

---

## 🔬 What is Li-Fi?

Li-Fi is a wireless communication technology that uses **modulated light signals** (typically from LEDs) to transmit data at high speed. Unlike Wi-Fi which uses radio frequency (RF), Li-Fi offers:

- **Higher bandwidth** — light spectrum is 10,000× wider than the RF spectrum
- **No RF interference** — safe for use in hospitals, aircraft, and sensitive environments
- **Improved security** — light cannot pass through walls

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Microcontroller | Arduino / Embedded C/C++ |
| Transmitter | LED with modulation circuit |
| Receiver | Photodetector / LDR / Photodiode |
| Programming Language | C / C++ |
| Signal Processing | PWM-based modulation |

---

## ✨ Features

- **Data Transmission via Light** — Text/binary data encoded into light pulses
- **LED Modulation** — PWM-based ON/OFF keying for signal encoding
- **Real-time Reception** — Photodetector decodes light signals back to data
- **Serial Monitor Output** — Decoded data displayed via UART/Serial
- **Low-cost Hardware** — Built with widely available components

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────┐
│                  TRANSMITTER SIDE                   │
│  Input Data → Encoder → LED Driver → LED Emission  │
└────────────────────────┬────────────────────────────┘
                         │ (Light Signal)
                         ▼
┌─────────────────────────────────────────────────────┐
│                   RECEIVER SIDE                     │
│  Photodetector → Amplifier → Decoder → Output Data │
└─────────────────────────────────────────────────────┘
```

---

## 📂 Project Structure

```
lifi-communication-system/
├── transmitter/
│   ├── transmitter.ino     # Arduino sketch for TX side
│   └── encoder.h           # Data encoding logic
├── receiver/
│   ├── receiver.ino        # Arduino sketch for RX side
│   └── decoder.h           # Signal decoding logic
├── circuit/
│   ├── transmitter_circuit.png
│   └── receiver_circuit.png
├── docs/
│   └── project_report.pdf
└── README.md
```

---

## ⚙️ Hardware Requirements

| Component | Quantity | Purpose |
|-----------|----------|---------|
| Arduino Uno/Nano | 2 | Microcontroller (TX & RX) |
| High-intensity LED | 1 | Light transmitter |
| Photodiode / LDR | 1 | Light receiver |
| Op-Amp (LM358) | 1 | Signal amplification |
| Resistors, Capacitors | Multiple | Circuit conditioning |
| USB Cables | 2 | Power & programming |

---

## 🚀 Getting Started

### Prerequisites

- Arduino IDE installed
- Arduino Uno/Nano boards
- Basic circuit components (see hardware list above)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Chethu182003/lifi-communication-system.git
   cd lifi-communication-system
   ```

2. **Upload Transmitter Code**
   - Open `transmitter/transmitter.ino` in Arduino IDE
   - Select the correct COM port and board
   - Upload to the **transmitter** Arduino

3. **Upload Receiver Code**
   - Open `receiver/receiver.ino` in Arduino IDE
   - Upload to the **receiver** Arduino

4. **Assemble the Circuit**
   - Build the transmitter and receiver circuits as shown in `/circuit/`
   - Align the LED and photodetector facing each other

5. **Test**
   - Open Serial Monitor (9600 baud) on the receiver Arduino
   - Send data from the transmitter — it will appear decoded on the receiver's serial monitor

---

## 📸 Demo

> _Add photos of your hardware setup and serial monitor output here_

---

## 📊 Results

| Parameter | Value |
|-----------|-------|
| Transmission Medium | Visible Light (LED) |
| Data Encoding | On-Off Keying (OOK) |
| Communication Range | ~1–2 meters (LoS) |
| Baud Rate | 9600 bps |
| Error Rate | < 2% under optimal conditions |

---

## 🧠 What I Learned

- Fundamentals of optical wireless communication (OWC)
- PWM-based signal modulation and demodulation
- Embedded C/C++ programming for real-time systems
- Hardware-software co-design and circuit debugging
- Signal integrity and noise management in analog circuits

---

## 🔮 Future Improvements

- [ ] Increase data rate using advanced modulation (OOK → OFDM)
- [ ] Add full-duplex communication (bidirectional)
- [ ] Implement error detection (CRC / Hamming code)
- [ ] Extend range with higher-power LEDs and lenses
- [ ] Integrate with Raspberry Pi for network-level Li-Fi

---

## 📄 Related Technologies

- **VLC** — Visible Light Communication
- **IrDA** — Infrared Data Association
- **FSO** — Free-Space Optical communication
- **IEEE 802.11bb** — Li-Fi standard (ratified 2023)

---

## 👤 Author

**Chethan** — B.E. Electronics & Communication Engineering  
📍 Bengaluru, India  
🔗 [GitHub](https://github.com/Chethu182003) | [LinkedIn](https://linkedin.com/in/your-profile)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
