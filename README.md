# Controle de Mesas de Sinuca

Sistema simples (1 arquivo HTML, sem servidor, sem instalação) para controlar as 4 mesas com sessão fixa de 1 hora cada.

## O que faz
- Cada mesa tem um botão **▶ Iniciar 1h** que começa a contagem regressiva de 60:00.
- **↺ Zerar** interrompe a mesa a qualquer momento, mesmo antes de terminar a hora.
- Quando o tempo de uma mesa chega a zero: toca um alarme sonoro, o card e o ícone da mesa piscam em vermelho, e (se você ativar) aparece uma notificação do navegador — mesmo com a aba minimizada.
- **Mapa do Salão** no topo mostra as 4 mesas com uma cor por status: cinza (livre), dourado (em jogo), vermelho piscando (hora encerrada, aguardando zerar).
- O progresso fica salvo no navegador (localStorage): se der refresh na página sem querer, o tempo continua contando certinho de onde estava.

## Como colocar no GitHub (GitHub Pages)
1. Crie um repositório novo no GitHub (ex: `controle-sinuca`).
2. Suba o arquivo `index.html` para a raiz do repositório.
3. Vá em **Settings → Pages**, em "Source" escolha a branch `main` e a pasta `/ (root)`, salve.
4. Em alguns segundos o GitHub te dá um link tipo `https://seu-usuario.github.io/controle-sinuca/` — esse é o sistema já no ar, funcionando em qualquer computador, tablet ou celular com esse link.

Não precisa de banco de dados, backend nem custo nenhum — é só esse arquivo.

## Observações
- O alarme sonoro só toca se a aba estiver aberta no navegador; o navegador pode pedir para você interagir com a página uma vez antes de liberar som (clique em qualquer botão para "destravar").
- Clique em **"Ativar avisos de fim de hora"** uma vez para permitir notificações do sistema operacional (aparecem mesmo com a aba em segundo plano).
- Se quiser deixar isso fixo numa tela do balcão, é só abrir o link em tela cheia (F11) num navegador — funciona bem em um monitor ou tablet dedicado.
- Cada mesa é independente: dá pra ter 2 mesas rodando e 2 livres ao mesmo tempo, sem problema.
