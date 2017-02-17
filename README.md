# practica-6 

# descomponer st

# para descomponer una serie de tiempo graficamente se usa una funcion llamada
# decompose

desoc<-sample(3:8,44,replace = T)
tdesoc<-ts(desoc,frequency = 4,start = 2005)
plot(decompose(tdesoc))
plot(tdesoc)
pibm<-read.csv("C:\\Users\\luisa\\OneDrive\\Documentos\\r series de tiempo\\pib.csv")
pibmts<-ts(pibm,frequency = 4,start = 2007)
plot(pibmts)
plot(decompose(pibmts))
View(pibm)
summary(pibmts)
names(pibmts)
dpibmts<-decompose(pibmts)
names(dpibmts)
dpibmts$trend
dpibmts$seasonal

td<-read.csv("C:\\Users\\luisa\\OneDrive\\Documentos\\r series de tiempo\\tarea2.csv")
tdts<-ts(td,frequency = 4,start = 2005)
View(td)
summary(tdts)
names(tdts)
dtdts<-decompose(tdts)
names(dtdts)
dtdts$trend
dtdts$seasonal
dtdts$random
plot(tdts)
plot(decompose(tdts))

# en 2008 hay una caida por la gran depresion debido a la crisis hipotecaria
# existiendo desempleo de mucho personal crediticio

coyun<-read.csv("C:\\Users\\luisa\\OneDrive\\Documentos\\r series de tiempo\\cuadro.csv")
coyunts<-ts( coyun ,frequency = 4,start = 2005)
