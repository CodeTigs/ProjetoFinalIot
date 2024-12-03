# ProjetoFinalIot 
Matheus José Almeida Finamor 1436


Tiago Rodrigues Plum Ferreira 1996 

# SmartPlant Automation System

Este projeto implementa um sistema de automação para cultivo inteligente utilizando ESP32 e integração com o Blynk. Ele monitora a umidade do solo, o nível de água do reservatório e controla a iluminação de crescimento de plantas, proporcionando um ambiente ideal para cultivo indoor.

## Funcionalidades

- **Monitoramento de umidade do solo**: Liga automaticamente a bomba de água quando o solo está seco.
- **Monitoramento do nível de água do reservatório**: Envia alertas e acende LEDs indicadores quando o nível de água está baixo.
- **Controle de luz de crescimento**: Gerencia automaticamente o horário de iluminação com base no ciclo diário configurado.
- **Integração com o Blynk**: Permite controle e monitoramento remoto através de um aplicativo.

## Hardware Necessário

- ESP32
- Relé para bomba de água
- Relé para luz de crescimento
- Sensores de nível de água e umidade do solo (simulados neste exemplo)
- LEDs indicadores (verde, vermelho e azul)
- Fonte de alimentação compatível

## Configuração do Ambiente

### Pré-requisitos

- **Blynk**: Configure um projeto no aplicativo Blynk e obtenha o `Auth Token`.
- **WiFi**: Configure o SSID e senha da sua rede WiFi.

### Bibliotecas Utilizadas

- [WiFi.h](https://www.arduino.cc/en/Reference/WiFi)
- [BlynkSimpleEsp32.h](https://github.com/blynkkk/blynk-library)
- [TimeLib.h](https://www.pjrc.com/teensy/td_libs_Time.html)

### Instalação das Bibliotecas

Utilize o **Gerenciador de Bibliotecas** do Arduino IDE para instalar as dependências necessárias.

### Conexões

| Componente                 | Pino do ESP32         |
|----------------------------|-----------------------|
| Relé da bomba de água      | GPIO 26              |
| Relé da luz de crescimento | GPIO 25              |
| LED verde                  | GPIO 14              |
| LED vermelho               | GPIO 27              |
| LED azul                   | GPIO 33              |

## Código

O código principal é configurado no arquivo `main.cpp`. Certifique-se de atualizar os valores de `BLYNK_TEMPLATE_ID`, `BLYNK_TEMPLATE_NAME`, `BLYNK_AUTH_TOKEN`, `ssid` e `pass` com os dados do seu projeto.

## Como Usar

1. Faça upload do código para o ESP32 usando a Arduino IDE.
2. Abra o monitor serial para verificar as mensagens de inicialização e depuração.
3. Controle e monitore o sistema utilizando o aplicativo Blynk no smartphone.

## Demonstração de Funções

- **Controle Automático**:
  - A bomba de água é ativada automaticamente quando a umidade do solo está abaixo de 40%.
  - A luz de crescimento segue um ciclo diário de 14 horas a partir das 6h.
  - Alertas são enviados quando o nível do reservatório de água está baixo.
- **Controle Manual via Blynk**:
  - Ligue/desligue a bomba de água e a luz de crescimento diretamente pelo aplicativo.
  - LEDs indicam o status de cada funcionalidade.

## Melhorias Futuras

- Adicionar sensores reais para monitoramento mais preciso.
- Implementar histórico de dados para análise de cultivo.
- Expandir para suportar múltiplos ambientes de cultivo.


---

**Desenvolvido por[Tiago Rodrigues Plum Ferreira]**
