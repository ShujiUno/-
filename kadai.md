# 課題１レポート

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); %　原画像の入力  
imagesc(ORG); axis image;　%　画像の表示  

によって，原画像を差し込んだ．表示結果を図１に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai1-1.png)  
図１　原画像  

原画像を1/2サンプリングするためには，画像を1/2倍の縮小した後，2倍に拡大すればよい．なお，拡大するために「box」オプションを設定する．  

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2.0); % 画像の拡大  

1/2サンプリングの結果を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai1-2.png)  
図2 1/2サンプリング  

同様に原画像を1/4サンプリングするには、画像を1/2の縮小した後、2倍に拡大すればよい．すなわち，　　

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2.0); % 画像の拡大  

とする．1/4サンプリングの結果を図3に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai1-3.png)  
図3 1/4サンプリング  

1/8から1/32サンプリングは，

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

を繰り返す．サンプリングの結果を図４～６に示す．

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai1-4.png)  
図4 1/8サンプリング

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai1-5.png)  
図5 1/16サンプリング

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai1-6.png)  
図6 1/32サンプリング

このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪みが発生する．
