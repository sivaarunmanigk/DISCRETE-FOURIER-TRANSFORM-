# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 

To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
# DIRECT
    clc;
    clear;
    close;
    
    // Input sequence
    x = [1 2 3 4];
    
    // Length of sequence
    N = length(x);
    
    // Initialize output
    X = zeros(1, N);
    
    // Direct DFT computation
    for k = 0:N-1
        sum1 = 0;
        for n = 0:N-1
            sum1 = sum1 + x(n+1)*exp(-%i*2*%pi*k*n/N);
        end
        X(k+1) = sum1;
    end
    
    // Display result
    disp("DFT using Direct Method:");
    disp(X);
    
    // Plot magnitude spectrum
    plot2d3(0:N-1, abs(X));
    xtitle("DFT using Direct Method", "Frequency Index", "Magnitude");
    
 # FFT
    clc;
    clear;
    close;
    
    // Input sequence
    x = [1 2 3 4];
    
    // FFT computation
    X = fft(x, -1);
    
    // Display result
    disp("DFT using FFT Method:");
    disp(X);
    
    // Plot magnitude spectrum
    plot2d3(0:length(x)-1, abs(X));
    xtitle("DFT using FFT Method", "Frequency Index", "Magnitude");
# OUTPUT: 
# DIRECT
<img width="1919" height="1138" alt="Screenshot 2026-05-21 151834" src="https://github.com/user-attachments/assets/d65f993f-a864-44bd-bc16-e39d59026c6c" />
# FFT
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/ef32de03-9f0c-46f0-a0bb-8060f951da20" />

# RESULT: 
Thus,The DFT and FFT of the given sequence is obtained using SCILAB.
