## APÊNDICE C: CONFIGURAÇÃO DO RASPBERRY PI

Antes de testar o experimento é preciso preparar o SBC com aplicativos e servidores para acesso e controlar os experimentos. Nos experimentos do RexLab é usado o SBC (Single Board Computer) Raspberry PI modelo 3B+. Contudo, outros modelos também podem ser utilizados.

![image](https://user-images.githubusercontent.com/90244580/184411109-c52ad552-0b24-44b6-b170-fbfc9e205aa8.png)  

**Materiais para Preparação no SBC**  

As ferramentas mínimas para preparação do nosso SBC são:  
* Ambiente de trabalho: Computador Desktop PC Intel com Windows 10 x64 com conexão à rede;
* O Raspberry PI instalado e com conexão à rede;
* Cartão SD no mínimo 8GB.  

**Imagem do Sistema Operacional**  

Cada experimento há uma imagem da distribuição Linux já pronta devidamente configurado e com softwares exclusivos instalados. As imagens foram adquiridas no link do RexLab: http://wiki.rexlab.ufsc.br/cd/images/  

Pegue a imagem “arduino-labx-3B+.rar” e descompacte:
![image](https://user-images.githubusercontent.com/90244580/184411580-6db27609-f5cf-4a1b-bd3a-5b1d1a4d8e4b.png) 

Insira o cartão SD no seu PC, em muitos casos é requerido adaptadores, pois geralmente os PCs não tem entradas para esses tipos de mídia. A imagem a seguir mostrado um dos tipos de adaptadores USB para cartão SD:  
![image](https://user-images.githubusercontent.com/90244580/184411635-8acd21cb-6635-46fe-bb2b-e63b864d3d19.png)  

Formate o cartão SD com o “SD Formatter”, execute esse aplicativo como administrador. Vá em opções e coloque o tipo de formatação rápida e ajuste de tamanho ligado:
![image](https://user-images.githubusercontent.com/90244580/184411732-cd95c594-43bf-4cc8-b11f-db20ddf0e6b6.png)  

Selecione o driver do pendrive alvo e clique em formatar:
![image](https://user-images.githubusercontent.com/90244580/184411761-13b35eba-1fd0-4d2b-ac57-73731d7b4e28.png)  

Execute o “Win32DiskImager”:
![image](https://user-images.githubusercontent.com/90244580/184411799-57ae67da-3e13-48bc-8a94-b5fcac6a2b75.png)  

Busque a imagem do sistema operacional clicando no botão com símbolo da pastinha azul:
![image](https://user-images.githubusercontent.com/90244580/184411831-c703ab2e-0c13-42c0-bddc-8f08ff4242c0.png)  

Navegue até o local da imagem e o aponte a imagem e clique em abrir:
![image](https://user-images.githubusercontent.com/90244580/184411852-87942f56-30bf-4a91-be68-75f2a6ae279a.png)  

Selecione a unidade onde se encontra o cartão SD e clique no botão “write” dando início ao processo de gravação da imagem no cartão SD:
![image](https://user-images.githubusercontent.com/90244580/184411875-cfc4f3c5-7cc5-4fcf-ab45-ff24293ac0d2.png)  

Espere pelo processo de gravação:
![image](https://user-images.githubusercontent.com/90244580/184411907-153bdca5-57c0-4cde-8d5f-cc4128099d1e.png)  

No fim da gravação o software vai emitir um aviso de gravação concluída com sucesso. Clique “OK” para finalizar o processo.
![image](https://user-images.githubusercontent.com/90244580/184411943-99119a75-d43d-4221-9b19-e976bb1c965d.png)  
  
  **Configurando**  
   
Acesse o cartão SD para fazermos algumas configurações. Se for o modelo raspberry pi 3, seja nacional ou não, devemos desabilitar o bluetooth, pois a UART que usamos é redirecionado para ele. Abra o arquivo “config.txt” da partição Windows do cartão SD:  
![image](https://user-images.githubusercontent.com/90244580/184412096-0551e03f-9517-44af-b496-3e4f4153021b.png)  

Adicione a seguinte a linha: “dtoverlay=pi3-disable-bt” logo após de “#dtoverlay=lirc-rpi”:  
![image](https://user-images.githubusercontent.com/90244580/184412148-5802cd99-0f41-43ac-8dff-098ee25b0cc8.png)  

É preciso ajustar o IP do SBC para que possamos acessá-lo para os testes nos experimentos. Abra o arquivo “cmdline.txt”:  
![image](https://user-images.githubusercontent.com/90244580/184412193-6afcf04f-8ae3-43ca-805f-123f519807fc.png)  

A adicione o seguinte comando no fim da linha da com os dados da sua rede de trabalho:  
`ip=<endereço ip>::<gateway>:<mascara>rpi:eth0:off`  
Exemplo:  
 `ip=192.168.0.25::192.168.1.1:255.255.255.0:rpi:eth0:off`  
![image](https://user-images.githubusercontent.com/90244580/184412330-d5730e27-68c0-4cbb-9b41-a530c850fb33.png)  

 Ejete o cartão SD do PC com segurança:  
 ![image](https://user-images.githubusercontent.com/90244580/184412356-a91eb173-15ca-4531-a1cf-d4162099006c.png)  
 
 Após a preparação do cartão SD insira-o no SBC:  
 ![image](https://user-images.githubusercontent.com/90244580/184412389-6c114645-a009-4721-a301-6470692fc10a.png)  
 
 Conecte o cabo de rede no SBC e ligue o experimento. Espere pelo boot. Quando o LED verde ficar piscando regularmente no mesmo ritmo indica que o boot já foi feito por completo e o SBC já está no modo de trabalho. No PC abra um prompt e testa a comunicação dando um ping no IP do SBC:  
 ![image](https://user-images.githubusercontent.com/90244580/184412441-f3c47035-4b5a-4e9b-8fb6-e0218545f09a.png)
  
   
**Acessando**  
   
 Podemos conectar monitor, mouse e teclado e trabalhar direto no SBC, ou acessar remotamente via protocolo SSH com Putty e WinSCP.   
 
O “Putty”, este pode ser baixado do site: http://www.putty.org/  
 
Execute-o e digite o endereço IP do SBC, que neste caso 192.168.0.25	, entre aporta de conexão do protocolo SSH, onde o padrão é a porta 22, selecione o tipo de conexão SSH, opcionalmente entre com o nome da secção e salve para futuras conexões, e tecle o botão de abrir a conexão:  
 ![image](https://user-images.githubusercontent.com/90244580/184412554-fef27165-8f8e-4c1b-97f0-737a13a05cd5.png)
  
 Durante a primeira conexão com esse IP e usuário vai haver uma troca de chave de segurança, neste caso clicando sim porque a conexão é legitima:  
 ![image](https://user-images.githubusercontent.com/90244580/184412596-20e84689-2aef-46ba-b8b7-0552ddab2790.png)
  
 Quando a conexão for feita entre com usuário root e sua senha. A primeira vez pode demorar um pouco para fazer o login:  
 
**EXPERIMENTO** | **USUÁRIO** | **SENHA DO ROOT**
 :--: | :--: | :--:
 eletric_frame_ac-v2 | root | rexlabAC1!CA
 inclined_plane-v4 | root | rexlabPI2@IP
   
 Quando a conexão for feita um terminal do Linux vai aparecer na espera de comandos:  
 ![image](https://user-images.githubusercontent.com/90244580/184413066-4be07d6a-d9c4-494a-aba7-859ec921074d.png)
  
 node-gyp rebuild: recompila algum código para o node que não foi escrito javascript, em nosso caso o C. Ele gera um addon pro javascript que se comunicar com o C.  
   
 **Fazendo Backup**  
   
 Com o SBC já instalado com Linux e devidamente configurado para o experimento, vamos fazer o backup do cartão SD, criando uma imagem do mesmo, para que se possa replicar para novos experimentos.  
 Insira o cartão SD no seu PC, em muitos casos é requerido adaptadores, pois geralmente os PCs não tem entradas para esses tipos de mídia. A imagem a seguir mostrado um dos tipos de adaptadores USB para cartão SD:  
 ![image](https://user-images.githubusercontent.com/90244580/184413158-33479c42-8e96-4ca4-b03f-f4af846f3ca6.png)
  
 Execute o “Win32DiskImager”;  
 Entre com o local e nome do arquivo, com extensão IMG, que será salvo a imagem. Utlize o mesmo nome dado pela UFSC. E depois clique para ler o cartão:  
 Entre com o local e nome do arquivo, com extensão IMG, que será salvo a imagem. Utlize o mesmo nome dado pela UFSC. E depois clique para ler o cartão:  
 ![image](https://user-images.githubusercontent.com/90244580/184413232-e17f12ec-79ed-4104-a66e-db1634d56b9e.png)
  
 ![image](https://user-images.githubusercontent.com/90244580/184413256-2251d151-a471-4e2d-9499-a8f4475e895e.png)
  
 Compactar a imagem:  
 ![image](https://user-images.githubusercontent.com/90244580/184413284-6d0a31a1-03a6-4da3-bebf-6648830af416.png)
  
 Salve a imagem no local adequado e renomeie de acordo com o projeto:  
 ![image](https://user-images.githubusercontent.com/90244580/184413312-58b6a38e-eed0-446c-8a26-f11f5858c970.png)
  
   
 **Restaurar a Imagem**  
 Utilize a imagem backup desejada e siga o processo de formatação e gravação do cartão do documento   