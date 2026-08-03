<img width="1600" height="1586" alt="image" src="https://github.com/user-attachments/assets/e0db5cd8-b0d4-4baf-a6e6-f1ddac8af6af" /># DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J)     moment of inertia of the rotor =    0.02 kg.m^2<br>
(b)     motor viscous friction constant =    0.002 N.m.s<br>
(Ktf)    motor torque constant   =           1.5 N.m/Amp<br>
(Ra)    armature resistance  =              2 Ohm<br>
(La)     armature inductance  =              0.5 H<br>
(Kb)      back emf constant = 0.5<br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 
<img width="1600" height="1586" alt="image" src="https://github.com/user-attachments/assets/535a2dfa-91a3-43f5-824a-15ba0cb4097b" />
<img width="1001" height="1600" alt="image" src="https://github.com/user-attachments/assets/d511707e-76b8-4ab2-9218-e866aed08f6c" />
<img width="1534" height="1600" alt="image" src="https://github.com/user-attachments/assets/937955be-aa24-438d-b7e3-f9e2d001f51f" />



## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program
```
Kt = 1.5;
J = 0.02;
B = 0.002;
Ra = 2;
La = 0.5;
Kb = 0.5;
S = tf('s');
ol_sys = Kt / ((J*S*S+B*S)*(Ra+La*S)+Kt*Kb*S);
subplot(2,1,1)
step(ol_sys)
title('Open-Loop Step Response');
Cl_sys = feedback(1*ol_sys,1);
subplot(2,1,2)
step(Cl_sys)
title('Closed-Loop Step Response');
```

## Output
<img width="832" height="646" alt="image" src="https://github.com/user-attachments/assets/3436f2e0-6407-47c6-a47f-4ed5fe84330a" />
<img width="817" height="561" alt="image" src="https://github.com/user-attachments/assets/e31472c5-e45d-496a-a5e7-c8e7b58bffb6" />


## Result
Thus, the position of dc motor is controlled using MATLAB. 
