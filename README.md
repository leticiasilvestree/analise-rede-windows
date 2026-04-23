# Análise básica de rede e conexões no Windows

Este projeto foi desenvolvido como parte dos meus estudos iniciais em Cibersegurança.

## Objetivo
Analisar informações básicas da rede e conexões do sistema utilizando comandos do Windows.

## Ferramentas utilizadas
- Prompt de Comando (CMD)

## Comandos utilizados

### Ver IP e rede
ipconfig

### Ver conexões ativas
netstat -an

### Ver processos conectados
netstat -ano
tasklist

## Análise das conexões

Durante a análise com o comando `netstat -an`, observei:

- Portas em estado LISTENING (serviços aguardando conexão)
- Conexões em estado ESTABLISHED (comunicação ativa)
- Uso da porta 443 (HTTPS), indicando conexões seguras
- Comunicação local (127.0.0.1), representando processos internos

## Identificação de processos

Utilizando o comando `netstat -ano`, identifiquei o PID das conexões e relacionei com os processos usando:

tasklist | findstr [PID]

## Exemplo prático

Identifiquei o processo `mc-fw-host.exe`, relacionado a serviços de segurança (antivírus/firewall), indicando comportamento legítimo.

## O que aprendi

- Como identificar o IP do computador
- O que é gateway padrão
- Como visualizar conexões ativas
- Como relacionar conexões com processos
- Noções básicas de análise de rede

## 🚀 Conclusão

Este projeto me permitiu entender como meu computador se comunica com a rede e como analisar conexões ativas — um passo importante na área de Cibersegurança.
