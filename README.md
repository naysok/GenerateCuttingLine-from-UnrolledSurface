# GenerateCuttingLine-from-UnrolledSurface  

こういうやつの展開図の、レーザー加工用の切り取り線をつくる。  

![photo](photo/Assemble-04.jpg)  

![photo](photo/Script.png)  



---  


###  how to use  

##### (1) ローポリ風の PolySurface を用意する  

Mesh の場合は、MeshToNURBS で、PolySurface に変換。  

![photo](photo/Mesh.jpg)  



##### (2) Unroll し、展開する  

Unroll のときの設定はこれとか  
分解は、各三角形ごとにばらばらにする。  
番号は、各辺の対応のナンバリング。組立てに必要  

![photo](photo/Unroll-01.jpg)  

結果  
ここで、数字のテキストドットと、サーフェイスがグループ化されているので、Ungroup しておく。  

![photo](photo/Unroll-02.jpg)  



##### (3) grasshopper に、サーフェスの取り込み  

SelSrf などで、サーフェスをすべて選んで、Input Surface のコンポーネントに入れる  
コンポーネントを右クリックで、Set Multiple Surfaces  



##### (4) パラメータの調整  

grasshopper 左側の緑の丸の所だけ調整すれば、ok  

Offset : のりしろの幅  
Tab : 切り残しの大きさ、切り落とすとばらばらになって、ナンバリングした意味がなくなる  
DottedLine : 点線の細かさ  

※　折り線をカッターの背で軽く傷つけて綺麗に折るみたいなものを、レーザーの強弱を調整して折り線にするのは怖かったので、点線にした。  

![photo](photo/Parameter.jpg)  

切り残しを手でちぎる。  

![photo](photo/Assemble-01.jpg)  



##### (5) Bake

Bake して、ライノ上の線のデータにする  
紙の大きさに合わせて並び替え等して、イラレ形式で書き出し、レーザー裁断、ナンバリングした 3D や、展開図を見て組立てる。

![photo](photo/CuttingLine.jpg)  


---  


### Assemble  

組立ての様子。  
A3x2枚分の紙空切り抜いた200ピースで、5-6時間くらい  
凹か凸か気にしながら進めるのが難しかった  

171125  

![photo](photo/Assemble-02.jpg)  

![photo](photo/Assemble-03.jpg)  

![photo](photo/Assemble-04.jpg)  

---  
