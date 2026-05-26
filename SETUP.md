# Opções de instalação e configuração

Esta página aborda os conceitos básicos de configuração do CYD.

## Configuração de hardware

Na verdade, não há nada para configurar aqui; basta conectar o CYD a um computador usando um cabo micro USB (ele vem até mesmo com um).

## Configuração de software

O driver precisa estar configurado para fazer upload para o CYD, incluindo o WebFlash de projetos.

### Driver

O CYD usa o chip USB para UART CH340. Se você ainda não tiver um driver instalado para esse chip, talvez precise instalar um. Consulte o [guia da Sparkfun para instruções de instalação](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all).

## Configuração para programação

Siga estas instruções se quiser escrever novos códigos para o CYD.

### Definição da placa

Você precisará ter o ESP32 configurado na sua Arduino IDE; as [instruções podem ser encontradas aqui](https://docs.espressif.com/projects/arduino-esp32/en/latest/installing.html).

Depois, você pode selecionar praticamente qualquer placa ESP32 no menu de placas. (Normalmente uso "ESP32 Dev Module", mas isso não faz muita diferença.)

Se ocorrerem erros ao fazer upload de um sketch, tente definir a velocidade de upload da placa como `115200`.

<a id="library-configuration"></a>
### Configuração da biblioteca

O CYD pode funcionar com diversas bibliotecas, mas a principal na qual este repositório se concentra é a [TFT_eSPI](https://github.com/Bodmer/TFT_eSPI), pois ela é bastante popular para trabalhar com esses tipos de tela e há muitos exemplos.

Ela pode ser instalada pelo gerenciador de bibliotecas, procurando por "TFT_eSPI".

 > Observação: após instalar a biblioteca, copie o arquivo [User_Setup.h](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/blob/main/DisplayConfig/User_Setup.h) para a pasta Arduino `libraries\TFT_eSPI`. Isso configura a biblioteca para uso com esta tela.

### Exemplos

Disponibilizei exemplos para você experimentar e obter ideias ou inspiração. [Confira aqui.](/Examples/)
