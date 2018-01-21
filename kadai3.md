# 課題３レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像をカラー画像から白黒画像に変換し画面に表示させる．  
表示させた画像を図1に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai3-1.png)  
図1 原画像  

原画像を閾値を輝度値64とした2値画像にするために，輝度値が64以上の画素を1，その他を0に変換すればよい．  

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  

によって閾値を輝度値64とした2値画像をに変換した．表示した画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai3-2.png)  
図2 閾値64の2値画像  

次に，原画像を閾値を輝度値96とした2値画像に変換する．そのためには，輝度値が96以上の画素を1，その他を0に変換すればよい．  

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  

によって，閾値を輝度値98とした2値画像に変換した．表示した画像を図3に示す．   

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai3-3.png)  
図3　閾値98の2値画像  

次に，原画像を閾値を輝度値128とした2値画像に変換する．よって，輝度値128以上の画素を1，その他を0に変換すればよい．  

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

によって，原画像を閾値を輝度値128とした2値画像に変換した．表示した画像を図4に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai3-4.png)  
図4　閾値128とした2値画像  

次に，原画像を閾値を192とした2値画像に変換する．よって，輝度値192以上の画素を1，その他を0に変換すればよい．  

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  

によって，原画像を閾値を輝度値192とした2値画像に変換した．表示した画像を図5に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai3-5.png)  
図5 閾値192の2値画像  
