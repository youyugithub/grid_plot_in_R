# grid_plot_in_R
grid plot in R


## mixing grid and base
https://www.codenong.com/14999802/
```
library(grid)
library(gridBase)
plot.new()
vp1 <- viewport(x=0,y=0.5,width=0.5, height=0.5, just = c("left","bottom"))
vp2 <- viewport(x=0.5,y=0,width=0.5, height=0.5, just = c("left","bottom"))
pushViewport(vp1)
grid.rect()
grid.text("vp1", 0.5, 0.5)
par(new=TRUE, fig=gridFIG())
plot(1,2)
upViewport()
pushViewport(vp2)
grid.rect()
grid.text("vp2", 0.5, 0.5)
par(new=TRUE, fig=gridFIG())
plot(1,2)
```
