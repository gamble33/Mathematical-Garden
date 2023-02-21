#Physics 

# Capacitor
---
## [[Energy]] Stored
$$\text{energy stored in the capacitor}=\frac{1}{2}QV$$
Only half the of the energy provided by the circuit is store in the capacitor, the rest is dissipated as heat.
$$V=\frac{Q}{C}$$
$$Q=CV$$
$$E=\frac{1}{2}\frac{Q^2}{C}$$
$$E=\frac{1}{2}CV^2$$

# Capacitor Equations during Discharge
$$Q=Q_0e^{-\frac t{CR}}$$
where:
* $Q$ is the charge after time $t$
	* This is the measure of charge at the (negative) terminal of the capacitor
* $Q_0$ is the initial charge at time $t=0$
* $t$ is time ($s$) after the switch has been flipped, and the capacitor begins to discharge.

$$I=I_0e^{-\frac t{CR}}$$
$$V=V_0e^{-\frac t{CR}}$$

> [!Side Note]
> For charging a capacitor, the formula is
> $$Q=Q_0\left(1-e^{-\frac{t}{RC}}\right)$$


## Uses
- Smoothing out [[Voltage|voltages]] in sensitive circuits.
- Short term back-up supply voltages (e.g., to give enough time for a PC to save its state when power is cut).
- Timing circuits (the charge/discharge rate of the capacitor can be used to time short delays in circuits, e.g., interrupts in processing chips)
- Pulsing circuits (circuits that repeatedly turn on and off).
- Tuning circuits (The charge/discharge rate of a capacitor has a natural oscillation that varying [[Resistance|resistance]] in the circuit effects. By fine tuning this resistance, you can calibrate an RC circuit to oscillate to a certain input frequency and tune a radio).
- Filter circuits (To filter out unwanted frequencies and tune a radio).