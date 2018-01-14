# 課題１レポート

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); %　原画像の入力  
imagesc(ORG); axis image;　%　画像の表示  

によって，原画像を差し込んだ．表示結果を図１に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/milkdrop.jpg)  
図１　原画像  

原画像を1/2サンプリングするためには，画像を1/2倍の縮小した後，2倍に拡大すればよい．なお，拡大するために「box」オプションを設定する．  

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2.0); % 画像の拡大  

1/2サンプリングの結果を図2に示す．  

