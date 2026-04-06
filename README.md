# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1='); 
Wc2=input('enter the value of Wc2='); 
N=input('enter the value of N=');
alpha=(N-1)/2; 
eps=0.001;

%Band Pass Filter Coefficient
n=0:1:N-1; 
hd=(sin(Wc1*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)

%Hanning Window Sequence 
n=0:1:N-1; 
wh=0.5-0.5*cos((2*pi*n)/(N-1)) 
hn=hd.*wh

% Plot the Low Pass Filter with Hanning Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'blue');

## OUTPUT:
![WhatsApp Image 2026-03-26 at 1 36 44 PM](https://github.com/user-attachments/assets/99cae421-95b0-49ac-9c25-eb064bf140d6)


## RESULT:
![WhatsApp Image 2026-04-05 at 4 58 22 PM (1)](https://github.com/user-attachments/assets/3283c76c-8a5a-4c58-874f-53fea73d70ce)


Step 6: Terminate the program.

## PROGRAM: 

## OUTPUT:

## RESULT:
