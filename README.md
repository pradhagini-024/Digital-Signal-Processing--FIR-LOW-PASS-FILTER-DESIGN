# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.

## Software Required:
MAT LAB R2012.

## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
% Pradhagini A [212224050031]

clc; % clear screen 
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%Low Pass Filter Coefficient
n=0:1:N-1;
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Blackman Window Sequence
n=0:1:N-1;
wh = 0.42 - 0.5*cos((2*pi*n)/(N-1)) + 0.08*cos((4*pi*n)/(N-1))
hn=hd.*wh
% Plot the Low Pass Filter with Blackman Window Technique 
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'ms');
```

## OUTPUT:
<img width="1588" height="927" alt="image" src="https://github.com/user-attachments/assets/e52ab945-f7c2-491d-97e5-bdbae2f90c0b" />

## RESULT:
<img width="1600" height="768" alt="image" src="https://github.com/user-attachments/assets/5aac28c0-fd64-461a-8b77-448cafe969f5" />
