## Módulo sensor de luminosidade  

Figura 15 – Sensor de Luminosidade 

![image](https://user-images.githubusercontent.com/110925995/185233295-badc92c5-6b2d-44cd-b306-158e00709422.png)  

O Sensor de Luminosidade ldr (Figura 15) integra um fotorresistor GL5528 para detectar a intensidade da luz. A resistência do fotorresistor (resistor dependente da luz) diminui quando a intensidade da luz aumenta.   

![image](https://user-images.githubusercontent.com/110925995/185233706-a6ddb921-2094-4a39-ae6c-2b0766f9b91d.png)  

![image](https://user-images.githubusercontent.com/110925995/185233875-529ed6c1-c8f0-43e4-adec-f133d92c6a6f.png)  

Um chip comparador duplo LM393 embarcado produz voltagem correspondente à intensidade da luz (ou seja, com base no valor de resistência). A sensibilidade pode ser alterada por um potenciômetro embarcado no módulo. O sinal de saída é um valor analógico, quanto mais brilhante for a luz, maior será o valor.   

Figura 16 – Diagrama esquemático

![image](https://user-images.githubusercontent.com/110925995/185234240-c1072d4e-85e1-4144-9861-33fa7ed000d8.png)  

Quadro x: Especificações  
Item	Valor  
Tensão de operação	3\~5V  
Corrente de operação	0.5~3 mA  
Tempo de resposta	20-30 millisegundos  
Comprimento de onda máximo	540 nm  
Resistência à luz	20KΩ  
Resistência sem escura  	
Foto-resistor	GL5528(datasheet)  

A Figura 16 mostra a conexão do módulo sensor de luminosidade na base shield  

![image](https://user-images.githubusercontent.com/110925995/185235568-9e0c390e-a0fb-4c32-b570-4a26e79cef46.png)  

Exemplo de código:  

![image](https://user-images.githubusercontent.com/110925995/185235747-52c1157e-8c4d-429e-8300-4748bdb5e1b2.png)  

Exemplo de código no Block ino:  

![image](https://user-images.githubusercontent.com/110925995/185236005-febffa17-bec6-4d3a-900b-92449ee77557.png)

