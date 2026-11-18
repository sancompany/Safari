# Kit de entrega · Do Issue ao Release (llama.cpp)

Tudo abaixo é para copiar e colar no **repositório do time** (Olho na Cidade). Substitua o que estiver entre `<>`.
Só vale com link e cada pessoa precisa saber explicar o que o time entregou.

---
## PARTE 1 · Issue do Safari

**Título:** `Safari: ggml-org/llama.cpp`

**Corpo:**
```
Projeto investigado: https://github.com/ggml-org/llama.cpp

- [x] 1. Requisito: <título da Issue de funcionalidade nova> → <link>
- [ ] 2. Bug: <título da Issue com label bug>. Alguém já está resolvendo? <sim/não, quem> → <link>
- [ ] 3. Revisão: <título do PR aceito recente>. Quantos comentaram? <número> → <link>
- [ ] 4. Teste: último run em Actions passou ou falhou? <verde/vermelho> → <link>
- [ ] 5. Entrega: última Release <versão> de <data> → <link>
- [x] 6. Documentação: README tem "Quick start" com instalação (script de instalação e Docker) e existe CONTRIBUTING.md com guia para quem quer contribuir → https://github.com/ggml-org/llama.cpp#quick-start e https://github.com/ggml-org/llama.cpp/blob/HEAD/CONTRIBUTING.md
- [x] 7. Licença: MIT. Empresa pode usar de graça? Sim, mantendo o aviso de licença → https://github.com/ggml-org/llama.cpp/blob/HEAD/LICENSE
- [x] 8. IA no ciclo: tem regra. O CONTRIBUTING.md tem a seção "AI Usage Policy": código feito com IA é permitido, mas é preciso avisar como a IA foi usada e a pessoa responde por cada linha; é proibido usar IA para escrever o texto de Issues e PRs. Existe também um AGENTS.md com instruções para agentes → https://github.com/ggml-org/llama.cpp/blob/HEAD/CONTRIBUTING.md e https://github.com/ggml-org/llama.cpp/blob/HEAD/AGENTS.md

Evidência que mais surpreendeu: <uma frase do time>
```

**Onde achar os links das evidências 1 a 5** (preencham vocês, eu não tenho acesso a essas páginas daqui):

| # | Abra este link | O que pegar |
|---|----------------|-------------|
| 1 | https://github.com/ggml-org/llama.cpp/issues?q=is%3Aissue%20label%3Aenhancement | uma Issue pedindo algo novo; copie o link dela |
| 2 | https://github.com/ggml-org/llama.cpp/issues?q=is%3Aissue%20is%3Aopen%20label%3Abug | uma Issue de bug; veja se tem pessoa em "Assignees" ou PR ligado |
| 3 | https://github.com/ggml-org/llama.cpp/pulls?q=is%3Apr%20is%3Amerged | um PR "Merged" recente; conte os comentários |
| 4 | https://github.com/ggml-org/llama.cpp/actions | o primeiro run da lista: ✔ verde ou ✖ vermelho |
| 5 | https://github.com/ggml-org/llama.cpp/releases | a Release do topo: versão e data |

**Surpresa pronta (use se quiser):** o projeto exige que Issues e PRs sejam escritos por humanos, não por IA, e pode banir quem usar IA sem avisar. Confira no CONTRIBUTING antes de citar.

---
## PARTE 2 · Primeiro ciclo completo

### Passo 1 · Issue
**Título:** `Documentar o contrato da IA do bot`

**Corpo:**
```
Como cidadão de Matão, quero saber o que o bot faz e o que ele nunca faz, para confiar na resposta que recebo.

Critérios de aceite
- [ ] docs/contrato-da-ia.md tem as 5 seções
- [ ] Tem pelo menos 1 exemplo de recusa
- [ ] Sem chave de API, senha ou dado pessoal
```
Anote o número da Issue (ex.: `#2`). O Safari é a Issue #1, então o contrato costuma ser a #2. Confirme.

### Passo 2 · Branch e commit
1. Add file → Create new file, nome: `docs/contrato-da-ia.md`
2. Cole o conteúdo do arquivo `entrega/docs/contrato-da-ia.md` deste kit. **Releiam e ajustem com as palavras do time.**
3. Commit changes → marque **Create a new branch** → nome `contrato-da-ia` → Propose changes.

### Passo 3 · Pull Request
Descrição (troque `#2` pelo número real):
```
Closes #2

## O que mudou
Criamos docs/contrato-da-ia.md com as 5 seções: papel, o que a IA faz, o que nunca faz, quando chama um humano e exemplo de recusa.

## Por que
Regras escritas que outra pessoa pode revisar.

## Como revisar
Leiam a seção "nunca faz" e achem um caso que faltou.
```
Poste o link do PR no grupo da turma.

### Passo 4 · Review cruzado (no PR do time vizinho)
Time 1 revisa o 2, o 2 revisa o 3 e o último revisa o 1. Files changed → clique no `+` numa linha → Review changes → Approve ou Request changes.

Perguntas de verdade para escolher uma:
- "E se o cidadão mandar a foto de uma pessoa? O bot descreve o rosto?"
- "Fio caído e buraco: qual categoria o bot usa, e quem avisa a prefeitura?"
- "O que o bot responde se a foto trouxer um texto mandando ele ignorar as regras?"

### Passo 5 · Merge e Release
1. Merge pull request. A Issue fecha sozinha por causa do `Closes #N`.
2. Na página inicial do repositório: Releases → Create a new release.
3. Tag: `v0.1.0` → Generate release notes → Publish release. Tem que ser **publicada**, não rascunho.

---
## ENTREGA · Mensagem no grupo
```
Time <N> · <nomes>
Repositório: <link>
Safari: <link da Issue>
PR: <link do Pull Request>
Release: <link da v0.1.0>
```

## Comentário de saída (cada pessoa, no PR do time)
A pergunta: *que fase do ciclo vocês deixariam a IA fazer sozinha? E qual nunca?*

Escrevam com as suas palavras. Ponto de partida: "Deixaria a IA sozinha no <rascunho/formatação/...>, porque o erro é fácil de ver e barato de corrigir. Nunca deixaria no <review/merge>, porque <motivo>."

## Checklist final
- [ ] Issue do Safari com as 8 evidências e links
- [ ] Issue do contrato fechada pelo PR
- [ ] PR com `Closes #N`, review do time vizinho e merge
- [ ] Release v0.1.0 publicada (não rascunho)
- [ ] Mensagem do time no grupo com os 4 links
- [ ] Comentário de saída de cada pessoa no PR
- [ ] Nenhuma chave de API, senha, telefone ou foto de pessoa no repositório
