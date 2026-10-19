# Ossu — gerar o APK sem Android Studio

Você só precisa de uma conta gratuita no GitHub. O APK é montado na nuvem.

1. Acesse github.com, crie uma conta e clique em **New repository**. Nome: `ossu`. Marque **Private** e crie.
2. Clique em **uploading an existing file**. Descompacte este zip no computador e arraste TODO o conteúdo (incluindo a pasta `.github`, `www` e `assets`) para a página. Clique em **Commit changes**.
   - Se a pasta `.github` não subir: clique em **Add file > Create new file**, digite `.github/workflows/build-apk.yml` no nome e cole o conteúdo do arquivo.
3. Abra a aba **Actions**, escolha **Build APK** e clique em **Run workflow**. Leva uns 5 a 10 minutos.
4. Quando ficar verde, abra a execução e baixe **ossu-apk** em *Artifacts*. Descompacte: o arquivo é `app-debug.apk`.
5. Envie o `.apk` por WhatsApp ou Drive. Quem instalar precisa permitir "instalar apps desconhecidos" e pode ver um aviso do Play Protect (normal para APK fora da loja).

## Atualizar o app
Troque `www/index.html` no GitHub (lápis > colar o novo código) e rode o workflow de novo.

## Para vender na Google Play
Este APK é de teste (debug). Para a loja é preciso gerar um pacote assinado (AAB), com conta Play Console (taxa única de US$ 25), política de privacidade e teste fechado com 12 pessoas por 14 dias. Para assinatura paga, use a versão Flutter (ossu-flutter-starter.zip), que tem Google Play Billing e login por WhatsApp.
