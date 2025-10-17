
# Alugo - Vite + React + Tailwind + Firebase (Auth, Firestore, Storage)

Projeto preparado para deploy na Vercel. Inclui autenticação (email), cadastro de imóveis com upload de imagem (Firestore + Storage).

## Passos iniciais (rápido)

1. Crie um projeto no Firebase: https://console.firebase.google.com/
2. Habilite Authentication -> Email/Password.
3. Habilite Firestore (modo produção com regras adequadas mais tarde).
4. Habilite Storage and create a bucket (default).
5. Vá em Project Settings -> SDK setup and config — copie as credenciais.

Defina as seguintes variáveis de ambiente na Vercel (Project Settings -> Environment Variables):
- VITE_FIREBASE_API_KEY
- VITE_FIREBASE_AUTH_DOMAIN
- VITE_FIREBASE_PROJECT_ID
- VITE_FIREBASE_STORAGE_BUCKET
- VITE_FIREBASE_MESSAGING_SENDER_ID
- VITE_FIREBASE_APP_ID

## Rodando localmente (opcional)
```bash
npm install
npm run dev
```

## Deploy na Vercel
1. Faça upload do conteúdo deste diretório no GitHub (ou use Upload Project na Vercel).
2. Em Vercel, importe o repositório e clique em Deploy.
3. Adicione as mesmas variáveis de ambiente no painel da Vercel.
4. O site estará ativo (ex: https://alugo.vercel.app)

## Observações de segurança
- Firestore e Storage devem ter regras que limitem escrita apenas a usuários autenticados.
- Para produção, revise regras do Firestore e do Storage, e habilite cobrança no Firebase se necessário.
