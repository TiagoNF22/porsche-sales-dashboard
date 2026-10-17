# Porsche Sales Intelligence Dashboard

Dashboard interativa em arquivo HTML único para explorar a base sanitizada de 100 vendas da Porsche. Usa HTML, CSS e JavaScript; gráficos renderizados com Chart.js via CDN.

## Acesse a dashboard

Depois de ativar o GitHub Pages, substitua o endereço abaixo pelo link publicado:

`https://github.com/TiagoNF22/porsche-sales-dashboard`

## Perguntas de negócio

1. **Quais modelos aparecem com maior volume de vendas em cada cidade?** O gráfico compara os modelos mais frequentes nas cidades com maior volume no recorte.
2. **Qual ano-modelo tem o maior número de vendas registradas?** O gráfico separa o ano-modelo do veículo do ano em que a venda aconteceu.
3. **Quais combinações de modelo e estado apresentam aumento, queda ou novos registros entre períodos comparáveis?** A tabela compara contagens em janelas equivalentes (1º de janeiro a 16 de outubro), mostrando diferença absoluta, variação percentual quando há base anterior e um aviso de tamanho da amostra.

## Filtros e indicadores

Filtros: modelo, ano-modelo do veículo, cidade, estado e método de pagamento. Os filtros atualizam os KPIs, gráficos de distribuição, insights e a tabela de comparação temporal.

KPIs: quantidade de vendas registradas, receita total, ticket médio e modelo líder. O painel de qualidade de dados conta datas inválidas, datas posteriores a 16/10/2026 e datas válidas até a data de referência.

## Tratamento dos dados

A dashboard usa exclusivamente os campos sanitizados da aba `Sanitized`: data de venda, modelo, ano-modelo, preço, método de pagamento, cidade, estado e status de entrega. Preço e ano-modelo são tratados como números; datas que não correspondem a `AAAA-MM-DD` são excluídas da análise temporal.

Na base fornecida, há **100 registros**, dos quais **24 datas inválidas** e **20 datas posteriores a 16/10/2026**. A data de referência está fixada em 16/10/2026 para que a publicação seja reproduzível. Essas 44 linhas continuam incluídas nos KPIs gerais, mas não entram nas comparações temporais. O comparativo limita cada ano a 1º de janeiro–16 de outubro para comparar janelas de igual duração e evitar utilizar datas futuras.

A dashboard incorpora os valores sanitizados no próprio HTML para funcionar sem carregar a planilha externa. Não publique informações sensíveis. Como a amostra contém poucas vendas para muitas combinações de estado e modelo, várias comparações são classificadas como amostra pequena; as diferenças são sinais descritivos, não prova de uma tendência de mercado.

## Prompt usado como ponto de partida

> Crie uma dashboard em um único arquivo HTML com CSS e JavaScript, usando os campos sanitizados da planilha de vendas da Porsche. Inclua filtros por modelo, ano-modelo do veículo, cidade, estado e método de pagamento; KPIs de vendas, receita, ticket médio e modelo líder; gráficos para modelos mais vendidos por cidade, vendas por ano-modelo, ranking de modelos e formas de pagamento; e uma seção de comparação temporal por combinação de modelo e estado. Compare janelas equivalentes até a mesma data do ano (1º de janeiro a 16 de outubro), exclua datas inválidas e posteriores à data de referência, e mostre diferença absoluta, variação percentual apenas quando houver base anterior e um indicador para amostras pequenas. Use um visual empresarial, minimalista e refinado, inspirado na identidade visual do site oficial da Porsche nos Estados Unidos, sem reproduzir logotipos ou afirmar afiliação oficial.

## Ferramentas e publicação

- **Ferramenta:** ChatGPT para elaborar e refinar o HTML a partir da planilha fornecida.
- **Formato:** arquivo HTML único (`index.html`), com os dados sanitizados incorporados.
- **Gráficos:** Chart.js carregado por CDN; requer conexão com a internet para renderizar os gráficos.
- **Hospedagem:** GitHub Pages, após configuração manual no repositório.

## Referência visual

Site oficial Porsche EUA: https://www.porsche.com/

## Limitações

- Os resultados representam apenas os 100 registros da planilha, não o mercado Porsche dos Estados Unidos.
- “Mais vendido” significa maior contagem de registros na seleção atual.
- A variação percentual não é calculada quando não há vendas no período anterior; um novo registro é rotulado como “Novo na janela”.
- Combinações com menos de cinco registros somados nos dois períodos são sinalizadas como “Amostra pequena”.
- A data de referência está fixada em 16/10/2026 para tornar explícitos os registros futuros na data da análise.
