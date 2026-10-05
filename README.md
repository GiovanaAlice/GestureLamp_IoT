# Gesture Lamp 💡🖐️

https://github.com/user-attachments/assets/fa7c4b91-96c3-4831-8471-62e1d0efd080

Projeto simples que permite ligar ou desligar uma lâmpada utilizando gestos, com MediaPipe, AWS IoT Core e ESP8266.

## Sobre o projeto

A ideia do projeto é estudar AWS IoT de uma forma prática e visual.

## Arquitetura

<img width="783" height="349" alt="photo_4974645583289191591_x" src="https://github.com/user-attachments/assets/75b5fbc0-24e4-460f-bdac-9a9659392634" />

### Fluxo

Python + MediaPipe → AWS IoT Core → ESP8266 → Relé → Lâmpada

## Tecnologias utilizadas

- Python
- OpenCV
- MediaPipe
- MQTT
- AWS IoT Core
- C++
- Arduino IDE

## Hardware

- ESP8266 NodeMCU
- Módulo relé
- Lâmpada

## Como funciona

A câmera captura os movimentos da mão utilizando OpenCV. O MediaPipe analisa as imagens e identifica o gesto realizado.

A partir do gesto reconhecido, o Python gera um comando, como `LIGHT_ON` ou `LIGHT_OFF`, e publica essa mensagem no AWS IoT Core utilizando MQTT.

O ESP8266 está inscrito no tópico MQTT e, ao receber o comando, aciona sua saída GPIO, controlando o relé e consequentemente a lâmpada.

## Estrutura do projeto
