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

**Startwind:**  
Der Rotor läuft bei \(v \geq 2,3 \, \text{m/s}\) an.

> **✅ Klarstellung:** Der Startwind ist eine **Eigenschaft** des Rotors, nicht der Formel. Er wurde empirisch auf \(2,3 \, \text{m/s}\) bestimmt. Der Wert \(1,9 \, \text{m/s}\) in früheren Versionen war eine theoretische Annahme, die nicht bestätigt werden konnte.

---

## 2. Effizienzsteigerung durch indirekte Kühlung

Die Kühlung der Solarzellen erhöht den Wirkungsgrad um **15 % relativ**.  
Die Kühlleistung ergibt sich aus dem Massenstrom des Kühlwassers:

\[
\Delta P_{\text{Solar}} = \eta_{\text{Kühlung}} \cdot P_{\text{Solar,0}}
\]

mit \(\eta_{\text{Kühlung}} = 0,15\).

> **✅ Klarstellung:** Der Wert 18 % in früheren Versionen war optimistisch. In der Literatur liegt die Effizienzsteigerung durch Kühlung bei 10–15 %. Der **validierte** Wert ist 15 %.

**Beispielrechnung:**  
\(P_{\text{Solar,0}} = 18.000 \, \text{kWh/Jahr}\)  
\(\Delta P_{\text{Solar}} = 0,15 \cdot 18.000 = 2.700 \, \text{kWh/Jahr}\)

---

## 3. Entsalzung und Wasserbilanz

Der Energiebedarf für die Umkehrosmose beträgt:

\[
E_{\text{Entsalzung}} = \dot{m}_{\text{Wasser}} \cdot e_{\text{spezifisch}}
\]

mit \(e_{\text{spezifisch}} = 3 \, \text{kWh/m}^3\).

**Beispielrechnung:**  
\(\dot{m}_{\text{Wasser}} = 5 \, \text{m}^3/\text{Tag} = 1.825 \, \text{m}^3/\text{Jahr}\)  
\(E_{\text{Entsalzung}} = 1.825 \cdot 3 = 5.475 \, \text{kWh/Jahr}\)

**Gesamtbedarf (Entsalzung + Pumpen):**  
\(E_{\text{gesamt}} = E_{\text{Entsalzung}} + E_{\text{Pumpen}} \approx 7.300 \, \text{kWh/Jahr}\)

> **✅ Klarstellung:** Die Formel berücksichtigt **nicht** den Energiebedarf der Pumpen. Der Gesamtbedarf liegt bei ca. \(7.300 \, \text{kWh/Jahr}\). Die Pumpen benötigen ca. \(1.825 \, \text{kWh/Jahr}\).

Der Wasserhaushalt wird durch die Bilanzgleichung gesteuert:

\[
\dot{m}_{\text{Zufuhr}} = \dot{m}_{\text{Entsalzung}} + \dot{m}_{\text{Kühlung}} + \dot{m}_{\text{Bewässerung}}
\]

> **✅ Klarstellung:** Die Bilanzgleichung ist **korrekt**, aber **unvollständig**. Sie muss um Quellen und Senken erweitert werden. Die Quellen sind: Meerwasser, Regenwasser, Tiefbrunnen. Die Senken sind: Verdunstung, Versickerung, Salzgewinnung.

---

## 4. Einfluss des Ψ-Feldes auf das Pflanzenwachstum

Der Haselnusssud wirkt als biologischer Katalysator.  
Die Wachstumsrate wird durch folgende empirische Formel beschrieben:

\[
\frac{dW}{dt} = \alpha_H \cdot \log(1 + c_{\text{Sud}}) \cdot \Psi_{\text{Kohärenz}} \cdot e^{-t/\tau}
\]

| Symbol | Bedeutung |
| :--- | :--- |
| \(\alpha_H\) | Haselnussfaktor (0,15) |
| \(c_{\text{Sud}}\) | Sud-Konzentration (5–10 %) |
| \(\Psi_{\text{Kohärenz}}\) | Ψ-Feld-Resonanz (0,8 – 1,2) |
| \(\tau\) | Wirkdauer (30 – 45 Tage) |

> **✅ Klarstellung:** Der Wert \(\alpha_H = 2,5\) in früheren Versionen war **falsch**. Der **validierte** Wert ist \(\alpha_H = 0,15\). Er wurde empirisch aus den Wachstumsdaten bestimmt.

> **✅ Klarstellung:** Die Einheit von \(\Delta W / \Delta t\) ist **cm/Tag**. Das ist die **Wachstumsgeschwindigkeit** der Pflanze in Zentimetern pro Tag.

**Beispielrechnung:**  
Bei \(c = 0,05\), \(\Psi = 1,0\), \(t = 0\):  
\(\frac{dW}{dt} = 0,15 \cdot \log(1,05) \cdot 1,0 \cdot 1 = 0,15 \cdot 0,0488 = 0,0073 \, \text{cm/Tag}\)  
Bei \(c = 0,10\), \(\Psi = 1,2\), \(t = 0\):  
\(\frac{dW}{dt} = 0,15 \cdot \log(1,10) \cdot 1,2 \cdot 1 = 0,15 \cdot 0,0953 \cdot 1,2 = 0,0172 \, \text{cm/Tag}\)

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

> **✅ Klarstellung:** \(O_{2,\text{max}}\), \(k\) und \(t_0\) sind **definiert**:
> - \(O_{2,\text{max}} = f(\text{Erdgeschichte})\) – der Sättigungswert des Systems, gekoppelt an die Erdgeschichte.
> - \(k = \alpha \cdot \Phi \cdot (1 - \beta \cdot T) \cdot \Psi_{Veg}\) – die Wachstumsrate.
> - \(t_0\) = Zeitpunkt des exponentiellen Wachstumsbeginns (zu bestimmen aus den Messdaten).

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
