# Configuração: Melhor Look Nostálgico

A página usa Firebase (plano gratuito) para login, fotos e notas compartilhadas.

## 1. Criar o projeto
1. Acesse https://console.firebase.google.com com uma conta Google sua.
2. **Adicionar projeto** → nome: `farra-deizon` → desative o Google Analytics → **Criar**.

## 2. Ativar login por e-mail e senha
1. Menu **Authentication** → **Começar** → **Email/Password** → ative → **Salvar**.

## 3. Criar o banco
1. Menu **Firestore Database** → **Criar banco de dados** → modo **produção** → escolha a região `southamerica-east1`.
2. Aba **Regras**: apague o conteúdo e cole o conteúdo de `firestore.rules` → **Publicar**.

## 4. Conectar a página
1. Ícone **</>** (Web) na tela inicial do projeto → registre o app (sem Hosting).
2. Copie o objeto `firebaseConfig` que aparece e cole em `index.html`, substituindo os valores `COLE_AQUI`.

## 5. Criar o perfil do fotógrafo (Fernando)
1. **Authentication** → **Users** → **Add user** → e-mail e senha do Fernando.
2. Copie o **User UID** que aparece na lista.
3. **Firestore Database** → **Iniciar coleção** → ID `usuarios` → ID do documento = o UID copiado.
4. Campos: `nome` (string) = `Fernando`, `papel` (string) = `fotografo`.

## 6. Como a trinca entra
- Cada uma acessa a página e clica em **Primeira vez? Criar conta**.
- Seleciona o próprio nome (Cris, Deizon ou Nayara), informa e-mail e senha (mínimo 6 caracteres).
- As regras só aceitam esses três nomes, com papel de jurado. Qualquer outro nome é recusado pelo servidor.

## 7. Publicar no GitHub Pages
- Só depois de configurar: o `index.html` com as chaves e as regras publicadas.
- O repositório pode ser público: as fotos e as notas ficam no Firebase, atrás de login, e não no código.
  A chave do Firebase também pode ficar pública; quem protege os dados são as regras publicadas.
- No GitHub, em Settings → Pages, escolha a branch `main` e a pasta `/ (root)`. O link sai em alguns minutos.
