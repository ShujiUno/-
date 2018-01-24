#課題8 レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG = imread('milkdrop.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって原画像を差し込み，カラー画像からモノクロ画像に変換し画面に表示する．  
表示した画像を図1に示す．　　

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai9-1.png)  
図1 原画像  

次に，原画像にノイズを付与する．  

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって原画像にノイズを付与する．  
ノイズを付与した画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai9-2.png)　　
図2 ノイズを付与した原画像  


次に，平滑フィルタを用いてノイズを除去する．  

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって，平滑フィルタを用いてノイズを除去する．  
平滑フィルタを用いてノイズを除去した画像を図3に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai9-3.png)    
図3 平滑フィルタによるノイズ除去  


次に，メディアンフィルタを用いてノイズを除去する．  

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によってメディアンフィルタを用いてノイズを除去する．  
メディアンフィルタを用いてノイズを除去した画像を図4に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai9-4.png)  
図4 メディアンフィルタによるノイズ除去  
