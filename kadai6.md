#課題6 レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像をカラー画像からモノクロ画像に変換し画面に表示する．  
表示した画像を図1に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai6-1.png)  
図1 原画像  

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，閾値128とした2値画像に変換し画面に表示する．  
表示した画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai6-2.png)  
図2 閾値128の2値画像  

次にディザ法により2値画像に変換する．  

IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，ディザ法を用いて2値画像に変換し，表示する．  
表示した画像を図3に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai6-3.png)  
図3 ディザ法による2値画像  

図2，3より閾値128としたものよりディザ法を用いたものの方がより原画像を再現していることがわかる．  
