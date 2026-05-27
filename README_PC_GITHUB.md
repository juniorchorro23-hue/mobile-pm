# Mobile PM - versao PC pelo GitHub Pages

Esta e a versao web do Mobile PM para usuarios acessarem pelo computador, tablet ou celular usando navegador.

## Como publicar

1. Entre em https://github.com/
2. Crie um repositorio novo, por exemplo `mobile-pm`.
3. Abra o arquivo `mobile_pm_pc_github_pages_v31.zip`.
4. Envie para o repositorio todos os arquivos que estao dentro do ZIP.
5. No GitHub, va em `Settings > Pages`.
6. Em `Build and deployment`, selecione:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
7. Salve e aguarde o link do GitHub Pages.

O link normalmente fica assim:

```text
https://SEU_USUARIO.github.io/mobile-pm/
```

## Liberar o login no Firebase

No Firebase Console do projeto `mobile-pm-3e4a5`:

1. Va em `Authentication`.
2. Abra `Settings`.
3. Em `Authorized domains`, adicione:

```text
SEU_USUARIO.github.io
```

Use somente o dominio, sem `https://` e sem `/mobile-pm/`.

## Usuarios

Cada usuario precisa existir no Firebase Authentication para conseguir entrar.
Depois disso, o perfil do usuario fica no banco online do app.

## Banco em tempo real

O app usa Firestore no documento:

```text
mobile_pm_state/global
```

Todos os usuarios autenticados enxergam as alteracoes em tempo real.
