# Streaming de imagens

  Em laboratórios remotos, um dos sensores mais difundidos e empregados na experiência é o 
sensor de imagem. Através de uma câmera de vídeo, imagens são captadas e transferidas para 
um computador, e deste compartilhadas para outros computadores de modo simultâneo 
enquanto ocorre. 
No RExLab se optou pelo uso de câmeras web com conexão USB devido o baixo custo e a 
facilidade de aquisição. O mesmo computador embarcado utilizado para controle do 
experimento também é o responsável pelo gerenciamento e disponibilização do streaming no 
formato MJPEG (Motion JPEG). O MJPEG é um formato de compressão de vídeo na qual cada 
frame de vídeo é comprimido separadamente como uma imagem JPEG.

  No HTTP streaming, cada imagem é separada em respostas individuais por um marcador 
específico. O tipo de conteúdo (mime-type) multipart/x-mixed-replace informa ao cliente para 
esperar vários quadros delimitados por um identificador (boundary-name). 

  Visto que existem muitos servidores de streaming de código aberto, optou-se pelo Motion para 
explorar aspectos de leveza (utilização de poucos recursos) e configuração flexível. O Motion é 
um software escrito em C para sistemas Linux que usa a API de vídeo linux, e é capaz de detectar 
se uma parte significante da imagem tem mudado. Algumas variáveis são ajustadas através de 
seu arquivo de configuração principal para adequar-se aos requisitos de nossa aplicação.

  Atualmente, os principais navegadores do mercado como Firefox, Google Chrome e Safari já 
possuem o suporte nativo para o streaming MJPEG. Outros navegadores, como o Internet 
Explorer podem apresentar o fluxo de imagens com o auxílio de plug-ins externos, como o 
Cambozola. Para clientes Android existem bibliotecas de código fonte aberto para incluir um 
visualizador MJPEG em aplicações de código nativo
