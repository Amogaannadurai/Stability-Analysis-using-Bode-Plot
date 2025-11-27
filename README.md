## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
Open MATLAB software
Open a new script file.
Type the program.
Save and Execute the program.
Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
Also determine the stability.

![IMG-20251127-WA0013](https://github.com/user-attachments/assets/b6706967-3620-4929-bd64-e9a9606daf66)
![IMG-20251127-WA0014](https://github.com/user-attachments/assets/63558234-1b1e-4723-bf45-72c98480199d)
![IMG-20251127-WA0015](https://github.com/user-attachments/assets/bee1454a-d922-4b3a-a404-4f4b1472a905)

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```


## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/edf7c306-6a13-4967-a07f-bc8b6bc31520" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60 <br>
Gain crossover frequency =  0.907 <br>
Phase crossover frequency = 4.4721 <br>
The system is  stable

