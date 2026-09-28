# Military LFM Radar Pulse Compression & DRFM ECCM Engine

![Python 3](https://img.shields.io/badge/Language-Python%203.10-blue)
![Electronic Warfare](https://img.shields.io/badge/Domain-Radar%20Signal%20Processing%20%26%20EW-red)
![Developer](https://img.shields.io/badge/Developer-Ayoub%20Lahmar-brightgreen)

An electronic counter-countermeasures (ECCM) signal processing engine for military radar systems. Utilizes Linear Frequency Modulation (LFM) chirp synthesis and fast matched filtering to compress pulse energy and extract true targets amidst active Digital Radio Frequency Memory (DRFM) deceptive jammer signals.

Implemented by **Ayoub Lahmar** ([@Redayoub-lang](https://github.com/Redayoub-lang)).

## 📐 Mathematical Formulation

The complex baseband Linear Frequency Modulation (LFM) chirp pulse \(s(t)\) is formulated as:

$$
s(t) = \exp\left(j \pi K t^2\right), \quad -\frac{\tau}{2} \le t \le \frac{\tau}{2}
$$

Where \(K = \frac{B}{\tau}\) denotes the chirp frequency rate. The matched filter frequency response \(H(f) = S^*(f)\) achieves maximum processing gain \(G_p\):

$$
G_p = 10 \log_{10}(B \cdot \tau)
$$

Target range \(R\) is extracted from matched compression time delay \(\tau_{\text{delay}}\):

$$
R = \frac{c \cdot \tau_{\text{delay}}}{2}
$$

## 💻 Build & Run

```bash
python radar_eccm.py