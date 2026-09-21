# Site — Dr. Daniel Leles da Silveira

Site institucional de um médico com atendimento online. Site estático (HTML + CSS + JS), sem backend. O agendamento é feito pelo WhatsApp.

- **Hospedagem:** Vercel
- **Domínio:** (preencher quando registrar)
- **Contato do cliente:** WhatsApp (31) 99547-1130 — somente mensagens

## Estrutura

```
.
├── index.html        # página única do site
├── privacidade.html  # política de privacidade (LGPD)
├── robots.txt        # instruções para buscadores
├── sitemap.xml       # mapa do site (trocar o domínio)
├── vercel.json       # cabeçalhos de segurança e cache
└── img/              # fotos reais do médico (ver img/LEIA-ME.txt)
```

## Rodar localmente

Abrir `index.html` no navegador já funciona. Para um servidor local (recomendado, porque caminhos absolutos como `/privacidade.html` funcionam igual à produção):

```bash
python3 -m http.server 5500
# acesse http://localhost:5500
```

## Antes de publicar

- [x] Colocar as fotos reais em `img/` (ver `img/LEIA-ME.txt`)
- [ ] Trocar `https://www.drdanielleles.com.br/` pelo domínio real em `index.html` (canonical + og:url + JSON-LD), `robots.txt` e `sitemap.xml`
- [ ] Revisar com o médico os textos marcados com `<!-- EDITE -->`
- [ ] Confirmar o texto com as regras de publicidade médica do CFM/CRM-MG
- [ ] Conferir se o número do WhatsApp abre a conversa certa

## Fluxo de trabalho com branches

```bash
git switch -c feat/nome-da-mudanca   # cria a branch
# ... edita ...
git add -A && git commit -m "feat: descrição curta"
git push -u origin feat/nome-da-mudanca
# abre o Pull Request no GitHub, confere o Preview da Vercel, faz merge em main
```

`main` é sempre o que está no ar. Nunca se edita `main` direto.
