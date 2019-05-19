#coding:utf-8
from PIL import Image
import os
path="F:\iPhone music\IphonePhoto\OurLife"
canvasImage=Image.new('RGBA',(2000,1000))
ncol=20
nrow=10
proposal=[0,1,2,3,4,5,9,17,1+1*ncol,8+1*ncol,10+1*ncol, 16+1*ncol,18+1*ncol,1+2*ncol,11+2*ncol,15+2*ncol,
          19+2*ncol,1+3*ncol,     12+3*ncol,15+3*ncol,19+3*ncol,
          2+4*ncol,12+4*ncol,     15+4*ncol,19+4*ncol,3+5*ncol,
          11+5*ncol,15+5*ncol,    19+5*ncol,4+6*ncol,10+6*ncol,
          15+6*ncol,19+6*ncol,    3+7*ncol,9+7*ncol,
          15+7*ncol,19+7*ncol,    2+8*ncol,8+8*ncol,
          16+8*ncol,18+8*ncol,    1+9*ncol,8+9*ncol,
          9+9*ncol,10+9*ncol,     11+9*ncol,12+9*ncol,
          17+9*ncol]
listPic=[]
for i in os.walk(path):
      listPic.append(i)
k=0
for j in range(1, 1000):
    if j in proposal:
        orgImage = Image.open(os.path.join(path,listPic[0][2][k]))
        print(orgImage)
        canvasRow = j % 20;
        canvasCol = int((j - canvasRow) / 20);
        print(canvasRow)
        print(canvasCol)
        print()
        orgImage = orgImage.resize((100, 100), Image.ANTIALIAS)
        canvasImage.paste(orgImage, (canvasRow * 100, canvasCol * 100))
        k=k+1
canvasImage.save('F:/Our520.bmp')
