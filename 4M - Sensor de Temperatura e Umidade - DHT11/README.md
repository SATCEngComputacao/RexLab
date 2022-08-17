## Sensor de Temperatura e Umidade - DHT11  

O módulo sensor de temperatura e umidade DHT11 (Figura 10), fornece uma saída digital pré-calibrada. Um elemento sensor capacitivo exclusivo mede a umidade relativa e a temperatura é medida por um termistor de coeficiente de temperatura negativo (NTC). Possui excelente confiabilidade e estabilidade de longo prazo. Deve-se observar que este sensor não funcionará em temperaturas abaixo de 0 graus.
![image 1](https://user-images.githubusercontent.com/90244580/185216499-5df624de-8ac2-45d0-b74b-6287ba649b3f.png)  
  
A Figura a seguir mostra a conexão do sensor de temperatura/umidade - DHT11 no Arduino:  
![image 2](https://user-images.githubusercontent.com/90244580/185223941-61cabe8c-7666-4528-b4ff-69b62bc661a2.jpg)

#### Características eletrônicas:

Itens | Parâmetro | Min | Max | Unidade
:--- | :---: | :---: | :---: | :---:
VCC | - | 3.3 | 5 | Volts
Média de fornecimento de corrente | - | 1.3 | 2.1 | mA
Média de corrente consumida | - | 0.5 | 1.1 | mA
Faixa de medição | Umidade<br> Temperatura | 90%<br> 0 | RH<br> 50 | 90%<br> °C
Precisão | Umidade<br> Temperatura | | ±5%<br> ±2 | RH<br> °C
Sensibilidade | Umidade<br> Temperatura | | 1%<br> 1 | RH<br> °C
Repetibilidade | Umidade<br> Temperatura | | ±1%<br> ±1 | RH<br> °C

**Exemplo de código DHT11:**

![image 3](https://user-images.githubusercontent.com/90244580/185226105-209c9db7-f8ca-4dcd-85f0-8e241b1505a4.png)  
  
Todo programa de Arduino tem dois métodos:  
  
setup() é usado uma vez, no início do programa – ou seja, quando é recém-instalado no Arduino, o botão de reset é pressionado ou o fornecimento de energia é interrompido. Geralmente, é aqui que os dispositivos são inicializados.  

loop() é usado em um loop contínuo quando a configuração é concluída. É aqui que a lógica de programação real acontece – os dados são recuperados do sensor, o sucesso da recuperação é testado e os dados são transferidos para a interface serial. O atraso no final é de particular importância: é aqui que toda a execução é interrompida por um segundo, para que o console possa ser lido no computador.  

O programa é construído com “sketch” → “verify/compile” para copiá-lo no Arduino. Você também receberá notificações sobre erros de programação e possíveis problemas. É possível que um alerta vermelho apareça na saída de status do Arduino Studio, pois o NAN foi definido recentemente. Isso vem da biblioteca do sensor de temperatura e pode ser ignorado.  

Com “sketch” → “upload”, o programa é escrito no Arduino e é construído automaticamente no processo. Você pode ver a seguinte saída indo em “Tools” → “Serial monitor”:  

![image 4](https://user-images.githubusercontent.com/90244580/185227752-a4e7adcd-3b9b-4b50-99f0-3802e274f6b3.png)  
  
**Exemplo de código no BLOCKINO, lendo a umidade:**  
![image 5](https://user-images.githubusercontent.com/90244580/185227893-e67790a7-f73f-4520-a413-c9b5bd46efa6.png)  