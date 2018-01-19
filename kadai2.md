# 課題2レポート

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって，原画像を差し込み，元がカラー画像であるためモノクロ画像へ変換した．表示された画像を図1に示す．    

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai2-1.png)  
図１　原画像  


IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  

生成した2階調画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai2-2.png)  
図2 2階調画像  

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;   

生成した4階調画像を図3に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai2-3.png)  
図3 4階調画像  

8階調画像は，  

IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>128;  
IMG3 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2 + IMG3;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  

生成した8階調画像を図4に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai2-4.png)  
図4 8階調画像  

生成した画像を見るとわかるように，階調数が上がるごとに元のモノクロ画像に近づいている．  
