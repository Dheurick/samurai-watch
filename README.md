# Samurai Watch

Primeira versão experimental do painel web para o Btalk Lite.

## O que já está incluído
- Interface responsiva para celular e computador.
- Conexão Web Bluetooth (requer navegador compatível e HTTPS).
- Leitura de bateria pelo serviço padrão BLE, quando disponível.
- Escuta de frequência cardíaca pelo serviço padrão `180D / 2A37`.
- Ações experimentais de vibração, consulta de passos, firmware e mostrador, baseadas nos testes do protocolo MOYOUNG-V2.

## Limitações importantes
- O projeto ainda é experimental e não substitui um aplicativo médico.
- A leitura de frequência cardíaca apenas recebe notificações; não garante iniciar a medição no relógio.
- Comandos proprietários podem variar entre versões de firmware.
- O navegador pode exigir permissões Bluetooth e interação direta do usuário.
- Não há coleta, envio ou armazenamento de dados pessoais nesta versão.

## Publicar no GitHub Pages
1. Extraia o ZIP.
2. Envie `index.html` e `README.md` para a raiz do repositório `samurai-watch`.
3. No GitHub, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)`, depois clique em **Save**.
6. Aguarde a publicação. O endereço esperado será `https://dheurick.github.io/samurai-watch/`.

Abra a página no iPhone pelo Bluefy para testar Web Bluetooth.

## Estrutura
- `index.html` — aplicação web inicial.
- `README.md` — instruções e limitações.


## Diagnóstico Bluetooth
A interface inclui o botão **Exportar** na seção Registro técnico. Após conectar o relógio e executar os testes desejados, exporte o arquivo `.txt` e compartilhe-o para análise.
O registro inclui UUIDs GATT, propriedades das características, notificações BLE, comandos e valores de frequência cardíaca. Ele **não grava áudio** nem conteúdo do microfone.
Observação: navegadores Web Bluetooth podem limitar a enumeração de serviços e características aos serviços autorizados na solicitação de conexão. Perfis Bluetooth clássicos como HFP/áudio de chamadas normalmente não são enumeráveis por Web Bluetooth.
