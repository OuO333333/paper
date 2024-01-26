# Y<sub>k</sub> = W<sub>k</sub><sup>H</sup>H<sub>k</sub>F<sub>k</sub>X<sub>k</sub> + Ñ<sub>k</sub>
K: OFDM 的子載波數  
M<sub>T</sub>: 發送端形成信號的波束數  
M<sub>R</sub>: 接收端形成信號的波束數  
N<sub>T</sub>: 發射端的天線數量  
N<sub>R</sub>: 接收端的天線數量  
N<sub>T</sub><sup>RF</sup>: 發射端的 RF 數量  
N<sub>R</sub><sup>RF</sup>: 接收端的 RF 數量  
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
  
在發送端, X<sub>k</sub> 總共有 M<sub>T</sub> 個波束, 每個波束只使用一個 RF  
在接收端, 用 M<sub>R</sub> 個波束來取得 1 個發送端的波束, 而接收端有 N<sub>R</sub><sup>RF</sup> 個 RF,  
因此處理 1 個發送端的波束需要使用 channel M<sub>R</sub> / N<sub>R</sub><sup>RF</sup> 次,  
處理整個 X<sub>k</sub> 需要使用 channel M<sub>T</sub> * M<sub>R</sub> / N<sub>R</sub><sup>RF</sup> 次
  
-------------------------------------------------------------  
  
![image](https://github.com/OuO333333/paper/assets/37506309/92f8e685-3841-4b06-9fb8-2abe6bffb340)  
![image](https://github.com/OuO333333/paper/assets/37506309/0abea4ce-1978-4e6b-9941-46b647af62ef)
  
-------------------------------------------------------------  

Y<sub>k</sub> = √P * W<sup>H</sup>H<sub>k</sub>F + Ñ<sub>k</sub>  
R<sub>k</sub> = G<sub>L</sub>Y<sub>k</sub>G<sub>R</sub> = √P * G<sub>L</sub>W<sup>H</sup>H<sub>k</sub>FG<sub>R</sub> + G<sub>L</sub>Ñ<sub>k</sub>G<sub>R</sub>  
![image](https://github.com/OuO333333/paper/assets/37506309/c90f8e3e-2e8a-4462-a8e4-2e124923974c)  
M<sub>R</sub> ≥ N<sub>R</sub>, M<sub>T</sub> ≥ N<sub>T</sub>, 比較好懂, 就是分別消掉 W<sup>H</sup> 跟 F。  
M<sub>R</sub> < N<sub>R</sub>, M<sub>T</sub> < N<sub>T</sub>, 就不懂了。  
  
-------------------------------------------------------------  

看起來是先初步估計出 R<sub>k<sub>0</sub></sub>, R<sub>k<sub>1</sub></sub> 當 input, 目標求出 output H<sub>k<sub>0</sub></sub>, H<sub>k<sub>1</sub></sub>。  
然後再用 H求出原本的 X<sub>k<sub>0</sub></sub>, X<sub>k<sub>1</sub></sub>。
