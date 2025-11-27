# SSB

EXP NO: 3	SSB-SC-AM MODULATION using SCILAB

AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

Note: Keep all the switch faults in off position


Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: The baseband signal that will be modulated.
•	Carrier Signal: A high-frequency signal used for modulation.
•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
3.	SSBSC Modulation:
•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
4.	SSBSC Demodulation:
•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
5.	Visualization:
•	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.


PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="704" height="178" alt="image" src="https://github.com/user-attachments/assets/32ee29b3-0d95-4192-9762-972d50c05c90" />
<img width="706" height="167" alt="image" src="https://github.com/user-attachments/assets/bff0d8fd-d679-444e-af37-0b34585853c1" />

Program
```
Ac=10.3; 
fc=2030; 
Am=4.3; 
fm=330; 
fs=25000; 
t=0:1/fs:2/fm; 
Wm=2*3.14*fm; 
Wc=2*3.14*fc; 
Em=Am*sin(2*3.14*fm*t); 
subplot(2,2,1); 
title('Message'); 
plot(t,Em); 
Ec=Ac*sin(2*3.14*fc*t); 
subplot(2,2,2); 
title('Carrier'); 
plot(t,Ec); 
Edsbsc1=((Am/2)*cos((Wc-Wm)*t))-((Am/2)*cos((Wc+Wm)*t)); 
Edsbsc2=((Am/2)*cos((Wc-Wm)*t))+((Am/2)*cos((Wc+Wm)*t)); 
Elsb=Edsbsc1+Edsbsc2; 
subplot(2,2,3); 
title('Lsb'); 
plot(t,Elsb); 
Eusb=Edsbsc2-Edsbsc1; 
subplot(2,2,4); 
title('Usb'); 
plot(t,Eusb);
```
OUTPUT WAVEFORM

<img width="1785" height="855" alt="image" src="https://github.com/user-attachments/assets/cace67ab-a221-4647-9716-a908d86220d2" />


TABULATION

<img width="1600" height="1385" alt="image" src="https://github.com/user-attachments/assets/14f8f49c-30ae-4618-ab69-6ae943fffcf2" />








RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





