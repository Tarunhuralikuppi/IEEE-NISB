## Low-pass filter for a sensor signal
#### Aim:Design a low-pass filter for a 1kHz sensor signal with a 10kHz cutoff. Which filter type would you choose and why? How would you calculate the RC values? How would you handle high-frequency spikes?
#### Requirements: Signal Genrator, Resistor(Ω), Capacitor(F).
 The Low-pass filter I used in the question to design this is RC Low-pass filter.
 
 Reason behind this filter to use is its cost efeective which makes low cost solution,Easy to Implement in the circuit,Take less size to build it,Dosen't require any external power supply to it,Direct debug of solution when there is problem in resistor or capacitor.This makes the RC low-pass filter a reliable to use in our application of sensor signal.  

## Circuit Design:
![RC Low pass filter](https://github.com/user-attachments/assets/0df5c190-fe1e-4018-8084-7cfa516faba6)

Signal generator is connected to the Resistor and capacitor in series combination where the output is drawn across a capacitor,where the actual fitering takes place.

The input value by signal generator is the sensor signal of 1kHz,Dc offset Voltage is 10v,amplitude is 1V.

For the selection of the resistor and capacitor value we have the cutoff frequency of 10kHz

Cutoff frequency of low pass capacitor is given by

```math
fh = \frac{1}{2.π.R.C}
```
Assume Resistor(R)=1.5kΩ
and having f<sub>h</sub>=10kHz
```math
C = \frac{1}{2.π.R.f<sub>h</sub>}
```
```math
C=\frac{1}{2*π*1.5*1000*10*1000}=10.60nF
```
Hence the capacitor for the cutoff frequency of 10kHz is 10.6nF

AC analysis of the circuit:
![frequency response](https://github.com/user-attachments/assets/56e63f3a-b858-4af0-ad81-377295e47e53)


The high frequency spikes are handled by usinng RC low pass filter which filters out low frequency signal above the cutoff frequency and reaches the low frequency signal to the output.
