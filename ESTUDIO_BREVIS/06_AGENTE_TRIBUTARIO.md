# AGENTE TRIBUTÁRIO — BREVIS TRIBUTÁRIO
### Linha editorial semanal · Criado em: 03/11/2026

> Pedido do Jean em 03/11/2026: uma linha só de tributário, pensando na reforma tributária e nas regras de transição, no mesmo estilo das outras, para o pessoal acompanhar sem misturar com o "geralzão". O Brevis Semanal continua cobrindo cível, criminal e as demais áreas.

## INSTRUÇÃO PARA A IA

Leia junto: `01_AGENTE_EDITORIAL.md` (§8 precisão, §11 lições, §13 dupla verificação, §14 layout v2), `05_AGENTE_VERIFICADOR.md` e `04_AGENTE_ARQUIVO.md` (reciclagem entre as TRÊS linhas). Nenhuma edição sai sem a dupla verificação. Se alguma camada não puder ser feita, não publique: salve o rascunho, avise o Jean e espere.

## 1. Identidade

- **Nome:** Brevis Tributário. **Periodicidade:** semanal, às **quartas-feiras** (decisão do Jean em 03/11/2026). A edição nº 001 saiu em 03/11/2026 (terça) como lançamento; a nº 002 está prevista para 11/11/2026.
- **Arquivo:** `brevis-tributario-edicaoNNN-AAAA-MM-DD.html` (ex.: `brevis-tributario-edicao001-2026-11-03.html`).
- **Paleta:** verde-escuro e cobre. Variáveis: `#0C2A20` (escuro), `#1C4A39` (médio), `#2F7D5F` (claro), `#B8742F` (cobre), `#E8B882` (cobre claro), fundo `#08170F`. O arquivo é gerado a partir do modelo do Previdenciário (layout v2), trocando as cores e acrescentando as etiquetas `t-trib`, `t-rfb`, `t-cgibs`, `t-conf`, `t-gov`.
- **Cobertura:** (a) reforma tributária do consumo: EC 132/2023, LC 214/2025, LC 227/2026, CBS, IBS, Imposto Seletivo, Comitê Gestor do IBS (CGIBS), alíquotas de referência, regimes específicos, Simples, split payment, notas fiscais, calendário de transição (2026 a 2033); (b) tributário geral: STF, STJ, CARF, PGFN, Receita Federal, ICMS e Confaz, ISS, ITBI, PIS/Cofins, IRPJ/CSLL, IRPF e dividendos, transação, prescrição, execução fiscal.
- **Público:** advogados tributaristas e de empresas; foco em prazos, janelas de regularização e riscos para clientes.

## 2. Fontes (ordem de confiança)

1. Portal do STF (andamento e decisões), Notícias do STF, STJ, TST quando houver reflexo tributário.
2. Texto do ato: Planalto, DOU, `normasinternet2.receita.fazenda.gov.br` (editais, portarias, instruções normativas da Receita), site do CGIBS (atos e PDFs), Confaz, Senado, Câmara, TCU.
3. Notícias oficiais: Receita Federal, Agência Brasil, Agência Senado.
4. Pistas (marcar como fonte secundária): Pimentel e Rohenkohl, Cescon Barrieu, Felsberg, ConJur, Migalhas /quentes/, Portal Reforma Tributária, substituicaotributaria.com, Guia Tributário, CBIC, IBDT.
5. ChatGPT e Gemini só como auditores, nunca como fonte.

Observação do ambiente (edição 001): os agentes de pesquisa não abriram portal do STF, Planalto, Confaz nem DOU. O STF abre no Chrome; os editais da Receita abrem pela cópia de `rotadajurisprudencia.com.br` ou por `curl`; PDFs do CGIBS baixam por `curl` e leem com `pdftotext`. Leia o texto do ato sempre que conseguir.

## 3. Regras próprias da linha

1. **Anúncio não é ato.** Declaração de ministro, "MP deve sair" e proposta em discussão entram como acompanhamento com a ressalva visível, sem alíquota, prazo ou número que não esteja no texto. Reverificar o DOU no dia da publicação.
2. **Convênio autoriza, não concede.** Convênio do Confaz só vale com ratificação e depende de lei ou decreto de cada Estado; confira o Ato Declaratório e a norma estadual antes de aconselhar.
3. **Edital e portaria:** ler o texto do edital; portaria que só prorroga prazo não traz as condições. Público do edital (por exemplo, o Edital RFB 10 é restrito) e efeitos da adesão (desistência, renúncia) entram no conselho.
4. **Calendário da reforma:** separar publicação, vigência, produção de efeitos e aplicação. Alíquota de referência calculada pelo TCU não é alíquota fixada pelo Senado.
5. **Pauta de tribunal:** citar órgão e incidente (embargos, agravo interno, mérito). Data de pauta pode mudar. Tema com mérito já julgado volta à pauta por recurso sobre modulação, não como julgamento novo.
6. **Conselho de esperar:** se o prazo prescricional ou de adesão corre, não aconselhar a esperar o fim do julgamento.
7. **Reciclagem:** itens de reforma que já saíram no Brevis Semanal entram aqui como acompanhamento, com remissão (ex.: TCU/CBS 11,3% e opção do Simples, Semanal 017). Itens tributários do Semanal e do Tributário não devem repetir o mesmo fato como novidade.
8. Quatro a seis movimentos por edição; o radar recebe pautas, acompanhamentos e itens de fonte única; "O que deixamos de fora" sempre presente.

## 4. Fluxo de cada edição (quarta-feira)

1. Pesquisa em paralelo (reforma e tributário geral), janela de 7 a 14 dias. Agentes não abrem sites do governo: confirmar eu mesmo no Chrome ou por `curl`.
2. Redação no layout v2 (modelo: `brevis-tributario-edicao001-2026-11-03.html`; gerado por script a partir do modelo do Previdenciário com a paleta verde e cobre).
3. Dupla verificação (`05_AGENTE_VERIFICADOR.md`): conferência própria, agente verificador independente, ChatGPT e Gemini, reverificação de cada apontamento. Registrar o que cada um pegou e o que foi rejeitado.
4. Publicação: subir o HTML e o `index.html` em github.com/brevis-newsletter/brevis (branch main), atualizar `04_AGENTE_ARQUIVO.md`, conferir no ar.

## 5. Como atualizar o index (desde 03/11/2026)

O `index.html` agora é dirigido por dados: três "portas" (Geral, Previdenciário, Tributário) e uma lista pesquisável com todas as edições. Para cada edição nova:
- acrescentar um objeto na matriz `E` do script (campos `l` linha: `geral`, `prev`, `trib` ou `especial`; `n` número; `d` data AAAA-MM-DD; `t` título; `m` assuntos separados por " · "; `h` arquivo);
- atualizar a porta da linha (edição, data, título e resumo) e a data em "Atualizado em".
A etiqueta "Nova" aparece sozinha por oito dias. Não apagar edições antigas.

## 6. Edições

| Nº | Data | Arquivo | Observação |
|----|------|---------|------------|
| 001 | 03/11/2026 | brevis-tributario-edicao001-2026-11-03.html | Lançamento. Ver `04_AGENTE_ARQUIVO.md`. |

---

*Estúdio Brevis · Agente Tributário · v1.0 · 03/11/2026*
