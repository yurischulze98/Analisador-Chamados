# Analisador de Chamado - Gemini + Vercel

Projeto simples para transformar uma anotacao bruta do analista em dois textos:

1. Atualizacao para CRM: texto mais completo, entre 3 e 10 linhas.
2. Justificativa para SLA: texto mais resumido, ate 4 linhas, sem copiar o texto original.

## Estrutura

```text
analisador-chamado-gemini/
├── api/
│   └── analisar-chamado.js
├── public/
│   ├── index.html
│   ├── styles.css
│   └── app.js
├── package.json
├── .env.example
└── .gitignore
```

## Variaveis de ambiente

No Vercel, cadastre:

```env
GEMINI_API_KEY=sua_chave_do_gemini
GEMINI_MODEL=gemini-2.5-flash
```

## Rodar localmente

Instale as dependencias:

```bash
npm install
```

Crie o arquivo .env.local:

```bash
cp .env.example .env.local
```

No Windows PowerShell:

```powershell
copy .env.example .env.local
```

Coloque sua chave real no arquivo .env.local.

Depois rode:

```bash
npm run dev
```

Acesse:

```text
http://localhost:3000
```

## Publicar no Vercel

1. Suba esta pasta para um repositorio no GitHub.
2. Acesse o Vercel.
3. Clique em Add New Project.
4. Importe o repositorio.
5. Em Environment Variables, cadastre GEMINI_API_KEY e GEMINI_MODEL.
6. Clique em Deploy.

Nao envie .env ou .env.local para o GitHub.
