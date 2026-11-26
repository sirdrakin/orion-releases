# Orion Gestão Empresarial 2.3.1

## Novo: assistente de primeira instalação

- Abertura guiada em instalações novas, sem modificar automaticamente bases antigas.
- Escolha entre **uso individual**, **PC principal (servidor)** e **PC secundário (cliente)**.
- Cadastro inicial da empresa, responsável, endereço, telefone e logo.
- Criação de usuário **Administrador**, com senha.
- Configuração de backups automáticos, intervalo e retenção.
- Canal de atualizações sugerido: `sirdrakin/orion-releases`.
- Pareamento do computador secundário pelo código `ORION-LAN-...`.
- Continuação de configurações interrompidas, preservando o administrador já criado.
- Administradores podem reabrir o assistente em Configurações.

## Compatibilidade

- Mantidos os registros anteriores de vendas, caixa, estoque, clientes, produtos, pedidos, orçamentos, recibos e usuários.
- Caminho de dados mantido: `%LOCALAPPDATA%\CaixaCertoDesktop`.
- Modo individual continua funcionando sem internet.
- Para rede local, todos os computadores devem usar a mesma versão do Orion.

## Atenção

- Faça um **backup completo** antes de atualizar.
- O modo rede ainda não foi validado entre dois computadores Windows físicos: **pré-lançamento para testes**, não recomendado para produção em rede.
- A Central de Atualizações consulta lançamentos **estáveis** do GitHub; pré-lançamentos não aparecem como atualização automática.
- Não compartilhe publicamente backups ou códigos de pareamento.

## Arquivos de publicação

- `Orion-Instalador-v2.3.1.exe` — instalação Windows 64 bits.
- `Orion-Desktop-v2.3.1.exe` — executável portátil.
- `SHA256SUMS.txt` — hashes para verificação de integridade.

Os arquivos devem ser anexados ao **Release v2.3.1**, não adicionados ao repositório como arquivos comuns.
