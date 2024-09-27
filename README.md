# Projeto IoT com Visão Computacional para Detecção de Movimentos

## Descrição

Este projeto utiliza técnicas de **visão computacional** e **inteligência artificial (IA)** para detectar a presença de pessoas em um ambiente e controlar uma lâmpada automaticamente. O sistema usa uma câmera conectada a uma **CPU** para processar imagens e identificar movimentos e pessoas em horários específicos do dia. A IA aprende a reconhecer padrões de presença e ativa a lâmpada apenas quando necessário.

Confira uma simulação no [Tinkercad](https://www.tinkercad.com/things/gC1vLRuSV5x-lampada-sensor-pir).

## Funcionalidades

- **Detecção de movimentos:** O sistema identifica quando há movimento dentro do ambiente.
- **Reconhecimento de pessoas:** A IA é treinada para distinguir entre pessoas e outros objetos em movimento.
- **Automação da iluminação:** A lâmpada é acesa automaticamente quando uma pessoa é detectada em horários predefinidos.
- **Treinamento contínuo:** A IA aprimora sua capacidade de reconhecimento com o tempo, ajustando-se ao padrão de movimento no ambiente.
  
## Tecnologias Utilizadas

- **Visão Computacional:**
  - OpenCV (para processamento de imagens)
  - TensorFlow / PyTorch (para IA e aprendizado de máquina)
- **Hardware:**
  - Câmera de vídeo
  - CPU (para processamento de imagens em tempo real)
  - Dispositivo IoT (para controle da lâmpada, ex: ESP32 ou Raspberry Pi)
- **Linguagens:**
  - Python (para processamento de imagens e treinamento da IA)
  - C++/MicroPython (para comunicação com a lâmpada via dispositivo IoT)
- **Protocolos:**
  - MQTT (para comunicação entre o sistema de visão e o dispositivo IoT)
  
## Arquitetura

1. **Câmera:** Captura imagens em tempo real do ambiente.
2. **Processamento na CPU:**
   - A CPU processa as imagens para detectar movimento e identificar a presença de pessoas.
   - A IA é responsável por analisar e aprender padrões de comportamento no ambiente.
3. **Dispositivo IoT:** Recebe comandos via MQTT para acender ou apagar a lâmpada com base na análise da IA.
4. **Lâmpada:** A lâmpada é conectada a um microcontrolador que responde aos comandos de ativação/desativação.

## Configuração e Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/usuario/projeto-iot-visao-computacional.git
2. Instale as depêndencias necessárias:
   ```bash
   pip install -r requirements.txt
3. Configuração do dispositivo IoT:
   - Configure ESP32/Raspberry Pi com MicroPython ou C++ para controlar a lâmpada via MQTT.
   - Defina o endereço IP do broker MQTT e as credenciais no código do dispositivo.
4. Treinamento da IA:
   - Use o script train_model.py para treinar o modelo de reconhecimento de pessoas.
   - Ajuste os paramentros de treinamento conforme necessário para o seu ambiente.
5. Executar o sistema de visão:
   ```bash
   python main.py
## Uso
- O sistema iniciará a detecção de movimentos e o reconhecimento de pessoas automaticamente.
- Quando uma pessoa for detectada, a lâmpada será acesa de acordo com as regras estabelecidas. 
