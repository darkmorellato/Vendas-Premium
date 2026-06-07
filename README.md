# PR Analytics Dashboard

Dashboard executivo para análise de vendas e mix de produtos.

## Estrutura de Arquivos

```
├── index.html          # Dashboard principal
├── pr.jpg             # Logo da empresa
├── dados/
│   ├── dados.json     # Arquivo combinado com todos os meses (usado pelo dashboard)
│   ├── maio2026.json  # Dados de Maio 2026 (arquivo separado)
│   ├── abril2026.json # Dados de Abril 2026 (arquivo separado)
│   ├── mar2026.json   # Dados de Março 2026 (arquivo separado)
│   ├── fev2026.json   # Dados de Fevereiro 2026 (arquivo separado)
│   ├── jan2026.json   # Dados de Janeiro 2026 (arquivo separado)
│   ├── dez2025.json   # Dados de Dezembro 2025 (arquivo separado)
│   ├── nov2025.json   # Dados de Novembro 2025 (arquivo separado)
│   └── out2025.json   # Dados de Outubro 2025 (arquivo separado)
```

## Como usar

1. **Visualização**: Abra o `index.html` em qualquer navegador moderno.
2. **Navegação**: Use o menu lateral para alternar entre:
   - Visão Geral (KPI, gráficos e tabela)
   - Categorias & Mix (performance por categoria)
   - Comparativo Mensal (evolução e tendências)

3. **Atualização de dados**: Para atualizar ou adicionar novos meses:
   - Edite os arquivos JSON individuais na pasta `dados/` (ex: `maio2026.json`)
   - O arquivo `dados/dados.json` é gerado automaticamente contendo todos os meses
   - O dashboard lê o `dados/dados.json` combinado
   - A ordem de exibição é controlada pela chave `_ordem_exibicao` dentro do `dados/dados.json`

## Adicionando um novo mês

1. Copie um arquivo existente (ex: `fev2026.json`) e renomeie (ex: `jun2026.json`)
2. Altere o conteúdo:
   - `label`: Nome do mês e ano
   - `total`: Total de itens no mês
   - `data`: Lista de produtos com `name`, `quantity`, e `percentage`
3. Reconstrua o `dados/dados.json` incluindo a nova chave no início da lista `_ordem_exibicao`
4. Recarregue o dashboard no navegador

## Tecnologias utilizadas

- HTML5, CSS3, JavaScript (ES6+)
- Tailwind CSS (via CDN)
- Chart.js para gráficos
- Lucide Icons

## Observações

- Os percentages são valores decimais (ex: 0.0213 = 2,13%)
- Categorias são detectadas automaticamente a partir do nome do produto
- Interface responsiva e otimizada para desktop

---

© 2026 PR Analytics Platform. Uso estritamente confidencial.