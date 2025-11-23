# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__
```
import numpy as np
import matplotlib.pyplot as plt
Am = 15.2
Fm = 460
B = 5.8
Ac = 30.4
Fc = 4600
Fs = 4600000
t = np.arange(0, 2/Fm, 1/Fs)
em = Am * np.cos(2 * np.pi * Fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, em)
plt.grid()
ec = Ac * np.cos(2 * np.pi * Fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, ec)
plt.grid()
efm = Ac * np.cos((2*np.pi*Fc*t) + ( B*np.sin(2*np.pi*Fm*t)))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.tight_layout()
plt.show()
```

__Tabulation__:

<img width="1056" height="1144" alt="image" src="https://github.com/user-attachments/assets/8d664eeb-192d-47c0-919c-eaa635ef74e1" />

__Calculation__:

▲f  = Fmax – Fc
       = 4761.904 - 6600
       = 161.904
ß = ▲f/Fm
   = 161.904 / 460
   = 0.3

__Output:__

<img width="784" height="585" alt="image" src="https://github.com/user-attachments/assets/e74bf09b-39ab-4bed-b8af-77d4af8b904a" />


__Result:__

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
