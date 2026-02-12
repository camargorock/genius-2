# Genius Webapp (Next.js + API)

Projeto full stack pronto para deploy no Vercel.

## Stack

- Next.js 14 (App Router)
- Frontend em `public/genius.html` (UI original convertida para consumir API)
- API em rotas serverless do Next (`app/api/*`)

## Login demo

- Email: `admin@genius.com`
- Senha: `password`

## Rodar local

```bash
npm install
npm run dev
```

Acesse `http://localhost:3000`.

## Deploy no Vercel

1. Suba esta pasta para um repositório GitHub.
2. No Vercel, importe o repositório.
3. Configure a variável de ambiente:
   - `JWT_SECRET`
4. Deploy.

## Estrutura

- `app/page.tsx`: redireciona para `genius.html`
- `public/genius.html`: frontend principal
- `app/api/auth/*`: login, sessão e logout
- `app/api/leads/*`: listagem e atualização de status no CRM
- `lib/*`: autenticação e store em memória

## Observação importante

Os dados estão em memória (`lib/data.ts`) para simplificar o bootstrap. Em ambiente serverless (Vercel), isso é efêmero. Se quiser persistência real, o próximo passo é conectar Supabase/Postgres.
