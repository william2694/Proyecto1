# Proyecto1
package pack;

import giovynet.nativelink.SerialPort;
import giovynet.serial.Baud;
import giovynet.serial.Com;
import giovynet.serial.Parameters;
import gnu.io.CommPortIdentifier;

import java.util.Enumeration;
import java.util.List;

public class puertoSerial {

public static void main(String[] args)throws Exception{

//Definición de parametros
Parameters settings = new Parameters();

//definición del puerto que se va a utilizar
settings.setPort("COM3");

//definición de la velocidad de impresión, se debe tener en cuenta dicho argumento en las especificacion de velocidad del dispositivo

settings.setBaudRate(Baud._9600);

settings.setMinDelayWrite(10);

//asignamos los parametros al objeto com1
Com com1 = new Com(settings);

//envio de cadena de caracteres



for(int i = 1, j = 0; j < 100000; j++) {
	String entradaCom = com1.receiveSingleString();
	System.out.print(entradaCom);
	if (entradaCom==","){
		System.out.println(",");
		
}
}

     }
}
