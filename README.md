# Laser-Protocol-Java

An implementation of a stateful, encrypted binary messaging protocol client in Java. This project focuses on the low-level mechanics of socket communication, custom bit-level serialization, and authenticated encryption.

### Technical Implementation

This repository demonstrates several core systems engineering concepts:

* **Networking:** Asynchronous TCP socket management and handling of fragmented packet reassembly.
* **Security:** Implementation of the **NaCl (Networking and Cryptography)** library for public-key exchange (Curve25519) and session-based authenticated encryption.
* **Data Serialization:** Manual management of byte-streams for encoding and decoding complex data types into a structured binary format.
* **Architecture:** Utilization of the **Factory Pattern** (`LogicLaserMessageFactory`) for dynamic message type resolution.

### Research Objectives

1. **Handshake Security:** Analyzing the efficiency of NaCl-box handshakes in high-latency networking environments.
2. **Stream Integrity:** Implementing robust byte-stream readers to handle packet framing and protocol versioning.
3. **State Management:** Maintaining a consistent client-side state machine during asynchronous communication with a remote host.

### Usage

**Compilation:**
Navigate to the source directory and compile the entry point:

```bash
cd src
javac com/haccercat/client/Main.java -d out

```

**Execution:**
Start the client by targeting a host and port:

```bash
cd out
java com/haccercat/client/Main <host> <port>

```

**Protocol Analysis:**
To enable decryption and dumping of server-side payloads for research purposes:

```bash
java com/haccercat/client/Main <host> <port> dump

```

### Technical Note

This software is intended for educational research into network security and binary protocol analysis. Usage of this tool is at the sole responsibility of the user, and it must be utilized in accordance with relevant terms of service and local regulations.

---

### Credits

Developed by **S.B** and **risporce#6552**.

* Updated protocol support and logic refinements provided by community contributors.

### Support

If this implementation was a helpful reference for your research or learning, feel free to leave a 🌟!

**[Join the community](https://discord.peterr.dev)**
