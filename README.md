# Robô seguidor de pessoas

Projeto acadêmico de um robô móvel capaz de acompanhar uma pessoa, utilizando a **Texas Instruments Tiva C Series LaunchPad EK-TM4C123GXL** (microcontrolador **TM4C123GH6PM**, ARM Cortex-M4F) como unidade de controle.

> **Status:** planejamento inicial. Sensores, driver de motor, chassi e ferramentas de compilação ainda precisam ser definidos e documentados conforme o hardware do protótipo.

## Objetivo

Construir um robô que detecte uma pessoa, estime sua posição ou distância e controle os motores para acompanhá-la com segurança. A LaunchPad executará a lógica de controle e fará a interface com os sensores e o circuito de acionamento dos motores.

A placa, por si só, não identifica pessoas: o projeto precisa de um sensor ou módulo apropriado para essa tarefa. A escolha desse componente determinará como os dados serão obtidos e processados.

## Arquitetura prevista

1. **Detecção e acompanhamento:** um sensor ou módulo identifica a pessoa e fornece informações como direção e, se disponível, distância.
2. **Controle:** o firmware na LaunchPad interpreta essas informações e calcula os comandos de movimento.
3. **Acionamento:** um driver de potência recebe os comandos da placa e controla os motores do robô.
4. **Parada segura:** se a pessoa deixar de ser detectada, os dados do sensor forem inválidos ou ocorrer uma falha, o robô deve parar até que a condição segura seja restabelecida.

## Componentes a definir

- LaunchPad EK-TM4C123GXL;
- sensor ou módulo para detecção e acompanhamento de pessoas;
- driver compatível com os motores e a tensão/corrente do conjunto;
- motores, rodas e chassi;
- bateria e reguladores de tensão adequados;
- cabos, conectores e suporte mecânico.

A compatibilidade elétrica e as interfaces de comunicação devem ser verificadas antes de conectar os componentes. **Não conecte motores diretamente aos pinos da LaunchPad**; use um driver apropriado e uma alimentação dimensionada para o conjunto.

## Firmware

O firmware deverá integrar a leitura do sensor, a lógica de acompanhamento e o controle dos motores. Os detalhes de compilação, gravação e execução serão adicionados quando forem escolhidas as ferramentas e a implementação do projeto.

## Segurança e testes

- Faça os primeiros testes com as rodas suspensas ou em uma área controlada e livre de obstáculos.
- Implemente uma condição de parada quando a pessoa não for detectada ou quando a leitura do sensor não for confiável.
- Verifique alimentação, polaridade, níveis lógicos e limites elétricos de cada componente antes de ligar o circuito.
- Mantenha uma forma de desligar rapidamente a alimentação dos motores durante os testes.

## Próximos passos

- Escolher o sensor/módulo de detecção de pessoas e definir sua interface com a LaunchPad.
- Selecionar motores, driver, bateria e chassi compatíveis.
- Documentar o ambiente de desenvolvimento e os procedimentos para compilar e gravar o firmware.
- Implementar e testar a parada segura e o controle de movimento.
