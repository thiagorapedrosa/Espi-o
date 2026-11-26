# Disfarce: jogo do impostor (Android)

Jogo de festa offline, sem anúncios e sem assinatura. Todo o jogo fica em
`app/src/main/assets/index.html`, e as figuras 3D em `app/src/main/assets/figuras.js`. O app Android é só uma "moldura" (WebView) que abre esse arquivo.

## Opção A: gerar o APK pelo GitHub (sem instalar nada)

1. Crie um repositório novo no GitHub e envie o conteúdo desta pasta (pode ser pelo site: "Add file > Upload files", arrastando tudo, inclusive a pasta `.github`).
2. Abra a aba **Actions**. O fluxo "Gerar APK" roda sozinho (leva uns 3 a 5 minutos).
3. Quando terminar, clique na execução e baixe **Disfarce-apk** na seção *Artifacts*. Dentro do zip está o `app-debug.apk`.
4. Passe o APK para o celular e abra. O Android vai pedir para permitir "instalar apps desta fonte".

## Opção B: Android Studio

1. Instale o Android Studio e abra esta pasta (File > Open).
2. Espere o Gradle sincronizar.
3. Menu **Build > Build App Bundle(s) / APK(s) > Build APK(s)**.
4. O APK sai em `app/build/outputs/apk/debug/app-debug.apk`.

## Personalizar

- **Palavras e categorias:** edite o bloco `const CATS = { ... }` no `index.html`. Cada palavra é "figura + nome | dica", por exemplo `🐶 Cachorro|Melhor amigo de muita gente` (a dica não pode ter vírgula). Também dá para criar categorias dentro do próprio jogo (botão "+ Criar").
- **Nome do app:** `app/src/main/res/values/strings.xml`.
- **Identificador do app:** `applicationId` em `app/build.gradle` (troque antes de publicar).

## Publicar na Play Store (opcional)

O APK de debug serve para instalar no seu celular e no dos amigos. Para a Play Store, gere um
*Android App Bundle* assinado (Build > Generate Signed App Bundle) e crie uma conta de desenvolvedor no Google Play Console.

## Créditos das figuras

As figuras 3D são o Fluent Emoji da Microsoft, distribuído sob a licença MIT (veja `LICENCA-FIGURAS.txt`).
Os nomes de personagens são usados só como palavras do jogo.
