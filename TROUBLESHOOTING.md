# Primeiro, verifique se ele é um CYD!

Se estiver enfrentando algum problema, esta é a primeira coisa que eu verificaria!

Os exemplos e as informações contidos neste repositório destinam-se apenas à tela **ESP32-2432S028**. O número do modelo está escrito em dourado na parte traseira da tela, ao lado do conector do alto-falante.

<a id="display-is-not-turning-on"></a>
# A tela não liga

Se estiver enfrentando problemas para fazer a tela funcionar, a primeira coisa que eu tentaria seria usar o WebFlash de [um projeto existente](/PROJECTS.md#projects-1). Esses projetos contêm código reconhecidamente funcional e, se funcionarem corretamente, isso indica um problema de software, não de hardware.

## Se o projeto WebFlash exibir algo na tela

- Certifique-se de ter colocado o arquivo [User_Setup.h](DisplayConfig/User_Setup.h) no local correto, [conforme descrito aqui](/SETUP.md#library-configuration).
- O pino 21 é o pino de iluminação de fundo; certifique-se de que ele não esteja sendo usado para outra finalidade no seu sketch.

## O projeto WebFlash não exibe nada na tela

- Certifique-se de não conectar nada ao pino 21. Ele está disponibilizado no conector identificado como `P3`.
- Experimente outra fonte USB e/ou outro cabo.
- Se nada mais funcionar, seu CYD pode estar com defeito. Entre em contato com o vendedor.

# Tela, touch e cartão SD não funcionam ao mesmo tempo

O ESP32 oferece dois barramentos SPI de hardware utilizáveis, mas, no CYD, cada um dos dispositivos - tela, touch e cartão SD - usa um barramento diferente. Para usar os três dispositivos ao mesmo tempo, o SPI de um deles precisa ser "simulado" em software. Isso normalmente é feito para o dispositivo touch, pois ele não exige alta largura de banda. Portanto, use uma implementação de SPI por software, como [XPT2046_Bitbang_Slim](https://github.com/TheNitek/XPT2046_Bitbang_Arduino_Library), e siga o [exemplo de botões](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/tree/main/Examples/Basics/8-Buttons).

# A tela está piscando

- Experimente outra fonte USB e/ou outro cabo.
- Siga as etapas de [A tela não liga](#display-is-not-turning-on).
- Se nada mais funcionar, seu CYD pode estar com defeito. Entre em contato com o vendedor.

# Não é possível fazer upload
- No Ubuntu e suas variantes, desative ou desinstale o serviço `brltty` e certifique-se de que o usuário pertença ao grupo `dialout`.

# Flash automático com esptool falhou: modo de boot incorreto detectado (0x13)

Este é um problema conhecido ao gravar o ESP32 por meio de um conversor USB-UART, quando os sinais DTR e RTS são usados para alternar o chip para o modo bootloader (com lógica digital adicional de proteção com 2 transistores NPN). Em alguns PCs, sistemas operacionais e versões de driver ele funciona; em outros, não:

```
A fatal error occurred: Failed to connect to ESP32: Wrong boot mode detected (0x13)! The chip needs to be in download mode. For troubleshooting steps visit: https://docs.espressif.com/projects/esptool/en/latest/troubleshooting.html
```

A solução é substituir o capacitor entre EN (RST) e GND, instalado no CYD, de 0.1uF por um valor entre 1uF e 10uF.

**OBSERVAÇÃO:** No esquemático, esse capacitor é o C4, mas, pelo menos na versão Tipo-C do CYD, ele na verdade é o C5.
