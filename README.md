# paper  
K: OFDM 的子載波數  
M<sub>T</sub>: 形成信號的波束數  
X<sub>k</sub>: M<sub>T</sub> × M<sub>T</sub> matrix, 第 k 個子載波的信號  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;X<sub>k</sub>=diag(x<sub>k, 1</sub>, x<sub>k, 2</sub>, ..., x<sub>k, M<sub>T</sub></sub>)  
F<sub>k</sub>: N<sub>T</sub> × M<sub>T</sub> matrix, beamforming matrix  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;F<sub>k</sub> = [f<sub>k, 1</sub>, f<sub>k, 2</sub>, ..., f<sub>k, M<sub>T</sub></sub>]  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;transmitter transmits pilots, x<sub>k, u</sub>, using beamforming vectors, f<sub>k, u</sub> ∈ C<sup>N<sub>T</sub> × 1</sup>, u = 1, . . . , M<sub>T</sub>.  
![image](https://github.com/OuO333333/paper/assets/37506309/bf701a0a-867e-402f-a40d-0a9a2d2e8e82)
![image](https://github.com/OuO333333/paper/assets/37506309/e4d5dbc9-de8d-4c66-a872-1198bc912a50)  
H<sub>k</sub>: N<sub>R</sub> × N<sub>T</sub> matrix, channel matrix  
W<sub>k</sub>: N<sub>R</sub> × M<sub>R</sub> matrix, combining matrix  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;W<sub>k</sub> = [w<sub>k, 1</sub>, w<sub>k, 2</sub>, ..., w<sub>k, M<sub>R</sub></sub>]  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;combining vectors, w<sub>k, v</sub> ∈ C<sup>N<sub>R</sub> × 1</sup> , v = 1, ..., M<sub>R</sub>  
![image](https://github.com/OuO333333/paper/assets/37506309/427724a9-17b8-4cbc-8ec0-1fe5582f199f)
![image](https://github.com/OuO333333/paper/assets/37506309/9f036727-d641-4231-9980-ba79a88d666b)  
Ñ<sub>k</sub>: M<sub>R</sub> × M<sub>T</sub> matrix, noise matrix  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ñ<sub>k</sub> = W<sub>k</sub><sup>H</sup> × N<sub>k</sub>  
![image](https://github.com/OuO333333/paper/assets/37506309/9d13af86-0c04-44a6-90d8-a26283e29b1f)???

  
-------------------------------------------------------------  


![image](https://github.com/OuO333333/paper/assets/37506309/92f8e685-3841-4b06-9fb8-2abe6bffb340)  
![image](https://github.com/OuO333333/paper/assets/37506309/0abea4ce-1978-4e6b-9941-46b647af62ef)

