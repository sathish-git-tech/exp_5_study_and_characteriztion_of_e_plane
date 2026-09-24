# exp_5_study_characteriztion_of_e_plane

# Experiment 5 — Study and Characterization of E-Plane Tee

---

## Aim

To study and measure the characteristics of an E-plane tee.

## Apparatus Used

Klystron power supply, klystron mount with tube, isolator, variable attenuator, frequency meter, slotted line section, E-plane tee, detector mount / crystal detector, matched terminations, VSWR meter, waveguide stands.

## Experimental Setup

<img width="744" height="484" alt="image" src="https://github.com/user-attachments/assets/ea65ce6c-aced-4c5f-9f66-a6fcb5daff1b" />



---

## Theory

In an E-plane tee an auxiliary waveguide arm is fastened to the **broader wall** of the main guide. It is a three-port device in which the axis of the auxiliary arm is parallel to the plane of the electric field of the main guide, and the coupling from the main guide to the auxiliary guide is by means of **electric fields** — hence the name E-plane tee.

The junction causes the loads connected to its branches to appear **in series**, so it is often referred to as a **series tee**.

The two main-guide arms are symmetrical with respect to the auxiliary arm. If power is fed from the auxiliary arm it is distributed equally into arms 1 and 2 when they are terminated in equal loads. However, from the field configuration, the power flowing out of arm 1 is **180° out of phase** with that in arm 2. The E-plane tee therefore acts as a **subtractor (differencer)**.

### Summary of behaviour

| Feed point | Result |
|---|---|
| Auxiliary (E) arm | Equal split into arms 1 and 2, 180° out of phase |
| Arms 1 and 2 (equal, in phase) | Signals subtract at the E-arm |
| Function | Subtractor / differencer, series tee |

---

## Procedure

1. Set up the microwave bench: klystron power supply → klystron mount → isolator → variable attenuator → frequency meter → slotted section → component under test (E-plane tee) → detector mount → VSWR meter.
2. Keep the control knobs of the klystron power supply at their initial settings (mode switch: AM; beam voltage knob: fully anti-clockwise; repeller voltage knob: fully clockwise; meter switch: beam current) and switch on the supply, the VSWR meter and the cooling fan.
3. Energise the klystron for maximum output at the desired frequency by adjusting the beam and repeller voltages; measure the operating frequency with the frequency meter and then detune it.
4. **Reference reading:** without the E-plane tee in the line, set the variable attenuator to obtain a convenient full-scale reference reading on the VSWR meter. Note the attenuator setting **A₁** dB.
5. **Insert the component:** connect the E-plane tee in the line, feeding the arm under test and terminating the remaining arms in matched loads.
6. Reduce the attenuation until the VSWR meter reads the same reference value. Note the attenuator setting **A₂** dB. The difference (A₁ − A₂) dB gives the coupling/isolation for that pair of ports.
7. **Power division:** feed the E-arm, terminate one collinear arm in a matched load and measure the power at the other collinear arm; repeat with the arms interchanged. The measured coupling should be about **3 dB** for each collinear arm.
8. **Isolation:** feed the E-arm and measure the power coupled to the isolated port, with all other ports match-terminated.
9. **VSWR of each port:** feed the port under test, terminate the remaining ports in matched loads, and measure the VSWR using the slotted line.
10. Repeat the measurements for each of the three ports.

---

## Observation

### OBSERVATION

**Operating Frequency:** $9.45\text{ GHz}$

**Reference Power (Direct Connection without E-Plane Tee):** $P_{\text{ref}} = 0\text{ dB}$ (or Initial Attenuator Setting $A_1 = 38.0\text{ dB}$)

---

#### Table 1: Power Distribution & Coupling Characteristics (Input at E-Arm, Port 3)

| Input Port | Output Port | Terminated Port | Attenuator Reading $A_2$ (dB) | Power Received $P_{\text{out}}$ (dB) | Coupling / Attenuation $(A_1 - A_2)$ (dB) | Theoretical Value (dB) |
| --- | --- | --- | --- | --- | --- | --- |
| **Port 3 (E-arm)** | Port 1 (Collinear 1) | Port 2 (Matched Load) | $34.8$ | $-3.2$ | $3.2$ | $3.0$ |
| **Port 3 (E-arm)** | Port 2 (Collinear 2) | Port 1 (Matched Load) | $34.7$ | $-3.3$ | $3.3$ | $3.0$ |

---

#### Table 2: Isolation and Cross-Coupling Measurements

| Input Port | Output Port | Terminated Port | Attenuator Reading $A_2$ (dB) | Power Received $P_{\text{out}}$ (dB) | Isolation / Attenuation $(A_1 - A_2)$ (dB) |
| --- | --- | --- | --- | --- | --- |
| **Port 1** | Port 2 | Port 3 (Matched Load) | $35.9$ | $-2.1$ | $2.1$ |
| **Port 1** | Port 3 (E-arm) | Port 2 (Matched Load) | $34.8$ | $-3.2$ | $3.2$ |
| **Port 2** | Port 3 (E-arm) | Port 1 (Matched Load) | $34.7$ | $-3.3$ | $3.3$ |

---

#### Table 3: VSWR Measurements at Each Port

| Port Under Test | Remaining Ports Terminated In | Voltage Maximum $V_{\max}$ (V) | Voltage Minimum $V_{\min}$ (V) | Measured VSWR ($S = V_{\max} / V_{\min}$) |
| --- | --- | --- | --- | --- |
| **Port 1 (Collinear Arm 1)** | Ports 2 & 3 (Matched Loads) | $1.42$ | $1.00$ | $1.42$ |
| **Port 2 (Collinear Arm 2)** | Ports 1 & 3 (Matched Loads) | $1.44$ | $1.00$ | $1.44$ |
| **Port 3 (E-Plane Arm)** | Ports 1 & 2 (Matched Loads) | $1.76$ | $1.00$ | $1.76$ |

---

### CALCULATION

**1. Power Division Difference ($\Delta P$):**


$$\Delta P = \vert{}P_{\text{Port 1}} - P_{\text{Port 2}}\vert{} = \vert{}-3.2\text{ dB} - (-3.3\text{ dB})\vert{} = 0.1\text{ dB}$$


*(Confirms nearly equal 3 dB power split into the two collinear arms)*

**2. S-Matrix Representation (Experimental Magnitudes):**


$$[S] = \begin{bmatrix}  0.17 & 0.78 & 0.69 \\  0.78 & 0.18 & -0.68 \\  0.69 & -0.68 & 0.27  \end{bmatrix}$$

---




---

## Precautions

* Check all connections before switching on the kit.
* Keep all knobs at minimum before switching on the power supplies; the HT must be OFF while switching on the mains.
* Do not exceed a beam current of 30 mA, and keep the repeller voltage within the specified range.
* Terminate all unused ports in matched loads while taking readings.
* Do not look directly into an open waveguide.

## Result

The characteristics of the E-plane tee were studied.
