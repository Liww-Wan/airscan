# Airscan

Envio de arquivos grandes entre aparelhos, direto de navegador a navegador (WebRTC), sem nuvem. O pareamento é feito por QR code ou link.

## Publicar no GitHub Pages

1. Crie um repositório público no GitHub e envie o `index.html` para a raiz.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`.
3. Abra `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/` (precisa de HTTPS, que o GitHub Pages já oferece).

## Como usar

1. No aparelho A, toque em **Criar conexão**. Aparecem um QR e um link.
2. No aparelho B, aponte a câmera para o QR (ou use **Tenho um QR ou link** e **Escanear QR com a câmera**), ou cole o link.
3. Conectados, os dois lados podem enviar arquivos. Mantenha as duas telas abertas.
4. Se a conexão cair, toque em **Reconectar** para criar uma nova.

## Arquivos grandes

- No Chrome e no Edge, arquivos a partir de 256 MB mostram **Salvar em…** e são gravados direto no disco.
- Em outros navegadores, o arquivo vai para o armazenamento privado do navegador ou para a memória. Para vários GB, receba no Chrome ou no Edge.

## Privacidade e limites

- Para os aparelhos se encontrarem, a conexão é trocada por um serviço público (ntfy.sh, constante `SIGNAL` no início do script) com mensagens criptografadas (AES-GCM). A chave fica após o `#` do link, que o navegador não envia a servidor algum. Os arquivos nunca passam por ele.
- Com a opção de redes diferentes ligada, o navegador consulta um servidor STUN do Google só para descobrir o endereço público.
- Não há servidor TURN: redes que bloqueiam conexão direta podem impedir a conexão.
- Todo o texto da interface está na constante `T` no início do script (os textos fixos da página ficam no HTML).

## Licenças

Embute `qrcode-generator` (MIT) e `jsQR` (Apache-2.0).

## Repositório e licença

- O botão do GitHub no topo e os links do rodapé apontam para o repositório. No GitHub Pages o endereço é detectado sozinho; em outro domínio, edite a constante `REPO` no início do script.
- O ano do rodapé é atualizado automaticamente.
- O projeto usa a licença MIT (arquivo `LICENSE`). O ícone do GitHub vem do conjunto Octicons (MIT).
