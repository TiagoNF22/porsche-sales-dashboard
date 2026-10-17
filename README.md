# Porsche Sales Intelligence Dashboard

Dashboard interativa para explorar uma base sanitizada de 100 vendas da Porsche. O projeto usa HTML, CSS e JavaScript, com gráficos renderizados pelo Chart.js.

## Acesse a dashboard

Depois de ativar o GitHub Pages, substitua o endereço abaixo pelo link publicado:

`https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`

## Perguntas de negócio

1. **Quais modelos aparecem com maior volume de vendas em cada cidade?** Ajuda a identificar preferências locais na amostra analisada.
2. **Qual ano-modelo tem o maior número de vendas registradas?** Mostra quais anos-modelo concentram os registros no período representado pela base.
3. **Quais modelos lideram por estado e quais apresentam sinais de variação temporal?** O ranking estadual aponta os modelos com maior volume por estado; a comparação temporal é um sinal exploratório e não deve ser interpretada como prova de crescimento de mercado sem períodos comparáveis e amostra suficiente.

## Filtros e indicadores

Filtros disponíveis: modelo, ano-modelo, cidade e método de pagamento.

Indicadores de topo: número de vendas, receita total registrada, ticket médio e modelo líder no recorte selecionado.

## Tratamento dos dados

A dashboard foi montada usando os campos sanitizados da aba `Sanitized` da planilha do desafio. Foram utilizados os campos de data da venda, modelo, ano-modelo, preço, método de pagamento, cidade, estado e status de entrega. Preço e ano-modelo são tratados como valores numéricos; valores ausentes são apresentados como “Não informado” quando aplicável.

A base disponibilizada para este projeto contém 100 registros. Como se trata de uma amostra sanitizada, os resultados descrevem apenas os registros presentes na planilha e não necessariamente todo o mercado Porsche dos Estados Unidos. A dashboard não publica a planilha original separadamente: os dados usados estão incorporados no HTML.

## Prompt usado como ponto de partida

> Crie uma dashboard em um único arquivo HTML com CSS e JavaScript, usando os campos sanitizados da planilha de vendas da Porsche. Inclua filtros por modelo, ano-modelo, cidade e método de pagamento; KPIs de vendas, receita, ticket médio e modelo líder; gráficos para modelos mais vendidos por cidade, vendas por ano-modelo, ranking de modelos e distribuição por forma de pagamento; e uma tabela com o modelo líder por estado. Gere insights claros, distinguindo volume de vendas de crescimento temporal e explicando limitações quando os dados forem insuficientes. Use um visual empresarial, minimalista e refinado, inspirado na identidade visual do site oficial da Porsche nos Estados Unidos, sem reproduzir logotipos ou afirmar afiliação oficial.

## Ferramentas e publicação

- **Ferramenta:** ChatGPT para elaboração do HTML a partir da planilha fornecida.
- **Formato:** arquivo HTML único (`index.html`), com Chart.js carregado por CDN.
- **Hospedagem:** GitHub Pages, após configuração manual no repositório.

## Referência visual

Site oficial Porsche EUA: https://www.porsche.com/

## Limitações

- Os resultados dependem da qualidade, da cobertura temporal e do volume da base de 100 registros.
- “Mais vendido” significa maior contagem de registros na seleção atual.
- Uma diferença entre anos não comprova, por si só, aumento persistente de popularidade.
- O Chart.js é carregado por CDN; a primeira renderização dos gráficos requer conexão com a internet.
