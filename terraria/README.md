# Terraria Server

## O que é
Servidor de Terraria multiplayer, hospedado em VM dedicada (TerraVM), separada 
da VM do Minecraft — isolamento de ambiente para evitar que problemas em um 
jogo afetem o outro.

## Ambiente
- **Virtualização**: VirtualBox, VM dedicada (TerraVM) com Ubuntu Server 24.04 LTS
- **Acesso remoto**: administração via SSH (autenticação por senha)
- **Jogadores**: ~6 pessoas conectando via IP público da VM

## Rede
- Configuração de **port forwarding** no roteador, com porta customizada: 
  porta padrão do Terraria (7777) redirecionada para 30956
- Configuração de **IP fixo** na VM, mesma abordagem usada na MineVM

## Atualizações
- O Steam atualiza automaticamente o jogo dos jogadores, sem opção de 
  permanecer em versão anterior
- Como o servidor precisa estar na mesma versão do jogo para manter 
  compatibilidade, isso obriga a atualização manual do servidor logo após 
  cada atualização do Steam
- Diferente do Minecraft, onde é possível atrasar a atualização por escolha 
  própria, no Terraria a atualização do servidor é reativa — determinada pelo 
  cliente, não pelo administrador
- Atualizações não são muito frequentes, o que reduz o impacto dessa limitação

## Backup
- Mesma rotina da MineVM: cópia manual do mundo para o PC local, depois 
  enviada ao Google Drive antes de reconstruções

## O que eu aprendi
- Gerenciamento de múltiplas VMs separadas por serviço, evitando dependência 
  entre ambientes diferentes
- Diferença entre ambientes com controle total de atualização (Minecraft) 
  e ambientes com atualização forçada por terceiros (Terraria via Steam), 
  e como isso muda a forma de administrar cada um
- Reaplicação de práticas de rede (port forwarding, IP fixo) de forma 
  consistente entre múltiplos servidores
