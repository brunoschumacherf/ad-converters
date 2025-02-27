---

# 🎮 Projeto: Controle de LEDs e Display com Joystick

Este projeto utiliza um joystick para controlar LEDs RGB e um display OLED SSD1306 em um Raspberry Pi Pico, explorando conceitos de **PWM**, **ADC**, **I2C**, **interrupções** e **debouncing**.

---

## 🛠 Componentes Utilizados

- **LED RGB (GPIOs: 11, 12 e 13)** → Representa os eixos X e Y do joystick.
- **Joystick (GPIOs: 26 e 27 - ADC0 e ADC1)** → Entrada analógica para posicionamento.
- **Botão do Joystick (GPIO 22)** → Alterna o LED verde e modifica a borda do display.
- **Botão A (GPIO 5)** → Ativa/desativa os LEDs controlados por PWM.
- **Display OLED SSD1306 (I2C - GPIOs 14 e 15)** → Exibe posição do joystick e estilos de borda.

---

## 🚀 Funcionalidades

### 🎛 Controle de LEDs RGB via Joystick
- **LED Azul:** Brilho ajustado pelo eixo Y do joystick.
- **LED Vermelho:** Brilho ajustado pelo eixo X do joystick.
- **LED Verde:** Ligado/desligado pelo botão do joystick.

### 📟 Movimentação do Quadrado no Display SSD1306
- Quadrado de **8x8 pixels** se move conforme os valores do joystick.
- A borda do display muda de estilo ao pressionar o botão do joystick.

### ⏳ Interrupções e Debouncing
- **Botão do Joystick:** Alterna o LED verde e modifica a borda do display.
- **Botão A:** Ativa/desativa os LEDs RGB controlados por PWM.
- **Debouncing:** Implementado para evitar acionamentos múltiplos indevidos.

### 🛠 Configuração Inicial do Joystick
Na primeira utilização, ajuste os valores do joystick para garantir precisão:

```c
#define CENTRO_X_JOYSTICK 1922
#define CENTRO_Y_JOYSTICK 2025
```

---

## 🔧 Requisitos Técnicos

- **Interrupções** para os botões.
- **Debouncing** para leituras confiáveis.
- **Comunicação I2C** para o display OLED SSD1306.
- **ADC** para leitura do joystick.
- **PWM** para controle suave do brilho dos LEDs RGB.
- **Código organizado e bem comentado**.

---


