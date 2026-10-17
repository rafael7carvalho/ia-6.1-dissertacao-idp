# ia-6.1: esqueleto didático de dissertação

Autor: Rafael Carvalho dos Santos. Programa: Mestrado Profissional em Administração Pública, IDP.

Este projeto deriva de `alexlopespereira/TemplateLatexIDP`. O conteúdo personalizado é um exercício da disciplina Agentes de IA baseado no Pré-Projeto 4 de “A política dos números”. Não é dissertação concluída, não contém resultados empíricos e não altera o documento original do projeto.

## Entrega para revisão

- `main.pdf`: 13 páginas, compiladas localmente a partir das fontes personalizadas.
- `config/dados.tex`: título e autoria reais; orientação, defesa e catalogação não foram inventadas.
- `capitulos/`: cinco capítulos, cada um com dois parágrafos autorais, além dos elementos demonstrativos.
- `pretextual/resumo.tex` e `abstract.tex`: resumos equivalentes do desenho proposto, sem resultados fabricados.
- Figura e tabela com legendas, fontes, rótulos próprios e chamadas no texto. A tabela contém parâmetros do recorte, não observações simuladas da pesquisa.
- `referencias.bib`: três obras acadêmicas verificadas e uma entrada adicional do documento autoral fornecido, usado na citação longa.
- `VERIFICACAO-REFERENCIAS.md`: fontes externas e limites da verificação.

Ficha catalográfica, aprovação, dedicatória, agradecimentos, epígrafe e anexos de exemplo não são incluídos no PDF. Os arquivos opcionais originais do template permanecem como material de origem, sem participação no texto compilado.

## Compilação efetivamente realizada

```text
latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error main.tex
```

Foi usada uma distribuição TeX Live 2026 portátil, fora do repositório, com os pacotes necessários. O caminho da ferramenta foi acrescentado somente ao PATH do processo de compilação, sem instalação global.

O Biber fornecido nessa distribuição não iniciou no Windows, com erro de realocação de DLL. O backend BibTeX simples também não atendia à exigência do estilo biblatex-abnt. A adaptação final substitui somente o bloco de bibliografia da classe por abntex2cite, carregado após hyperref, mantendo o restante da estrutura visual do IDP. A alteração está identificada em idp.cls. Usa-se o estilo autor-data do abnTeX2; não se afirma identidade entre todas as opções bibliográficas dos dois pacotes.

O fluxo concluído foi pdflatex, BibTeX e novas passadas de pdflatex, automatizadas por latexmk. O arquivo .bbl foi gerado pelo BibTeX, não escrito manualmente. O latexmk terminou com código zero e informou todos os alvos atualizados. O log final não contém erros LaTeX nem referências ou citações indefinidas. A alternativa BibTeX é expressamente admitida na rubrica da reflexão do ia-6.1.

A tentativa pelo compilador integrado do aplicativo não foi usada como prova de sucesso: ela falhou durante a preparação, com fontes alteradas ao longo da tentativa. A evidência de sucesso é a compilação local final.

## Estado atual

Material revisado e publicação autorizada pelo participante. Fork público criado em https://github.com/rafael7carvalho/ia-6.1-dissertacao-idp, derivado do template original. As fontes e o PDF deste commit constituem a entrega aprovada. A avaliação e a submissão ao autograde ainda não foram executadas.

O Pré-Projeto original, suas versões Word/PDF e materiais privados não integram esta entrega. A citação longa reproduz somente o trecho identificado na seção de referências, sujeito à revisão do autor antes da publicação.
