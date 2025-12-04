# AUTO-CORRELATION-AND-PSD
## Aim
Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

## Equipments Needed
Computer with Intel i3 processor (or higher)
Scilab software
## Theory
The Wiener–Khinchin theorem states that:

The Power Spectral Density (PSD) of a wide-sense stationary random process is the Fourier Transform of its autocorrelation function.

<img width="466" height="74" alt="image" src="https://github.com/user-attachments/assets/18836991-c95b-479c-b874-e1fdf43d2eb9" />

This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.

## Algorithm
Load or Define the Signal: Input your time-domain signal.
Compute Autocorrelation: Calculate the autocorrelation function of the signal.
Compute Power Spectral Density (PSD):
Estimate the PSD using either:
Fourier Transform of the autocorrelation function, or
Methods like Welch’s periodogram.
Plot Results: Visualize both the autocorrelation function and PSD.
Procedure
Refer to the algorithm and write the code for the experiment.
Open Scilab on your system.
Type your code in a new editor.
Save the file.
Execute the code.
If any errors occur, debug and re-run the program.
Verify the generated waveform using tabulation and model waveform comparison.
## Program (Scilab Code)
```
clc
clc
clear all; 
t=0:0.01:2*%pi;
x=sin(9*t) + cos(7*t);
subplot(3,2,1);
plot(x);
au=xcorr(x,x);
subplot(3,2,2);
plot(au);
v=fft(au);
subplot(3,2,3);
plot(abs(v));
fw=fft(x);
subplot(3,2,4);
plot(fw);
fw2=(abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```
Output:
![WhatsApp Image 2025-12-01 at 10 30 28_b85d69e0](https://github.com/user-attachments/assets/965293c0-be08-48ac-b4cb-dbf8f971ad92)

![exp 9](https://github.com/user-attachments/assets/2b73442b-e924-4c81-9f0f-37691856ab1b)


Result:
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.

