# AGENTE VERIFICADOR — BREVIS NEWSLETTER
### Roteiro da dupla verificação · Criado em: 20/10/2026

> "Essas notícias são sérias, a gente não pode errar. Sempre faça uma dupla verificação." — Jean Barbosa, 20/10/2026

## INSTRUÇÃO PARA A IA

Este roteiro vale para toda edição do Brevis (Semanal, Previdenciário ou Especial). **Nenhuma edição é publicada sem passar por ele.** Se alguma etapa não puder ser feita, não publique: avise o Jean, diga o que faltou e espere a decisão dele.

Leia junto: `01_AGENTE_EDITORIAL.md` (§8 precisão, §11 lições, §13 dupla verificação) e `04_AGENTE_ARQUIVO.md` (reciclagem).

---

## 1. As duas camadas

**Camada 1 — Verificação própria na fonte** (quem escreve a edição). Cada número de processo, tema, data, relator, placar, valor e prazo é conferido em fonte primária ou quase primária antes de entrar no texto.

**Camada 2 — Verificação independente** (quem não escreveu a edição):
1. **Agente verificador Claude**, em contexto limpo, lê o HTML pronto e confere tudo na web.
2. **ChatGPT e Gemini** recebem o resumo dos fatos e apontam dúvidas.
3. Quem escreveu a edição **reverifica cada apontamento na fonte** antes de aceitar ou rejeitar.

Só publica quando as duas camadas estiverem concluídas e o resultado estiver registrado.

---

## 2. Prompt-modelo do agente verificador (Claude)

Usar um agente novo (sem o histórico da redação), com acesso à web. Não passar a conclusão desejada; passar o arquivo e os itens.

```
Você é revisor jurídico independente. Leia <CAMINHO DO HTML> (newsletter jurídica, edição de <DATA>,
período <INÍCIO–FIM>) e verifique CADA afirmação factual na web (WebSearch/WebFetch; prefira STF, STJ,
TST, TNU, CJF, Planalto, Senado, Câmara, Migalhas /quentes/, IBDP, IEPREV, Lex, escritórios).
Itens: <LISTA DOS MOVIMENTOS COM NÚMERO, DATA, PLACAR, RELATOR>.
Aponte: erros, datas e placares divergentes, afirmações sem fonte, excesso de certeza e conselhos
práticos arriscados. Para cada achado dê a fonte (URL). Não edite arquivos.
Responda em lista curta: CONFIRMADO / CORRIGIR / NÃO VERIFICÁVEL.
```

Para edições de maior porte ou com muitos itens sensíveis, usar **dois verificadores com recortes diferentes** (por exemplo, um para STF/STJ e outro para atos normativos e prazos) e comparar os resultados.

Observação de método: o WebFetch resume a página com um modelo menor e pode introduzir inferência. Para citação literal ou dado fino, buscar o texto bruto ou uma segunda fonte.

---

## 3. Checklist do verificador (por item)

- **Existência:** o fato existe na fonte? Número de processo, tema, norma e órgão corretos?
- **Datas:** data do julgamento, da publicação do acórdão (DJe) e da notícia, separadas. Se divergirem, citar as duas. Procurar a primeira notícia do mesmo fato.
- **Placar e votos:** usar o resultado mais recente; distinguir parcial de final; conferir vencidos, impedidos e ausentes.
- **Relator:** relator original x relator do acórdão x redator designado.
- **Alcance:** a decisão é de Plenário, Turma, Seção, Corte Especial ou caso concreto? Cabem embargos? Há modulação? O acórdão saiu?
- **Atos normativos:** data da promulgação, da publicação no DOU e do início de vigência; exceções e regras de transição.
- **Valores e prazos:** percentuais, tetos, datas de adesão, públicos abrangidos; conferir em mais de uma fonte.
- **Ressalvas:** fonte única, divergência entre fontes e itens sem confirmação oficial estão sinalizados no cartão?
- **Conselho prático:** o "O que fazer na carteira" vai além do que a fonte permite? Se o acórdão não saiu, trocar "ajuíze/encerre" por "avalie/aguarde a tese final".
- **Reciclagem:** o item já saiu em qualquer edição das DUAS linhas ou no radar anterior? Se saiu, entra só como acompanhamento.
- **Opinião x notícia:** o link é cobertura factual (Migalhas /quentes/, Jota factual) ou coluna de opinião?
- **Mecânica do HTML:** contagem de `<div>` abertos e fechados, rodapé, script e `</html>` presentes, "N movimentos" do cabeçalho batendo com o real, links das fontes abrindo.

---

## 4. Auditoria externa (ChatGPT e Gemini)

Técnica que funcionou: digitar o resumo dos fatos em blocos curtos, em ASCII e sem acento, no ChatGPT (`chatgpt.com`) e no Gemini (`gemini.google.com/app`), terminar com "Liste somente o que estiver errado ou duvidoso", enviar e esperar a resposta (o Gemini pode levar mais de um minuto). Ler com a extração de texto da página.

Como usar a resposta:
- É **pista**, não veredito. Os dois já erraram por usar informação desatualizada e já acertaram pontos que a apuração tinha deixado passar.
- Para cada apontamento: reverificar na fonte, anotar **aceito** ou **rejeitado** e o motivo.
- Quando só um dos dois aponta e a fonte não confirma, tratar como "não confirmado" e manter a ressalva no texto.

---

## 5. Registro obrigatório (ao fim de cada edição)

Anotar em `04_AGENTE_ARQUIVO.md` (nota de correção editorial):
1. O que cada verificação pegou (e a fonte).
2. O que foi rejeitado e por quê.
3. Itens que ficaram com ressalva no texto publicado.
4. Lições novas, que sobem para `01_AGENTE_EDITORIAL.md` §11 quando forem recorrentes.

---

## 6. Regras de ouro

1. Nunca aceitar correção às cegas, venha de IA, do verificador ou do Jean: reverificar na fonte.
2. Data real do julgamento, não a da busca nem a da notícia.
3. Resultado mais recente, não o primeiro que apareceu.
4. Fontes divergentes: dizer que divergem.
5. Sem confirmação, não publica; ou publica com a ressalva visível.
6. O conselho prático não passa da fonte.
7. Na dúvida entre publicar rápido e publicar certo, publica certo.

---

*Estúdio Brevis · Agente Verificador · v1.0 · 20/10/2026*
