a= imread('3.jpg');
r= a(:,:,1);% mengambil nilai matriks red
g= a(:,:,2);%mengambil nilai matriks green
b= a(:,:,3);% mengambil nilai matriks blue

c= 0.3;
h= 0.5;
k= 0.2;
abu= (c*r) + (h*g) +(k*b);% rumus rata rata keabuan
%imshow(abu)
abux=rgb2gray(a);% menggunakan rumus langsung
%imshow(abux);


%TUGAS 1%
  %disp('---------------OPERASI LOGARITMIK------');
  %cons=input('masukan nilai c : ');
  % g1 = cons*log(1+ double(abu));% operasi logaritmik 
  % g1= uint8(g1);% format integer 8 bit
  % subplot (2,2,1);imshow(g1);title(' hasil logaritmik');%menampilkan
   %gambar
   %subplot (2,2,2);imhist(g1);title(' hasil histogram');% menampilkan
   %histogram
  
  %--------------------------TUGAS 2------------------------------------% 
  
  x=80;
  abu1= abu + x;
  abu2 = abu - x;
 %subplot (2,2,1);imshow(abu1);title(' hasil abu1');
  %subplot (2,2,2);imhist(abu1);title(' hasil abu1');
  %subplot (2,1,2);imshow(abu2);title(' hasil abu2');
  %subplot (2,2,2);imhist(abu2);title(' hasil abu2');
  

 
  
  
  	%------------------------------no 3--------------------%
                    sobel1= double(abu1);
                        for w=1:size(sobel1,1)-2
                         for y=1:size(sobel1,2)-2
                         %mencari nilai x-direction (Gx)%
                         Gx=((2*sobel1(w+2,y+1)+sobel1(w+2,y)+sobel1(w+2,y+2))-(2*sobel1(w,y+1)+sobel1(w,y)+sobel1(w,y+2)));
                         %mencari nilai y-direction (Gy)%
                         Gy=((2*sobel1(w+1,y+2)+sobel1(w,y+2)+sobel1(w+2,y+2))-(2*sobel1(w+1,y)+sobel1(w,y)+sobel1(w+2,y)));                       
                     %    abu1(i,j)=sqrt(Gx.^2+Gy.^2);
                        end  
                    end
                    %figure,imshow(abu1); title('Sobel abu1');
   %-------------------------------------------------------------------------------------------------%
                 sobel2= double(abu2);
                     for z=1:size(sobel2,1)-2
                        for w=1:size(sobel2,2)-2
                            %mencari x-direction
                            Gi=((2*sobel2(z+2,w+1)+sobel2(z+2,w)+sobel2(z+2,w+2))-(2*sobel2(z,w+1)+sobel2(z,w)+sobel2(z,w+2)));
                            %mencari y-direction:
                            Gj=((2*sobel2(z+1,w+2)+sobel2(z,w+2)+sobel2(z+2,w+2))-(2*sobel2(z+1,w)+sobel2(z,w)+sobel2(z+2,w)));
                            %mencari gradient m
                            abu2(z,w)=sqrt(Gi.^2+Gj.^2);
     
                        end
                     end
                   figure,imshow(abu2); title('Sobel abu2');

       






