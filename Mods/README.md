# Modificações do CYD

Aqui estão algumas modificações de hardware que podem ser feitas no CYD para melhorar ou alterar parte de suas funcionalidades.

## Melhoria do alcance e desempenho do LDR

O LDR do CYD tem um alcance bastante limitado entre totalmente escuro e totalmente claro. Esta modificação aumenta esse alcance e também suaviza a saída do LDR.

Ela envolve solda manual sobre componentes 0603, portanto provavelmente não é adequada para iniciantes em soldagem!

[Link](https://github.com/hexeguitar/ESP32_TFT_PIO#1-ldr)

## Modificação do ganho do amplificador de áudio

A configuração do amplificador de áudio no CYD não é boa, resultando em áudio de baixa qualidade. Esta modificação reduz o ganho, proporcionando um som melhor.

Conforme descrito, ela envolve soldar outro resistor sobre um componente 0603, mas você também pode adicionar um resistor de 10k entre os dois terminais inferiores do IC para obter a mesma modificação. Faça o que parecer mais fácil para você!

![imagem](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/assets/1562562/04b98352-ca41-4bcc-bf77-380db4cce1da)

[Link](https://github.com/hexeguitar/ESP32_TFT_PIO#audio-amp-gain-mod)

## Adicionando PSRAM

É possível usar PSRAM com o CYD fazendo algumas modificações na placa.

Esta modificação envolve remover o LED RGB, cortar algumas trilhas e instalar o IC de PSRAM.

[Link](https://github.com/hexeguitar/ESP32_TFT_PIO#adding-psram)
