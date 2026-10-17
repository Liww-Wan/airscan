# Passe

Envio de arquivos entre aparelhos, de navegador a navegador (WebRTC), por link. Os arquivos não passam por servidor nem nuvem.

## Publicar no GitHub Pages

1. Crie um repositório público no GitHub e envie o `index.html` para a raiz.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`.
3. Abra `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

O site precisa estar em HTTPS (o GitHub Pages já está).

## Como usar

1. No aparelho A, toque em **Criar link de conexão** e envie o link ao aparelho B (WhatsApp, e-mail etc.).
2. No aparelho B, abra o link. A conexão é feita sozinha. Se preferir, abra o site e cole o link em **Tenho um link**.
3. Conectados, os dois lados podem enviar arquivos. Mantenha as duas telas abertas.

O link vale enquanto a página do aparelho A estiver aberta e serve para uma única conexão.

## Arquivos grandes (mais de 4 GB)

- O envio lê o arquivo em pedaços, então o tamanho não é limitado pelo remetente.
- No **Chrome e no Edge** (PC e Android recente), arquivos de 256 MB ou mais mostram o botão **Salvar em…**: o arquivo é gravado direto no disco, no local escolhido.
- Nos demais navegadores, o arquivo vai para o armazenamento privado do navegador, se houver suporte, ou para a memória. Para arquivos de vários GB, receba no Chrome ou no Edge.

## Privacidade e limites

- Para o link funcionar, os dois aparelhos trocam a conexão por um servidor público (ntfy.sh, definido na constante `SIGNAL` no início do script). Passam só mensagens criptografadas com AES-GCM; a chave fica na parte do link depois do `#`, que o navegador não envia a servidor algum. O arquivo nunca passa por ele. Se esse serviço estiver fora do ar, a conexão não é feita.
- Para trocar o serviço, aponte `SIGNAL` para seu próprio servidor ntfy.
- Com a opção de redes diferentes ligada, o navegador consulta um servidor STUN do Google apenas para descobrir o endereço público.
- Não há servidor TURN: em redes que bloqueiam conexão direta, a conexão pode falhar. Na mesma rede Wi-Fi funciona na maioria dos casos.
