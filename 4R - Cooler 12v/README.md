## Cooler 12v

O cooler 30mm tem acionamento DC e como tensão 12v, sendo ideal para baixar temperaturas.  

![image 1](https://user-images.githubusercontent.com/90244580/185233142-72f85abc-81f2-492b-adb5-df98285509b8.png)  

O Arduino e o Raspberry trabalham com 5v, já o cooler trabalha com 12, então foi necessário o uso de um transistor(tip122) e de um conversor de tensão (cn6009 step up) para que ficasse possível o uso do cooler em sua tensão correta.  
![image 2](https://user-images.githubusercontent.com/90244580/185233242-bceeb1ba-4922-435d-a8c7-431fa9fa1442.png)  
![image 3](https://user-images.githubusercontent.com/90244580/185233286-731d84b6-351f-46b7-8dd1-1d99fc3ead37.png)  
![image 4](https://user-images.githubusercontent.com/90244580/185233318-e411288f-f7a7-41bc-9704-e71d8da49bfd.png)  

GND deve estar conectado ao mesmo gnd da fonte externa e do microcontrolador.  

Exemplo de código:  
![image 5](https://user-images.githubusercontent.com/90244580/185233452-0821f5b7-3a59-40ad-ad61-97239859cba9.png)  

Exemplo de código no BLOCKINO:  
![image 6](https://user-images.githubusercontent.com/90244580/185233581-7f86db7a-bb2d-4fd7-a0f4-b56fcbd9e357.png)  
