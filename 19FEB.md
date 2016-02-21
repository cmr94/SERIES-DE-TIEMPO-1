# SERIES-DE-TIEMPO
CODIGOS EN R PARA SERIES DE TIEMPO
CLASE 19 DE FEBRERO

#Clase 19 de febrero 

BASE_ENOE1<-subset(BASE_ENOE,CLASE2==1,select=c(EDA, SEX, HRSOCUP, CLASE2, CLASE1, CLASE3, EDA5C, IMSSISSSTE)) 

#GRAFICA DE PIE
frec<-table(BASE_ENOE1$IMSSISSSTE)
pie(frec) #grafica mas sencilla

pie(frec, labels=c("Imss", "Issste", "Otra", "No recibe", "No especificado"))

pie(frec, labels=c("Imss", "Issste", "Otra", "No recibe", "No especificado"), main="Institucion de atencion médica")

pie(frec, labels=c("Imss", "Issste", "Otra", "No recibe", "No especificado"), main="Institucion de atencion médica", col=c("green", "red", "blue", "yellow", "maroon4"))
help(pie)

#GRAFICA DE BARRAS
frec1<-table(BASE_ENOE1$EDA5C)
barplot(frec1)

barplot(frec1,main="Cinco grupos de edad")

barplot(frec1,main="Cinco grupos de edad", col=c("green", "red", "blue", "yellow", "maroon4"), names.arg = c("menor", "14 a 24","25 a 44", "45 a 64", "65 y más", "n.e"))

barplot(frec1,main="Cinco grupos de edad", col=c("green", "red", "blue", "yellow", "maroon4"), names.arg = c("menor", "14 a 24","25 a 44", "45 a 64", "65 y más", "n.e"), ylim =c(0,85000) )

barplot(frec1,main="Cinco grupos de edad", col=c("green", "red", "blue", "yellow", "maroon4"), names.arg = c("menor", "14 a 24","25 a 44", "45 a 64", "65 y más", "n.e"), ylim =c(0,85000), xlab="Edad", ylab="Poblacion",  border = "dark blue", width=2, legend.text =c("menor", "14 a 24","25 a 44", "45 a 64", "65 y más", "n.e"))


#Etiquetar frec1,asi no usamos names.arg
names(frec1)<-c("menor", "14 a 24","25 a 44", "45 a 64", "65 y más", "n.e")
barplot(frec1,main="Cinco grupos de edad", col=c("green", "red", "blue", "yellow", "maroon4"), names.arg = c("menor", "14 a 24","25 a 44", "45 a 64", "65 y más", "n.e"))
help(barplot)
