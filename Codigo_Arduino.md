# Proyecto1

void setup(){
Serial.begin(9600);
}

void loop(){
//Serial.print(millis());
//Serial.print(",");
Serial.flush();
int sensorValue=analogRead(A0);
//Serial.print(",");
Serial.println(sensorValue);


//if (Srial.available() > 0) {
//  int  dat = Serial.read();
//  }
}
