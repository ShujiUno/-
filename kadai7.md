#課題7 レポート  


標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG = imread('milkdrop.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を差し込みカラー画像からモノクロ画像に変換し画面に表示する．  
表示した画像を図1に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai7-1.png)  
図1 原画像  

始めに原画像の画素のダイナミックレンジを表示する．  

imhist(ORG); % 濃度ヒストグラムを生成、表示  

によって濃度ヒストグラムを生成し表示する．　　
表示した画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai7-2.png)  
図2 原画像の濃度ヒストグラム  

次に，この原画像の画素のダイナミックレンジを0から255に変換し，変換した画像を表示する．

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像の画素のダイナミックレンジを変換し画像を表示する．  
表示した画像を図3に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai7-3.png)  
図3 ダイナミックレンジを変換した画像  

次に，変換した画像の濃度ヒストグラムを表示する．  

ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  

によって濃度ヒストグラムを表示する．  
表示した濃度ヒストグラムを図4に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai7-4.png)  
図4 ダイナミックレンジを変換した画像の濃度ヒストグラム  
