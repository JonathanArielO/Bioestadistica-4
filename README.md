# Bioestadistica-4
### dado<-1:6
### dado
### prob<-1/6
### prob
### esp_dado<-sum(dado*prob)
### esp_dado
### (1+2+3+4+5+6)/6
  
### lanzamientos<-1:50
### lanzamientos
### dbinom<-dbinom(lanzamientos,size=50,prob=0.55)
### dbinom
### plot(dbinom,col="red",pch=16,ylab="Probabilidad",xlab="Intentos",main="Efectividad de LeBron James")
### pbinom<-pbinom(lanzamientos,size=50,prob=0.55)
### pbinom
### plot(pbinom,col=rainbow(50,start=0.6,end=1),pch=16,ylab="Probabilidad",xlab="Intentos",main="Efectividad de LeBron James")
### producto<-lanzamientos*dbinom
### producto
### LeBron<-data.frame(lanzamientos,dbinom,producto)
### LeBron
### Esp_LeBron<-sum(LeBron$producto)
### Esp_LeBron
### puntos_10partidos<-c(29,24,22,34,29,18,16,33,57,26)
### puntos_10partidos
### x<-1:10
### x
### plot(x,puntos_10partidos,col="blue",pch=16,main="Puntos de LeBron primeros 10 partidos",xlab="Partidos jugados",ylab="Puntos convertidos",xaxt="n")
### axis(1,at=seq(1,10,by=1),las=1
 
### segments(x0=x, y0=27.5, x1=x, y1=puntos_10partidos,col="blue",lwd=2)
### abline(h=27.5,col="red",lwd=2)
### prob_10partidos<-1/10
### prob_10partidos
### tabla_varianza<-data.frame(prob_10partidos,puntos_10partidos,Esp_LeBron)
### tabla_varianza
### varianza_LeBron<-sum(((puntos_10partidos-Esp_LeBron)^2)*prob_10partidos)
### varianza_LeBron
### desviacion_LeBron<-sqrt(varianza_LeBron)
### desviacion_LeBron
### plot(x,puntos_10partidos,col="blue",pch=16,main="Puntos de LeBron primeros 10 partidos",xlab="Partidos jugados",ylab="Puntos convertidos",xaxt="n")
### axis(1,at=seq(1,10,by=1),las=1)
### ### segments(x0=x,y0=27.5,x1=x,y1=puntos_10partidos,col="blue",lwd=2)
### abline(h=27.5,col="red",lwd=2)
### par(new=TRUE)
### rect(0.5,16.47956,10.5,38.52044,col=rgb(0,0,1.0,alpha=0.2))

## Indica ubicación
### getwd()
## Cambiar ubicación
### setwd("C:/Users/Laboratorio/Downloads")
## Indica los archivos de la carpeta
### list.files()
### ### data<-read.csv("IQ.csv",header=TRUE,sep=";")
### data
### names(data)
### head(data)
### tail(data)
### dim(data)

### Mujeres<-data$sexo=="Mujer"
### Mujeres
### data$MRI[Mujeres]
### mean(data$MRI[Mujeres])
### Hombres<-data$sexo=="Hombre"
### Hombres
### data$MRI[Hombres]
### mean(data$MRI[Hombres])
### meanM<-mean(data$MRI[Mujeres])
### meanM
### diferencia<-(data$MRI[Mujeres]-meanM)
### diferencia
### varianza<-sum(diferencia^2)/(length(data$MRI[Mujeres])-1)
### varianza
### sdMujeres<-sqrt(varianza)
### sdMujeres
### var(data$MRI[Mujeres])
### sd(data$MRI[Mujeres])
### var(data$MRI[Hombres])
### sd(data$MRI[Hombres])
### cvM<-sd(data$MRI[Mujeres])/mean(data$MRI[Mujeres])
### cvM
### cvH<-sd(data$MRI[Hombres])/mean(data$MRI[Hombres])
### cvH
### promedio_MRI<-tapply(data$MRI,data$sexo,mean)
### promedio_MRI
### sd_MRI<-tapply(data$MRI,data$sexo,sd)
### sd_MRI
### boxplot(data$MRI~data$sexo,ylab="MRI")
### boxplot(data$FSIQ~data$sexo,ylab="Puntaje FSIQ")
