画图设置`%matplotlib inline`

事实上这个命令是`%matplotlib`, inline是它的参数,这条命令的作用是指定`%matplotlib`输出图像的环境,最常用的就是inline,让它内嵌在notebook中显示,同时也可以有别的,比如 `%matplotlib osx`(注意看平台,像osx明显是mac专属,gtk需要windows下gtk环境,wx也需要wx环境),qt,tk,inline,notebook应该是可以放心使用的),一般inline足够好了

%matplotlib --list

%matplotlib inline

import pylab as pl
pl.seed(1)
data = pl.randn(100)
pl.plot(data);


可以配合 `%config InlineBackend.figure_format="svg"`做图片输出格式的设置

%config InlineBackend.figure_format="svg"
%matplotlib inline

pl.plot(data);