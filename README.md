# paper  
K: OFDM 的子載波數  
M<sub>T</sub>: 形成信號的波束數  
X<sub>k</sub>: M<sub>T</sub> × M<sub>T</sub> matrix, 第 k 個子載波的信號  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;X<sub>k</sub>=diag(x<sub>k, 1</sub>, x<sub>k, 2</sub>, ..., x<sub>k, M<sub>T</sub></sub>)  
F<sub>k</sub>: N<sub>T</sub> × M<sub>T</sub> matrix, beamforming matrix  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;F<sub>k</sub> = [f<sub>k, 1</sub>, f<sub>k, 2</sub>, ..., f<sub>k, M<sub>T</sub></sub>]  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;transmitter transmits pilots, x<sub>k, u</sub>, using beamforming vectors, f<sub>k, u</sub> ∈ C<sup>N<sub>T</sub> × 1</sup>, u = 1, . . . , M<sub>T</sub>.  
H<sub>k</sub>: N<sub>R</sub> × N<sub>T</sub> matrix, channel matrix  
![image](https://github.com/OuO333333/paper/assets/37506309/3c3344ae-3248-459e-8924-cff06cea28b0)  
![image](https://github.com/OuO333333/paper/assets/37506309/92f8e685-3841-4b06-9fb8-2abe6bffb340)  
![image](https://github.com/OuO333333/paper/assets/37506309/0abea4ce-1978-4e6b-9941-46b647af62ef)

