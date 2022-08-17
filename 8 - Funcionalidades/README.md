## FUNCIONALIDADES  

Os Smart Devices desenvolvidos são capazes de comunicar-se com sensores através do barramento serial (Porta UART). Ao invés de usar o protocolo serial em sua forma bruta, optamos por incluir o protocolo Modbus na camada de aplicação para identificação de erros, endereçamento e controle de colisão. Conectados ao mesmo barramento (rede), cada sistema embarcado, responsável por um ou mais sensores ou atuadores, é um dispositivo escravo que responde às requisições da aplicação que é executada no Raspberry Pi.  

A descrição do serviço por metadados permite a descoberta de serviços pelo cliente, incluindo tipos de parâmetros, valores aceitos, unidades de medidas, etc. Tão importante quanto descrever os recursos internos ao experimento é validar as entradas fornecidas pelo usuário e observar e agir sobre estados internos que representam situações de risco, tal como: verificar a faixa de intervalos de tempo para manter a fonte de calor ligada e temperatura máxima lida em qualquer termômetro, respectivamente.  

Além do sistema de fila realizar a gerência da conexão do usuário com polling HTTP, a aplicação do experimento também reconhece a saída ou perda de conexão de um usuário. Os parâmetros desse mecanismo, também chamado de mensagens hearbeat, são ajustáveis pelo administrador do sistema (parâmetros timeout e interval). A aplicação contém um objeto que descreve os comportamentos e atributos de um experimento, ou seja, o modelo de um experimento. Ao identificar a saída de um usuário, esse objeto é responsável por restaurar a configuração inicial, quando possível.  

Um dos módulos desenvolvidos para aplicação é responsável pelo serviço de fila externo ou interno, sendo possível acoplar o serviço de fila provido pelo RELLE ou habilitar serviços internos.  

No primeiro caso, a aplicação usa a lógica necessária para validação de token de sessão enviado pelo cliente. Na segunda, todo processo realizado pela web API de fila é realizado pelo Smart Device.  
  
Outra funcionalidade é a página de testes, uma página HTML com informações sobre sensores e entradas para ser utilizada em depuração e manutenção. Fora da aplicação contamos com um script para inicialização da aplicação como serviço Linux para manter o processo ativo e facilmente gerenciável.   

