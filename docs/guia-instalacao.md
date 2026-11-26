# Guia de instalação — Orion Gestão Empresarial 2.3.1

## Baixar o Orion

Acesse [Releases oficiais](https://github.com/sirdrakin/orion-releases/releases). A versão estável mais recente fica em [Releases/latest](https://github.com/sirdrakin/orion-releases/releases/latest). Para testar a 2.3.1, selecione seu **pré-lançamento** na lista de Releases, quando publicado.

Em **Assets**, escolha `Orion-Instalador-v2.3.1.exe` para instalar no Windows 64 bits. Não é necessário baixar o código-fonte criado automaticamente pelo GitHub.

## Instalação em apenas um computador

1. Baixe o instalador oficial, execute e abra o Orion.
2. Em uma instalação nova, o **Assistente de configuração** é exibido automaticamente.
3. Escolha **Neste computador** (modo individual).
4. Informe os dados da empresa e crie a conta de administrador.
5. Configure os backups automáticos e finalize.

**Instalações antigas:** faça backup antes de atualizar. O assistente não reaparece automaticamente se já houver dados. Para revisá-lo, acesse **Configurações → Assistente de configuração**.

O caminho antigo `%LOCALAPPDATA%\CaixaCertoDesktop` permanece válido. **Não renomeie a pasta.**

## Rede local — computador principal

> O modo rede ainda precisa ser validado em dois computadores Windows reais. Use dados de teste.

1. Conecte os PCs à mesma rede privada, por cabo ou Wi-Fi.
2. No PC que armazenará os dados, entre como Administrador e faça um backup.
3. Em **Configurações → Computadores e rede local**, selecione **Compartilhar dados: PC principal**.
4. Salve com a porta padrão **38471** e reinicie o Orion.
5. Autorize o aplicativo no Firewall do Windows **somente para redes privadas**; se necessário, libere TCP **38471** apenas na LAN.
6. Volte à tela e clique em **Atualizar informações** para obter o código de pareamento `ORION-LAN-...`.

O PC principal deve permanecer ligado e com o Orion aberto para os secundários funcionarem.

## Rede local — computador secundário

1. Instale a mesma versão do Orion e conecte o PC à mesma rede privada.
2. Abra **Configurações → Computadores e rede local** e escolha **Conectar a um PC principal**.
3. Cole o código de pareamento fornecido pelo principal, salve e reinicie o Orion.
4. Acesse com uma conta criada no PC principal.

O secundário não trabalha offline com sincronização posterior: ele depende do principal.

## Checklist antes de usar de verdade

- [ ] Cliente de teste abre nos dois PCs.
- [ ] Uma venda criada no secundário aparece no principal.
- [ ] A baixa de estoque ocorre apenas uma vez.
- [ ] Usuários mantêm permissões próprias.
- [ ] Backup do banco principal é gerado e pode ser restaurado.

## Solução de problemas

- **Código não aparece:** reinicie o Orion no principal e clique em **Atualizar informações**.
- **Não conecta:** verifique rede privada, isolamento de Wi-Fi, Firewall TCP 38471 e PC principal aberto.
- **IP mudou:** gere outro código no principal.
- **Atualização não aparece:** confira o canal `sirdrakin/orion-releases`. A Central consulta apenas Releases estáveis, não pré-lançamentos.

**Segurança:** não abra a porta 38471 na internet nem publique códigos de pareamento ou backups financeiros.
