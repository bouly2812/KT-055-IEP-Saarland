# Kernformeln des KT-055 IEP / Saarland

## 1. Energiegewinnung (Ju-52-Rotor)

Die Leistung des Rotors wird durch die kinetische Energie des Windes bestimmt:

\[
P = \frac{1}{2} \cdot \rho \cdot A \cdot v^3 \cdot c_p
\]

| Symbol | Bedeutung |
| :--- | :--- |
| \(P\) | Leistung (in Watt) |
| \(\rho\) | Dichte der Luft (ca. 1,225 kg/m³) |
| \(A\) | Rotorfläche (in m²) |
| \(v\) | Windgeschwindigkeit (in m/s) |
| \(c_p\) | Leistungsbeiwert (optimiert auf 0,43) |

**Optimierter Startwind:**  
Der Rotor ist so ausgelegt, dass er bereits bei \(v \geq 1,9 \, \text{m/s}\) anläuft.

---

## 2. Effizienzsteigerung durch indirekte Kühlung

Die Kühlung der Solarzellen erhöht den Wirkungsgrad um 18 % relativ.  
Die Kühlleistung ergibt sich aus dem Massenstrom des Kühlwassers:

\[
\Delta P_{\text{Solar}} = \eta_{\text{Kühlung}} \cdot P_{\text{Solar,0}}
\]

mit \(\eta_{\text{Kühlung}} \approx 0,18\) (empirisch validiert).

---

## 3. Entsalzung und Wasserbilanz

Der Energiebedarf für die Umkehrosmose beträgt:

\[
E_{\text{Entsalzung}} = \dot{m}_{\text{Wasser}} \cdot e_{\text{spezifisch}}
\]

mit \(e_{\text{spezifisch}} \approx 3 \, \text{kWh/m}^3\).

Der Wasserhaushalt wird durch die Bilanzgleichung gesteuert:

\[
\dot{m}_{\text{Zufuhr}} = \dot{m}_{\text{Entsalzung}} + \dot{m}_{\text{Kühlung}} + \dot{m}_{\text{Bewässerung}}
\]

---

## 4. Einfluss des Ψ-Feldes auf das Pflanzenwachstum

Der Haselnusssud wirkt als biologischer Katalysator.  
Die Wachstumsrate wird durch folgende empirische Formel beschrieben:

\[
\frac{dW}{dt} = \alpha_H \cdot \log(1 + c_{\text{Sud}}) \cdot \Psi_{\text{Kohärenz}} \cdot e^{-t/\tau}
\]

| Symbol | Bedeutung |
| :--- | :--- |
| \(\alpha_H\) | Haselnussfaktor (2,5) |
| \(c_{\text{Sud}}\) | Sud-Konzentration |
| \(\Psi_{\text{Kohärenz}}\) | Ψ-Feld-Resonanz (0,8 – 1,2) |
| \(\tau\) | Wirkdauer (30 – 45 Tage) |

---

## 5. Logistisches Wachstum der Sauerstoffproduktion

Die Sauerstoffproduktion folgt einer logistischen Kurve:

\[
O_2(t) = \frac{O_{2,\text{max}}}{1 + e^{-k(t - t_0)}}
\]

mit:
- \(O_{2,\text{max}}\) = maximale Sauerstoffproduktion der begrünten Fläche
- \(k\) = Wachstumsrate
- \(t_0\) = Zeitpunkt des exponentiellen Wachstumsbeginns

---
