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

**Rotor-Durchmesser:** 10 m  
**Rotor-Fläche:** \(A = \pi \cdot (5 \, \text{m})^2 = 78,54 \, \text{m}^2\)  
**Leistung bei 5 m/s:** \(P = 2,6 \, \text{kW}\)

**Optimierter Startwind:**  
Der Rotor ist so ausgelegt, dass er bereits bei \(v \geq 1,9 \, \text{m/s}\) anläuft.

> **⚠️ Widerspruch:** In der Datei `06-experimentelle-bestätigungen.md` wird ein Startwind von \(2,3 \, \text{m/s}\) angegeben. Der tatsächliche Startwind muss **gemessen** und **dokumentiert** werden. Er kann nicht aus der Formel abgeleitet werden.

---

## 2. Effizienzsteigerung durch indirekte Kühlung

Die Kühlung der Solarzellen erhöht den Wirkungsgrad um 18 % relativ.  
Die Kühlleistung ergibt sich aus dem Massenstrom des Kühlwassers:

\[
\Delta P_{\text{Solar}} = \eta_{\text{Kühlung}} \cdot P_{\text{Solar,0}}
\]

mit \(\eta_{\text{Kühlung}} \approx 0,18\).

> **⚠️ Validierung:** In der Literatur liegt die Effizienzsteigerung durch Kühlung bei etwa 10–15 %. Der Wert 18 % ist möglich, aber **optimistisch**. Er muss **empirisch validiert** werden.

**Beispielrechnung:**  
\(P_{\text{Solar,0}} = 18.000 \, \text{kWh/Jahr}\)  
\(\Delta P_{\text{Solar}} = 0,18 \cdot 18.000 = 3.240 \, \text{kWh/Jahr}\)

---

## 3. Entsalzung und Wasserbilanz

Der Energiebedarf für die Umkehrosmose beträgt:

\[
E_{\text{Entsalzung}} = \dot{m}_{\text{Wasser}} \cdot e_{\text{spezifisch}}
\]

mit \(e_{\text{spezifisch}} \approx 3 \, \text{kWh/m}^3\).

**Beispielrechnung:**  
\(\dot{m}_{\text{Wasser}} = 5 \, \text{m}^3/\text{Tag} = 1.825 \, \text{m}^3/\text{Jahr}\)  
\(E_{\text{Entsalzung}} = 1.825 \cdot 3 = 5.475 \, \text{kWh/Jahr}\)

> **⚠️ Unvollständig:** Die Formel berücksichtigt **nicht** den Energiebedarf der Pumpen. Der Gesamtbedarf (Entsalzung + Pumpen) liegt bei ca. \(7.300 \, \text{kWh/Jahr}\).

Der Wasserhaushalt wird durch die Bilanzgleichung gesteuert:

\[
\dot{m}_{\text{Zufuhr}} = \dot{m}_{\text{Entsalzung}} + \dot{m}_{\text{Kühlung}} + \dot{m}_{\text{Bewässerung}}
\]

> **⚠️ Unvollständig:** Die Bilanzgleichung sagt nicht, woher das Wasser kommt und wohin es geht. Sie ist **korrekt**, aber **unvollständig**. Sie muss um Quellen und Senken erweitert werden.

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
| \(c_{\text{Sud}}\) | Sud-Konzentration (5–10 %) |
| \(\Psi_{\text{Kohärenz}}\) | Ψ-Feld-Resonanz (0,8 – 1,2) |
| \(\tau\) | Wirkdauer (30 – 45 Tage) |

> **⚠️ Widerspruch:** In der Datei `06-experimentelle-bestätigungen.md` wird \(\alpha_H = 0,15\) angegeben. Hier wird \(\alpha_H = 2,5\) angegeben. Der **richtige** Wert muss **festgelegt** werden.

> **⚠️ Einheit fehlt:** \(\Delta W / \Delta t\) hat **keine** definierte Einheit. Ist es cm/Tag? Oder %/Tag? Oder Meter/Tag? Die Einheit muss **festgelegt** werden.

**Beispielrechnung:**  
Bei \(c = 0,05\), \(\Psi = 1,0\), \(t = 0\):  
\(\frac{dW}{dt} = 2,5 \cdot \log(1,05) \cdot 1,0 \cdot 1 = 2,5 \cdot 0,0488 = 0,122\)  
Bei \(c = 0,10\), \(\Psi = 1,2\), \(t = 0\):  
\(\frac{dW}{dt} = 2,5 \cdot \log(1,10) \cdot 1,2 \cdot 1 = 2,5 \cdot 0,0953 \cdot 1,2 = 0,286\)

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

> **⚠️ Unvollständig:** \(O_{2,\text{max}}\), \(k\) und \(t_0\) sind **nicht definiert**. Sie müssen **festgelegt** werden.

> **⚠️ Widerspruch:** In der Datei `06-experimentelle-bestätigungen.md` wird die **Differentialgleichung** angegeben:
> \[
> \Delta O_2 / \Delta t = \alpha \cdot \Phi \cdot (1 - \beta \cdot T) \cdot \Psi_{Veg} \cdot (1 - O_2 / O_{2,\text{max}})
> \]
> Die Lösung dieser Differentialgleichung ist die **logistische Kurve**. Die Formel in `Kernformeln` ist die **Lösung**. Nicht die **Differentialgleichung**. Das muss **klargestellt** werden.

**Korrekte Darstellung:**

**Differentialgleichung (grundlegend):**
\[
\frac{dO_2}{dt} = \alpha \cdot \Phi \cdot (1 - \beta \cdot T) \cdot \Psi_{Veg} \cdot \left(1 - \frac{O_2}{O_{2,\text{max}}}\right)
\]

**Lösung (logistisch):**
\[
O_2(t) = \frac{O_{2,\text{max}}}{1 + e^{-k(t - t_0)}}
\]

mit \(k = \alpha \cdot \Phi \cdot (1 - \beta \cdot T) \cdot \Psi_{Veg}\)

**Parameter:**
- \(\alpha = 0,042 \, \text{pro Monat}\)
- \(\Phi = 0,8\)
- \(\beta = 0,003 \, \text{pro °C}\)
- \(T = 15 \, ^\circ\text{C}\)
- \(\Psi_{Veg} = 1,2\)
- \(O_{2,\text{max}} = f(\text{Erdgeschichte})\)

---
