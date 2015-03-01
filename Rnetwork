## Network to show Number of Shared Plotlines in TV Show 'Friends'
## Alex Albright--based on code by Katie Choi for Supreme Court Justices Dissent Network (2003)

## Creates an adjacency matrix for a fully connected network
Chandler<-c(0,1,1,1,1,1)
Joey<-c(1,0,1,1,1,1)
Monica<-c(1,1,0,1,1,1)
Phoebe<-c(1,1,1,0,1,1)
Rachel<-c(1,1,1,1,0,1)
Ross<-c(1,1,1,1,1,0)
adjmat<-rbind(Chandler,Joey,Monica,Phoebe,Rachel,Ross)

## Check to see if the matrix was formed
class(adjmat)

## Load the network package
library(network)

## Creates the network
friendship<-network(adjmat,matrix.type='adjacency',directed=FALSE, vertex.size=vertex.size*2)
#see vertex size above

## Creates the labels for the vertices
friends<-c("Chandler","Joey","Monica","Phoebe","Rachel","Ross")

## Creates a matrix of number of plotlines shared with each character 
ChandlerW<-c(0,69,94,16,20,25)
JoeyW<-c(69,0,27,28,40,26)
MonicaW<-c(94,27,0,40,33,12)
PhoebeW<-c(16,28,40,0,35,20)
RachelW<-c(20,40,33,35,0,81)
RossW<-c(25,26,12,20,81,0)
weights<-rbind(ChandlerW,JoeyW,MonicaW,PhoebeW,RachelW,RossW)

## Check to see if the matrix was formed
class(weights)

ChandlerC<-replace(ChandlerW,ChandlerW<=20,"black")
ChandlerC<-replace(ChandlerC,ChandlerC>20&ChandlerC<=35,"slateblue2")
ChandlerC<-replace(ChandlerC,ChandlerC>35&ChandlerC<=50,"azure3")
ChandlerC<-replace(ChandlerC,ChandlerC>50&ChandlerC<=94,"red")
JoeyC<-replace(JoeyW,JoeyW<=20,"black")
JoeyC<-replace(JoeyC,JoeyC>20&JoeyC<=35,"slateblue2")
JoeyC<-replace(JoeyC,JoeyC>35&JoeyC<=50,"azure3")
JoeyC<-replace(JoeyC,JoeyC>50&JoeyC<=94,"red")
MonicaC<-replace(MonicaW,MonicaW<=20,"black")
MonicaC<-replace(MonicaC,MonicaC>20&MonicaC<=35,"slateblue2")
MonicaC<-replace(MonicaC,MonicaC>35&MonicaC<=50,"azure3")
MonicaC<-replace(MonicaC,MonicaC>50&MonicaC<=94,"red")
PhoebeC<-replace(PhoebeW,PhoebeW<=20,"black")
PhoebeC<-replace(PhoebeC,PhoebeC>20&PhoebeC<=35,"slateblue2")
PhoebeC<-replace(PhoebeC,PhoebeC>35&PhoebeC<=50,"azure3")
PhoebeC <-replace(PhoebeC,PhoebeC>50&PhoebeC<=94,"red")
RachelC<-replace(RachelW,RachelW<=20,"black")
RachelC<-replace(RachelC,RachelC>20&RachelC<=35,"slateblue2")
RachelC<-replace(RachelC,RachelC>35&RachelC<=50,"azure3")
RachelC<-replace(RachelC,RachelC>50&RachelC<=94,"red")
RossC<-replace(RossW,RossW<=20,"black")
RossC<-replace(RossC,RossC>20&RossC<=35,"slateblue2")
RossC<-replace(RossC,RossC>35&RossC<=50,"azure3")
RossC<-replace(RossC,RossC>50&RossC<=94,"red")
edgecolors<-rbind(ChandlerC,JoeyC,MonicaC,PhoebeC,RachelC,RossC)

## Check to see if matrix was formed
class(edgecolors)

## reduce thickness of the line by a factor to make it easier to read 
weights<-weights*.5

## Create a color vector for the vertices: red for girl, blue for boy
vertexcolors<-c("turquoise2","turquoise2","yellow","yellow","yellow","turquoise2")

#verts<-(7,7,7,7,7,7)

## Plot the network without colored edges or vertices
plot.network(friendship,edge.lwd=weights,label=friends)

## Plot the network with colored edges but not vertices
plot.network(friendship,edge.col=edgecolors,edge.lwd=weights,label=friends)

## Plot the network with colored edges and vertices
plot.network(friendship,edge.col=edgecolors,vertex.col=vertexcolors,edge.lwd=weights,label=friends)
#plot.network(friendship,edge.col=edgecolors,vertex.col=vertexcolors,edge.lwd=weights,label=friends, vertex.size=verts)
title(main="'Friends' Network")
#text(locator(1), "Colors specify number of shared plotlines such that Black<=20<Blue<=35<Gray<=50<Red<=94")
#text(locator(1), "Density of edges corresponds to number of shared plotlines as well")
mtext("Edges Weighted by Number of Shared Plotlines",3)
mtext(

"Edge Coloring: Black [0,20]; Purple (20,35]; Gray (35,50]; Red (50,94]
Vertex Coloring: Yellow for Female Characters; Blue for Male Characters",1)
