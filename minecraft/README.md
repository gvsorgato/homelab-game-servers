# Minecraft Server Infra

## O que é
Administração de servidores de jogos multiplayer (Minecraft e Terraria), hospedados 
em ambiente próprio, com foco em rede, controle de acesso e manutenção contínua 
desde 2019.

## Ambiente
- **Virtualização**: VirtualBox, rodando VM com Ubuntu Server 24.04 LTS
- **Jogadores**: ~8 pessoas conectando via IP público da VM
- **Ciclo de vida**: servidores reconstruídos do zero periodicamente 
  (aproximadamente a cada 1,5 anos), como prática de manutenção e reaprendizado 
  do ambiente

## Rede
- Configuração de **port forwarding** no roteador, usando porta customizada 
  (ex: 30954 no lugar da porta padrão 25565 do Minecraft), como medida básica 
  de segurança
- Configuração de **IP fixo** na VM, resolvendo um problema recorrente inicial 
  em que o IP mudava a cada reinicialização do modem ou reinstalação do sistema, 
  derrubando o acesso dos jogadores

## Backup
- Antes de cada reconstrução ou atualização importante, o mundo do jogo era 
  copiado manualmente para o PC local e depois enviado ao Google Drive como 
  cópia de segurança
- Processo manual, sem automação até o momento — funcionou de forma 
  consistente ao longo dos anos, mas é um ponto identificado de melhoria futura 
  (ex: script de backup automatizado)

## Manutenção e versionamento
- Atualizações de versão aplicadas com atraso proposital de 1 a 1,5 meses após 
  o lançamento, permitindo que bugs críticos sejam corrigidos pela desenvolvedora 
  antes de impactar o ambiente em uso
- Reconstrução completa da VM e dos servidores periodicamente, como ciclo de 
  manutenção e teste de reconfiguração do ambiente do zero

## O que eu aprendi
- Configuração de rede doméstica para exposição controlada de serviços 
  (port forwarding, portas customizadas)
- Importância de IP estático em ambientes que dependem de acesso externo 
  consistente
- Gestão de atualizações com janela de segurança antes de aplicar mudanças 
  em produção
- Rotina de backup manual, com consciência de que automação é o próximo passo 
  natural de evolução do processo
- Administração de VM Linux (Ubuntu Server) do provisionamento à manutenção 
  contínua, incluindo ciclos completos de reconstrução
