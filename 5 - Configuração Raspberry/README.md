## Baixando os arquivos

  Antes de tudo, você deve acessar este link clicando [aqui](https://alunosatcedu-my.sharepoint.com/:f:/g/personal/jefferson_57221_alunosatc_edu_br/Ep4_SScbwBZFpGY_S-Wh9d0B6rdQTvU-0xS5ClqPOsheoA?e=wVx5ys) para acessar o OndeDrive 
e realizar o download do arquivo que será colocado em seu cartão MicroSD.

  Após isso, clique aqui para acessar o site para poder baixar o [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/). Depois disso, 
insira o seu cartão microSD e abra o Win32; selecione o cartão em Device, selecione o arquivo que foi baixado do OneDrive anteriormente e clique em WRITE, 
espere o processo ser concluído.

## Configuração 

  Com os arquivos no cartão, coloque-o no Raspberry e também um monitor, teclado e fonte de energia.
  Após um breve carregamento, em raspberry login digite **root**, aperte enter e em password escreva **./rexlabBL!LB**, dê enter novamente.
 -  A partir daqui apenas vá escrevendo o que for necessário e vá dando enter:
  1. cd/home, enter
  2. ls, enter
  3. cd labx, enter
  4. ls 
  5. nano queue.js
  
 - Vá para **var status={ video: "http://xxx.xxx.xxx.xxx:8080"**, e coloque o IP público na porta onde o vídeo da câmera será transmitido.
 
 - Com o IP configurado, aperte ctrl+x
  1. cd/home, enter
  2. ls, enter
  3. cd.., enter
  4. ls, enter
  5. cd etc, enter
  6. /etc# ls, enter
  7. /etc# nano dhcpcd.conf, enter
  
  - Dentre as 4 primeiras linhas que aparecerem, altere "static ip_address" para o IP público que você digitou anteriormente.
  
  
  
  
  
