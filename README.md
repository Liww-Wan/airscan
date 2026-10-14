# Passe

Envio de arquivos entre aparelhos, de navegador a navegador (WebRTC), sem servidor e sem nuvem. O pareamento é feito por QR code ou link.

## Publicar no GitHub Pages

1. Crie um repositório público no GitHub.
2. Envie o arquivo `index.html` para a raiz do repositório.
3. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`.
4. Aguarde um minuto e abra `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

O site precisa estar em HTTPS (o GitHub Pages já está) para a câmera funcionar.

## Como usar

1. No aparelho A, toque em **Criar conexão**. Aparece um QR.
2. No aparelho B, aponte a câmera do celular para o QR e abra o link. O aparelho B mostra um QR de resposta.
3. No aparelho A, toque em **Escanear QR com a câmera** e aponte para o QR do aparelho B. Se não tiver câmera, use **Copiar código** em B e cole no campo em A.
4. Conectados, os dois lados podem enviar arquivos.

## Limitações

- Não há servidor TURN. Em redes que bloqueiam conexão direta (algumas redes corporativas, 4G com NAT restritivo), a conexão pode falhar. Na mesma rede Wi-Fi funciona na maioria dos casos.
- Com a opção de redes diferentes ligada, o navegador consulta um servidor STUN do Google apenas para descobrir o endereço público. Nenhum arquivo passa por ele. Desmarque a opção para evitar isso (só funciona na mesma rede).
- Os arquivos recebidos são gravados no armazenamento privado do navegador quando ele suporta isso. Caso contrário, ficam na memória, e arquivos de vários GB podem travar o celular.
- Mantenha as duas telas abertas durante o envio.

## Licenças

Embute `qrcode-generator` (MIT) e `jsQR` (Apache-2.0).
