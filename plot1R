consumption  = read.table("household_power_consumption.txt", sep=";", header=TRUE, stringsAsFactors=FALSE)

needed_data_1_2 = subset(consumption, 
  as.Date(consumption$Date,format="%d/%m/%Y") == "2007-02-01" | 
  as.Date(consumption$Date,format="%d/%m/%Y") == "2007-02-02"
  )



needed_data_1_2$datetime <- strptime(paste(needed_data_1_2$Date, needed_data_1_2$Time), 
format="%d/%m/%Y %H:%M:%S", tz="CST6CDT")
needed_data_1_2$Date = as.Date(needed_data_1_2$Date,format="%d/%m/%Y")
needed_data_1_2$Global_active_power = as.numeric(needed_data_1_2$Global_active_power)
needed_data_1_2$Global_reactive_power = as.numeric(needed_data_1_2$Global_reactive_power)
needed_data_1_2$Voltage = as.numeric(needed_data_1_2$Voltage)
needed_data_1_2$Global_intensity = as.numeric(needed_data_1_2$Global_intensity)
needed_data_1_2$Sub_metering_1 = as.numeric(needed_data_1_2$Sub_metering_1)
needed_data_1_2$Sub_metering_2 = as.numeric(needed_data_1_2$Sub_metering_2)
needed_data_1_2$Sub_metering_3 = as.numeric(needed_data_1_2$Sub_metering_3)


#plot graph 1
hist(needed_data_1_2$Global_active_power,  col="red", main="Global Active Power")
