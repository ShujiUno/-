#課題5 レポート  

標準画像「milkdrop」を原画像とした．この画像は縦150画像，横150画像による正方形のディジタルカラー画像である．  

ORG=imread('milkdrop.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって，原画像をカラー画像からモノクロ画像に変換し，画面に表示させる．  
表示させた画像を図1に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai5-1.png)  
図1 原画像  

判別分析法を用いてこの原画像を2値画像に変換する．  

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納  
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end  
end  

IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;  

によって，判別分析法を実現させ，2値画像に変換し表示する．  
表示した画像を図2に示す．  

![原画像](https://github.com/ShujiUno/kadai/blob/master/image/kadai5-2.png)  
図2 判別分析法を用いて変換した2値画像  


