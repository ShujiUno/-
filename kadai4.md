# 課題4 レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG);  % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって原画像をカラー画像からモノクロ画像に変換し表示する．  
表示させた画像を図1に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai4-1.png)  
図1 原画像  

次に，この原画像の画素の濃度ヒストグラムを生成する．  

imhist(ORG); % ヒストグラムの表示  

によって，濃度ヒストグラムを生成する．生成した濃度ヒストグラムを図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai4-2.png)  
図2 濃度ヒストグラム  
