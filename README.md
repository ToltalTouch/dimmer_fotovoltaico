# Circuito dimmer fotovoltaico
---
Projeto visa a criacao de um circuito dimmerivel com fotosensibilidade para ajuste da luz ambiente. Utilizando:
- Transistor NPN (BC548, 2N2222): Atua como chave, controlando a corrente para o LED;
- LDR: Sensor para detectar luz no ambiente;
- Resistor de 1kΩ: Para limitar a corrente na base do transistor;
- Resistor de 100Ω a 330Ω: Limita a corrente para o LED, o valor vai variar de acordo com a tensão do LED;
- Fonte de alimentação de 9v a 12v;

Caso deseje utilizar uma fita de LED com a tensão de 12v, utilize um MOSFET de potencia de canal N (IRF540 ou IRF520)
---
## Montagem do circuito:
Utilizando uma protoboard, siga os passos:
1. Conecte o LDR com um dos terminais no positivo do circuito;
2. Conecte o Transistor:
   - O emissor do transistor deve ser ligado ao negativo do circuito;
   - O coletor deve ser ligado no terminal negativo do LED;
   - O resistor de 1kΩ deve estar entre o outro terminal do LDR e a **base** do transistor;
  1. Caso utilize um MOSFET:
     - Ligue o Source do mosfet no VCC;
     - o Drain ao negativo da fita;
     - O resistor de 1kΩ deve ser ligado entre o outro terminal do LDR e o **Gate**;
3. Conecte o LED:
   - O resistor de proteçao (100Ω~330Ω) deve ser conectado no VCC e no positivo do LED;

Cuidados com o MOSFET:
1. Se a fita for muito longa, o mosfet deve utilizar um dissipador de calor
2. Para um controle mais preciso, pode ser necessario utilizar um potenciometro (trimpont) em serie com o LDR

**Para desligar/ligar o circuito, coloque uma chave seletora no VCC do circuito**

---
## Funcionamento desejado:
1. Ambiente com alta luminosidade:
   - O LDR diminui a resistencia permitindo que a corrente aumente na base do transistor, ativando-o completamente. O                transistor deve permitir que a corrente maxima percorra para o LED que acendera com o **brilho total**

2. Ambiente com baixa luminosidade:
   - Com a baixa exposição a luz, a resistencia do LDR aumenta limitando a corrente na base do transistor, conduzindo menos          corrente, diminuindo.
---
Sera postado o projeto do circuito impresso, e o esquema para protoboard.
