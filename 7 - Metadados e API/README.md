# Metados e API


  Os Web services permitem acessar entradas e saídas de dispositivos conectados à internet. 
Funcionalidades referem-se a comportamentos internos como validação da faixa de entrada de 
um atuador ou reconhecimento de situações críticas, como o superaquecimento. Para isso, o GT-MRE elaborou uma especificação detalhada utilizando uma linguagem de descrição baseada em 
JSON (Javascript Object Notation). O compartilhamento dessa especificação permite um 
completo desacoplamento de cliente-servidor, e pretende garantir interoperabilidade e 
integração dos recursos do laboratório em qualquer software cliente.

O formato JSON é utilizado para descrever e trocar conjuntos de dados entre aplicações, 
independente da linguagem em que cada uma foi desenvolvida. Esse padrão foi utilizado para 
representar entradas e saídas de dados. Trazemos o exemplo do laboratório de circuitos 
resistivos DC para ilustrar a descrição deste Smart Device.
