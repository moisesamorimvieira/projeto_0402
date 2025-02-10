<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=02A6F4&height=120&section=header"/>
<h1 align="center">Embarcatec | Unidade 4 / Capítulo 6 Introdução às Interfaces de Comunicação Serial com RP2040 UART, SPI e I2C. </h1>

<div align="center">  
  <img width=40% src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=02A6F4&style=for-the-badge"/>
</div>

##Enunciado
Para consolidar os conceitos sobre o uso de interfaces de comunicação serial no RP2040 e explorar as funcionalidades da placa de desenvolvimento BitDogLab, propõe-se a realização da seguinte tarefa individual prática.

## Objetivo do Projeto

• Compreender o funcionamento e a aplicação de comunicação serial em microcontroladores.
• Aplicar os conhecimentos adquiridos sobre UART e I2C na prática.
• Manipular e controlar LEDs comuns e LEDs endereçáveis WS2812.
• Fixar o estudo do uso botões de acionamento, interrupções e Debounce.
• Desenvolver um projeto funcional que combine hardware e software.

## Descrição do Projeto:
Neste projeto, você deverá utilizar os seguintes componentes conectados à placa BitDogLab:
• Matriz 5x5 de LEDs (endereçáveis) WS2812, conectada à GPIO 7.
• LED RGB, com os pinos conectados às GPIOs (11, 12 e 13).
• Botão A conectado à GPIO 5.
• Botão B conectado à GPIO 6.
• Display SSD1306 conectado via I2C (GPIO 14 e GPIO15).

## Funcionalidades do Projeto 1. 
Modificação da Biblioteca font.h • Adicionar caracteres minúsculos à biblioteca font.h. Use sua criatividade para criar os novos caracteres.
2. Entrada de caracteres via PC
• Utilize o Serial Monitor do VS Code para digitar os caracteres.
• Cada caractere digitado no Serial Monitor deve ser exibido no display SSD1306.
Observação: Apenas um caractere será enviado de cada vez, não é necessário suportar o envio de strings completas.
• Quando um número entre 0 e 9 for digitado, um símbolo correspondente ao número deve ser exibido, também, na matriz 5x5 WS2812.
3. Interação com o Botão A
• Pressionar o botão A deve alternar o estado do LED RGB Verde (ligado/desligado).
• A operação deve ser registrada de duas formas:
o Uma mensagem informativa sobre o estado do LED deve ser exibida no display SSD1306
o Um texto descritivo sobre a operação deve ser enviado ao Serial Monitor.
4. Interação com o Botão B
• Pressionar o botão A deve alternar o estado do LED RGB Azul (ligado/desligado).
• A operação deve ser registrada de duas formas:
o Uma mensagem informativa sobre o estado do LED deve ser exibida no display SSD1306
o Um texto descritivo sobre a operação deve ser enviado ao Serial Monitor.

## 🗒️ Lista de requisitos
1) Caso o usuário clique no botão (pushbutton), os três LEDs serão ligados (todos em nível alto). A partir da primeira rotina de atraso, ocorrerá uma mudança de estado
Para o desenvolvimento, devem ser seguidos os seguintes requisitos:
1. Uso de interrupções: Todas as funcionalidades relacionadas aos botões devem ser implementadas utilizando rotinas de interrupção (IRQ).
2. Debouncing: É obrigatório implementar o tratamento do bouncing dos botões via software.
3. Controle de LEDs: O projeto deve incluir o uso de LEDs comuns e LEDs WS2812, demonstrando o domínio de diferentes tipos de controle.
4. Utilização do Display 128 x 64: A utilização de fontes maiúsculas e minúsculas demonstrará o domínio do uso de bibliotecas, o entendimento do princípio de funcionamento do display, bem como, a utilização do protocolo I2C.
5. Envio de informação pela UART: Visa observar a compreensão sobre a comunicação serial via UART.
6. Organização do código: O código deve estar bem estruturado e comentado para facilitar o entendimento.
   
## 🛠 Tecnologias

1. **Git e Github**;
2. **VScode**;
3. **Linguagem C**;
4. **Software de emulação PuTTy. (Opcional para testes)**
5. **Extensões no VScode do Raspberry Pi Pico Project e CMake**

## Entrega
Código: O código-fonte do projeto deve ser entregue em um link do seu repositório, contendo todos os arquivos necessários para sua execução.
Vídeo de demonstração: Deve ser produzido um vídeo de até 2 minutos, no qual o aluno deve:
• Aparecer pessoalmente demonstrando o funcionamento do projeto.
• Explicar brevemente as funcionalidades implementadas.
• Mostrar o projeto em execução na placa BitDogLab.
• Link do vídeo no Youtube ou Google Drive.
## 💻 Desenvolvedores
 
<table>
  <tr>
    
<td align="center"><img style="" src="https://avatars.githubusercontent.com/u/96251377?v=4" width="100px;" alt=""/><br /><sub><b> Moises Amorim </b></sub></a><br />👨‍💻</a></td>

  </tr>
</table>


## 🎥 Demonstração: 

<div align="center">
  <figure>  
    
    
<figcaption>

**Figura 1** - Youtube - Acessível em:[ https://wokwi.com/projects/421471551935887361](https://youtu.be/qZhzecNl0k8)
    </figcaption>
  </figure>
</div>
 
 

 
