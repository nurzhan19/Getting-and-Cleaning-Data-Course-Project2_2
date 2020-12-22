# Assingment1
###plot1
library(readxl)
Coursera_Explaratory_data <- read_excel("C:/Users/User/Downloads/Coursera Explaratory data.xlsx")
hist(Coursera_Explaratory_data$Global_active_power,main = "Global Active power",col="red",xlab = "Global Active power(kilowatts")
dev.copy(png,file="plot1.png",height = 480, width = 480)
dev.off




###plot2

library(readxl)
Coursera_Explaratory_data <- read_excel("C:/Users/User/Downloads/Coursera Explaratory data.xlsx")
Coursera_Explaratory_data$datetime <- strptime(paste(Coursera_Explaratory_data$Date, Coursera_Explaratory_data$Time), "%Y-%m-%d %H:%M:%S")
plot(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Global_active_power,type="l",xlab="",ylab="Global Active Power (kilowatts)")

dev.copy(png,file="plot2.png",height = 480, width = 480)
dev.off


###plot3

library(readxl)
Coursera_Explaratory_data <- read_excel("C:/Users/User/Downloads/Coursera Explaratory data.xlsx")
Coursera_Explaratory_data$datetime <- strptime(paste(Coursera_Explaratory_data$Date, Coursera_Explaratory_data$Time), "%Y-%m-%d %H:%M:%S")
plot(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Sub_metering_1,type="l",col="black",xlab = "",ylab = "Energu sub metering")
lines(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Sub_metering_2,col="red")
lines(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Sub_metering_3,col="blue")
legend("topleft", col=c("black", "red", "blue"), lwd=c(1,1,1),
       c("Sub_metering_1", "Sub_metering_2", "Sub_metering_3"))
dev.copy(png,file="plot3.png",height = 480, width = 480)
dev.off



#####plot4
library(readxl)
Coursera_Explaratory_data <- read_excel("C:/Users/User/Downloads/Coursera Explaratory data.xlsx")
Coursera_Explaratory_data$datetime <- strptime(paste(Coursera_Explaratory_data$Date, Coursera_Explaratory_data$Time), "%Y-%m-%d %H:%M:%S")

par(mfrow=c(2,2), mar=c(4,4,2,1), oma=c(0,0,2,0))

plot(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Global_active_power,type="l",xlab="",ylab="Global Active Power (kilowatts)")
plot(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Voltage,type="l",xlab="",ylab="Voltage")
plot(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Sub_metering_1,type="l",col="black",xlab = "",ylab = "Energu sub metering")
lines(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Sub_metering_2,col="red")
lines(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Sub_metering_3,col="blue")
legend("topleft", col=c("black", "red", "blue"), lwd=c(1,1,1),
       c("Sub_metering_1", "Sub_metering_2", "Sub_metering_3"))

plot(Coursera_Explaratory_data$Time,Coursera_Explaratory_data$Global_reactive_power,type="l",xlab = "",ylab = "Global reactive power(kilowatts)")
dev.copy(png,file="plot4.png",height = 480, width = 480)
dev.off
