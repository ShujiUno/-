#課題10 レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG = imread('milkdrop.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); %カラーからグレイへの変換  
imagesc(ORG); colormap('gray'); colorbar;% 画像表示  

によって，原画像を差し込み，カラー画像をモノクロ画像に変換し，画面に表示する．  
表示した画像を図1に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai10-1.png)  
図1 原画像  




![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai10-2.png)  
図2 ブレウィット法によるエッジ抽出  



![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai10-3.png)  
図3 ソベル法によるエッジ抽出  




![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai10-4.png)  
図4　キャニー法によるエッジ抽出
