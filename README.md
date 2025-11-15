# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as nm
import matplotlib.pyplot as pot
Am = 6.9
fm = 549
Ac = 13.8
fc = 5490
fs = 54900
b = 7.0
t = nm.arange(0,2/fm,1/fs)
m= Am*nm.cos(2*nm.pi*fm*t)
pot.subplot(3,1,1)
pot.plot(t,m)
c= Ac*nm.cos(2*nm.pi*fc*t)
pot.subplot(3,1,2)
pot.plot(t,c)
s=Ac*nm.cos(2*nm.pi*fc*t+b*nm.sin(2*nm.pi*fm*t))
pot.subplot(3,1,3)
pot.plot(t,s)
```

Output Waveform

<img width="700" height="521" alt="image" src="https://github.com/user-attachments/assets/5ba8c20e-e40c-48b3-96a5-2b56743b41e1" />


Tabular Column

<img width="712" height="900" alt="image" src="https://github.com/user-attachments/assets/db378fd4-6bde-46cd-9bf0-ed5c5638788d" />




Calculation

<img width="651" height="232" alt="image" src="https://github.com/user-attachments/assets/19932b5e-d74e-47ef-89a7-5b390fce92b9" />




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
