-----------------------------------------------------------------
# Sistema de Monitoramento de Luminosidade com Arduino

Este projeto utiliza um **Arduino Uno**, sensor **LDR**, **LCD 16x2**, **LEDs** e um **buzzer** para monitorar e alertar sobre o nível de luminosidade no ambiente. O sistema indica visualmente (LEDs + display LCD) e sonoramente (buzzer) diferentes faixas de intensidade luminosa.

---

## Esquema do Circuito

O circuito foi desenvolvido e simulado no **Tinkercad**. 

---

## Componentes Utilizados

- 1x Arduino Uno
- 1x Display LCD 16x2 (modo 4 bits)
- 1x Sensor de luminosidade (LDR)
- 3x LEDs (verde, amarelo, vermelho)
- 1x Buzzer piezoelétrico
- 3x Resistores para LEDs (220Ω)
- 1x Resistor para LDR (10kΩ)
- Protoboard e jumpers

---

## Conexões dos Componentes

### LCD 16x2:
| LCD Pin | Arduino Pin |
|---------|-------------|
| RS      | 12          |
| E       | 11          |
| D4      | 10          |
| D5      | 9           |
| D6      | 8           |
| D7      | 4           |

### LEDs:
- Verde: pino 7
- Amarelo: pino 6
- Vermelho: pino 5

### Buzzer:
- Pino 3

### LDR:
- Ligado em divisor de tensão com resistor de 10kΩ
- Saída vai para o pino A0

---

## Dependências

Este projeto requer apenas a biblioteca padrão do Arduino:

#include <LiquidCrystal.h>

---

Como Rodar o Projeto

1-Monte o circuito conforme a imagem ou instruções acima.

2-Copie o código do projeto para a IDE do Arduino.

3-Conecte o Arduino ao computador via cabo USB.

4-Selecione a placa correta (Arduino Uno) e porta em Ferramentas > Porta.

5-Faça o upload do código.

6-Observe a resposta do sistema ao alterar a iluminação no LDR.

---

Comportamento Esperado

Faixa de Luminosidade | Ação

< 50%                 | LED verde aceso, mensagem "Luz controlada!"
  50–80%              | LED amarelo, buzzer toca 3s, mensagem "LimiteOK"
> 80%                 | LED vermelho, buzzer contínuo, mensagem "ALERTA!"

---

Ajustes

Você pode personalizar os limites de luminosidade alterando as variáveis no código:

int limiteOK = 50;
int limiteAlerta = 80;

---

Feito com:

-Arduino Uno R3

-Tinkercad Circuits

-Criatividade e propósito educacional

-----------------------------------------------------------------







