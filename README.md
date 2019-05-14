# Arduino_MEGA_2560_Code

The arduino_code.cpp source code has been written for execution on MESP-A (Arduino MEGA 2560 module).
We include the appropriate libraries, and we initialize the components’ values, such as DHT11 digital
pin, soil temperature pin, GPS, and the serial string (incomingString) which listens to the remote commands 
that we can send to the module. We initialize the sensors to thresholds that are the results over many
experiments. From line 51 to 129 we have built the functions, one function for every sensor, that is responsible 
for the operation of each sensor. For DHT11 we have 2 functions, one for air-temperature and one for humidity. 
On void setup() we initialize the bitrate of the Serial Xbee and the bitrate of the GPS. Finally on void loop() 
we make initialization on the variables that store the values of the executed functions of each sensor. So, 
on every loop the code listens to what sensor returns and if a threshold has been exceeded it takes the decision 
to eliminate the wait period between 2 measurements. We have also included code that listens for commands, such 
as every how many seconds should the Arduino request for measurements over the sensors. Finally, there is input/output 
time curve correction, so that when we give the command to take measurements, for example every 60 sec, to actually 
take measurements, every 60 seconds.
