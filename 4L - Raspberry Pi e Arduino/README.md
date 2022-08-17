# Raspberry Pi e Arduino

  O dispositivo central do laboratório remoto é o “computador embarcado (CE)”, no caso o 
Raspberry Pi 3B+ que tem como principal função intermediar os acessos aos demais dispositivos 
de hardware dos experimentos via rede. O Raspberry Pi 3B+ é um pequeno computador “single board” baseado no processador Broadcom BCM2837B0, Cortex-A53, de 64-bits com quatro 
núcleos e clock de 1.4GHz. Dispõe de memória RAM de 1GB, do tipo LPDDR2 SDRAM e um cartão 
micro SD de 16GB, além de outras funcionalidades e roda sob o sistema operacional Linux 
(Debian). 
***
  O “computador embarcado” tem função prover interfaceamento e gerenciamento para a 
conexão entre a rede (web) e o Arduino3 Uno. O Arduino Uno é uma placa de microcontrolador 
baseado no ATmega328. Ele tem 14 pinos de entrada/saída digital (dos quais 6 podem ser usados 
como saídas PWM), 6 entradas analógicas, um cristal oscilador de 16MHz, uma conexão USB, 
uma entrada de alimentação uma conexão ICSP e um botão de reset. O CE acessa o Arduino Uno 
para a coletar os dados dos sensores ou para enviar comandos para os atuadores, essa 
comunicação é feita via porta UART (universal asynchronous receiver/transmitter) que se 
comunica via protocolo MODBUS4.
***
Os itens de hardware disponíveis, além da placa Arduino Uno, são os seguintes:
 1. Cooler;
2. Sensor de Temperatura LM35;
3. Sensor de Temperatura e Umidade - DHT11;
4. Módulo sensor de luminosidade;
5. Fita LED RGB;
6. LED Vermelho 5mm;
7. LED Azul 5mm;
8. LED Azul 5mm;
9. LED Azul 5mm;
10. LED Azul 5mm;
11. LED Azul 5mm;
12. LED Branco 5mm;
13. LED Branco 10mm;
14. LED Branco 10mm;
15. LED Branco 10mm;
16. LED Branco 10mm;
17. LED Branco 10mm;
18. Relé;
