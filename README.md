# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM
```scilab
clear;
clc;
close;
xn = [1 2 3 4];
n1 = 0:1:length(xn)-1;

subplot(2,2,1);
plot2d3(n1,xn);

xlabel('Time n');
ylabel('Amplitude');
title('Input Sequence');


Xk = fft(xn);
K1 = 0:1:length(Xk)-1;
magnitude = abs(Xk)

subplot(2,2,2);
plot2d3(K1, magnitude);

xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');

angle = atan(imag(Xk), real(Xk))

subplot(2,2,3);
plot2d3(K1, angle);

xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum');

y = ifft(Xk);
n2 = 0:1:length(y)-1;

subplot(2,2,4);
plot2d3(n2, y);

xlabel('Time n');
ylabel('Amplitude');
title('Inverse FFT OF X(K)');
```
### CALCULATIONS:

 <img width="1600" height="903" alt="207c34be-7df1-4869-b04d-c3f1d36d923f" src="https://github.com/user-attachments/assets/bb37f521-d4ae-46f7-ae5b-3510506375f0" />

 <img width="1600" height="903" alt="dd2434a7-6fa3-4b70-b87d-8a589bae2a00" src="https://github.com/user-attachments/assets/94036a3e-edf2-41a5-ac80-e9c75e84192d" />

### SAMPLE OUTPUT:
<img width="876" height="697" alt="553899618-79c7d5f1-7c8b-4090-bf88-1d75724fd0f1" src="https://github.com/user-attachments/assets/c20db670-5404-4576-8c55-3a5a80b7d51e" />


## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.

