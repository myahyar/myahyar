

int pinPIR = 2;    
int pinRELAY = 4;   
int statusPIR = 0;  

void setup(){
  
pinMode(pinPIR, INPUT);    
pinMode(pinRELAY, OUTPUT);  
Serial.begin(9600);         
}
void loop(){

statusPIR = digitalRead(pinPIR);
if (statusPIR ==HIGH) {

digitalWrite(pinRELAY, LOW);
Serial.println("ADA GERAKAN DELAY 10 DETIK");
delay(500);
}
else {
digitalWrite(pinRELAY, HIGH);
Serial.println("TIDAK ADA GERAKAN");
}
}
