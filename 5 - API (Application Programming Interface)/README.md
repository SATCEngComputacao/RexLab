## API (Application Programming Interface)  
As funcionalidades para disponibilizar os experimentos na internet estão baseadas em placas “Single board Computers” (SBC). Dentro das perspectivas do projeto, essas são soluções de baixo custo que estão em instituições que pesquisam e desenvolvem laboratórios remotos. Em relação à arquitetura de serviço proposta, a aplicação de cada laboratório remoto é executada em um hardware de baixo custo e de processamento reduzido, se comparado com máquinas comumente utilizadas, como servidores e microservidores web. Além disso, os componentes desse serviço são suficientemente leves para construir uma aplicação de back-end leve o suficiente para ser executada por um computador embarcado Raspberry Pi ou outros dispositivos de baixo custo (SBC ARM ou máquinas antigas).  

Nessa placa é embarcada a API desenvolvida pelo RExLab. Essa aplicação oferece uma interface aos sensores e atuadores na estrutura de um serviço web utilizando protocolos de alto desempenho, enquanto o sistema RELLE é responsável pela interface (UI) e outros serviços intrínsecos aos usuários. A aplicação não requer alto uso da memória e pode ser utilizada em qualquer sistema Linux. O desenvolvimento foi baseado no sistema Linux e, então, compilado para dispositivos Raspberry Pi (utilizando compilador cruzado).  

O resultado é uma arquitetura fracamente acoplada, adotada pelo RExLab, que habilita o compartilhamento dos experimentos em outras plataformas, como de demais laboratórios na nossa. Esse paradigma, chamado de Smart Devices ,vide Figura 3, já é utilizado no projeto Go-Lab  (Global Online Science Labs for Inquiry Learning at School),no qual estão bem destacadas aplicações clientes e servidor, e fornecem interfaces bem definidas entre o usuário e o sistema.  
  
  Figura 3 - UML Component diagram of the interactions between different GoLab services and the Smart Device.   
![image](https://user-images.githubusercontent.com/110925995/185224178-5803f295-74a1-40e4-ac16-cbcc3ab78adb.png)  

As seções seguintes apresentam com mais detalhes aspectos do serviço web utilizado no servidor de experimento, bem como as funcionalidades internas e as motivações para o uso de certos protocolos, padrões e ferramentas de desenvolvimento, conforme a Figura 4.  
  
  Figura 4 - Esquema de aplicação embarcada.  
  ![image](https://user-images.githubusercontent.com/110925995/185225067-57d81f26-a24f-48c2-828b-d01026bd2b87.png)

