# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM
```program
clc; 
clear; 

xn = [1 2 3 4 4 3 2 1]; 

n1 = 0:1:length(xn)-1; 
subplot(3,1,1); 
plot2d3(n1, xn); 
xlabel('Time n'); 
ylabel('Amplitude xn'); 
title('Input Sequence'); 

j = sqrt(-1); 
N = length(xn); 
Xk = zeros(1, N); 

for k = 0:N-1 
    for n = 0:N-1 
        Xk(k+1) = Xk(k+1) + xn(n+1)*exp((-j*2*%pi*k*n)/N); 
    end 
end 

disp(Xk); 

K1 = 0:1:length(Xk)-1; 
magnitude = abs(Xk); 

subplot(3,1,2); 
plot2d3(K1, magnitude); 
xlabel('frequency(Hz)'); 
ylabel('magnitude(gain)'); 
title('magnitude spectrum'); 

angle = atan(imag(Xk), real(Xk)); 

subplot(3,1,3); 
plot2d3(K1, angle); 
xlabel('frequency(Hz)'); 
ylabel('Phase'); 
title('Phase spectrum');
```
### CALCULATIONS:
<br>
<br>
<br>
<br>
<br>
### SAMPLE OUTPUT:
<br>
<br>
<br>
<br>



## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.

