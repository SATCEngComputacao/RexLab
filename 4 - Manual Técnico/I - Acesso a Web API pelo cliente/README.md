## Acesso a Web API pelo cliente  
**A Erro! Fonte de referência não encontrada**. 5 apresenta o esquema de comunicação no uso da API desenvolvido para o serviço/protótipo.    
  
  Figura 5 - Esquema de comunicação cross domain no uso da API desenvolvida pelo RExLab  
    
 ![image](https://user-images.githubusercontent.com/110925995/185228318-80d09b92-eeee-4d72-9494-b944a9f31dd0.png) 
 
 O cliente web disponibilizado pelo sistema RELLE é composto por um arquivo html, css e javascript diferentes para cada experimento. O RELLE provê uma página comum para cada experimento onde carrega os dados que foram inseridos no momento da publicação do experimento (armazenados numa base de dados). Por exemplo, o experimento de ID 1 é acessível pela URL “relle.ufsc.br/labs/1” pelo método GET e contém suas informações dentro do layout padrão do sistema. A partir do botão “Acessar” é possível disparar um evento para comunicação com a Web API FCFS (First-come first served).  
 
Ao obter a permissão no navegador, o cliente navegador poderá carregar os arquivos (html, css e js), pois a API já tem o seu token de sessão como usuário sendo servido.  Após carregar o cliente para o Smart Device (client.js), uma conexão WebSocket com este dispositivo é estabelecida. 

