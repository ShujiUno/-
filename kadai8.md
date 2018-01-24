#課題8 レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG = imread('milkdrop.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって原画像を読み込み，カラー画像からモノクロ画像に変換し画面に表示する．  
表示した画像を図1に示す.  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai8-1.png)  
図1　原画像  

次に，閾値128で原画像を2値化する．  

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を閾値128の2値画像に変換し画面に表示する．  
表示した画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai8-2.png)  
図2 閾値128の2値画像  

次に，この2値画像の各連結成分ごとにラベリングを行う．

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  

によって，ラベリングを行い画面に表示する．  
IMG = bwlabeln(IMG) で2値画像のラベリングを行う．  
ラベリングされた画像を図3に示す．

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai8-3.png)  
図3   ラベリングされた画像  

図3より，各連結成分ごとにラベリング(色付け)されていることがわかる．  
