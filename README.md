# � Análise de Meios de Transporte - CIESA

Um website profissional com **apresentação executiva** e **dashboard interativo** para análise de dados sobre mobilidade urbana dos alunos da instituição CIESA.

## 📋 O Que É

Uma aplicação web completa que funciona em três camadas:

1. **Hero/Apresentação**: Seção inicial atrativa com contexto da pesquisa
2. **Conteúdo Informativo**: Metodologia, dados e insights da pesquisa
3. **Dashboard Interativo**: Visualizações dinâmicas, gráficos e tabelas analíticas

A aplicação utiliza o arquivo CSV fixo da pesquisa realizada com 35 alunos de diferentes cursos (Análise e Desenvolvimento de Sistemas, Ciência da Computação e Direito).

## 🎯 Características Principais

### Seções do Site

#### 🏠 **Hero Section - Início**
- Apresentação do projeto de pesquisa
- 3 cards informativos (35 respondentes, 6 modalidades de transporte, 3 variáveis coletadas)
- Call-to-action para explorar o dashboard

#### 📊 **Metodologia**
- Detalhes da população e amostra
- Método de coleta (Google Formulários)
- Descrição das 3 variáveis coletadas:
  - **Meio de Transporte** (qualitativa nominal)
  - **Tempo de Deslocamento** (quantitativa em intervalos)
  - **Custo Transporte** (quantitativa contínua em R$)

#### 📈 **Dados e Insights**
- Estatísticas resumidas: 35 respondentes, 6 meios, ~45 min tempo médio, 4/5 satisfação
- Distribuição dos respondentes por curso

#### 📊 **Dashboard Interativo**
- **Filtro por Meio de Transporte**: Selecione um modal para análise específica
- **KPI Cards**: Total respondentes, meio mais popular, tempo e satisfação médios
- **4 Gráficos Interativos**:
  - Distribuição de meios de transporte (pizza)
  - Nível de satisfação (pizza)
  - Tempo de deslocamento (barras)
  - Distribuição de custos (barras)
- **Tabela Analítica**: Custo diário calculado, tempo médio e satisfação por modal

#### 🔗 **Footer**
- Navegação rápida entre seções
- Informações do projeto
- Links de crédito

## 🎨 Design e UX

- **Navbar Fixa**: Navegação smooth scroll entre seções
- **Design Nebula Analytics**: Paleta de cores moderna (#a3a6ff, #ac8aff, #9bffce)
- **Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **Animações**: Transições suaves e hover states
- **Modo Escuro**: Interface dark-mode por padrão

## 🛠️ Tecnologias

- **HTML5**: Estrutura semântica
- **Tailwind CSS**: Estilização responsiva e componentes
- **JavaScript Vanilla**: Lógica, parsing CSV e interatividade
- **Plotly.js**: Gráficos interativos profissionais
- **Material Symbols**: Ícones vetoriais

## 📂 Dados Utilizados

O sistema utiliza o arquivo CSV existente:
```
Pesquisa_ Meios de Transporte (respostas) - Respostas ao formulário 1.csv
```

**Estrutura esperada do CSV:**
- Carimbo de data/hora
- Nome do respondente
- Curso
- Principal meio de transporte
- Frequência de uso
- Tempo de deslocamento (ida)
- Necessidade de múltiplos meios
- Gasto mensal estimado
- Benefício tarifário
- Avaliação de facilidade de acesso
- Principais problemas
- Sugestões de infraestrutura

## 🚀 Como Usar

### 1. Abrir o Site

Simplesmente abra o arquivo `index.html` em um navegador web moderno:

```bash
# Usando Python (recomendado para local development)
python3 -m http.server 8000

# Depois acesse: http://localhost:8000
```

Ou clique duplo no arquivo `index.html` para abrir diretamente.

### 2. Explorar as Seções

1. **Clique em "Início"** para ver a apresentação da pesquisa
2. **Clique em "Metodologia"** para entender como a pesquisa foi realizada
3. **Clique em "Dados"** para ver insights resumidos
4. **Clique em "Dashboard"** para análise detalhada

### 3. Usar o Dashboard

- **Visualizar dados**: Todos os dados já estão carregados automaticamente
- **Filtrar por transporte**: Selecione um meio no dropdown para análise específica
- **Limpar filtro**: Clique em "Limpar Filtros" para voltar à visão geral
- **Interagir com gráficos**: Hover para ver detalhes, clique para interagir

## 📊 Análises Disponíveis

### KPIs (Key Performance Indicators)
- Total de respondentes
- Meio de transporte mais utilizado
- Tempo médio de deslocamento
- Nível de satisfação média

### Gráficos
- **Distribuição de Meios**: Proporção de cada modal utilizado
- **Satisfação**: Níveis de facilidade de acesso ao campus
- **Tempo**: Distribuição dos tempos de deslocamento
- **Custos**: Faixas de gastos mensais

### Tabela Detalhada
Por cada meio de transporte:
- Quantidade de usuários
- Custo diário médio (calculado a partir de custo mensal ÷ 20 dias úteis)
- Tempo médio de deslocamento
- Nível de satisfação predominante

## 🔧 Funcionalidades Técnicas

### Parsing de CSV
- Handler robusto para CSV com campos quoted
- Suporte a CRLF (quebras de linha do Windows)
- Extração automática de colunas por matching de texto

### Cálculos Automáticos
- **Custo Diário**: Extrai faixa de valores → calcula média → divide por 20 dias
- **Tempo Médio**: Converte descrições textuais em minutos → calcula média
- **Satisfação**: Agrupa por modal e identifica nível predominante

### Filtros Dinâmicos
- Filtra dados em tempo real
- Atualiza todos os gráficos e KPIs simultaneamente
- Exclui automaticamente "Bicicleta" dos dados (conforme análise)

## 📱 Funcionalidades Responsivas

- **Desktop**: Layout completo com 2 colunas de gráficos
- **Tablet**: Layout adaptado com 1 coluna
- **Mobile**: Interface otimizada com menu colapsável

## 🎓 Informações da Pesquisa

**Instituição**: CIESA  
**Data**: Março de 2026  
**Amostra**: 35 alunos  
**Método de Amostragem**: Não-probabilística por conveniência  
**Instrumento**: Google Formulários  
**Respondentes por Curso**:
- Análise e Desenvolvimento de Sistemas (~40%)
- Ciência da Computação (~40%)
- Direito (~15% restante)  

## ⚙️ Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Conexão com internet para carregar bibliotecas (Tailwind CSS, Plotly.js, Material Symbols)
- JavaScript habilitado

## 📊 Exemplo de Análise

Ao abrir o site e ir para o Dashboard, você verá:

1. **4 KPI Cards** mostrando estatísticas principais
2. **4 Gráficos interativos** com visualizações dos dados
3. **Tabela detalhada** com análise por meio de transporte
4. **Filtro** para explorar um tipo de transporte específico

Exemplo: Filtrar "Ônibus" mostrará:
- Quantos alunos usam ônibus (ex: 18)
- Custo diário médio (ex: R$ 5,50/dia)
- Tempo médio de deslocamento (ex: ~45 min)
- Nível de satisfação predominante (ex: Bom)

## 🎨 Customização

O arquivo `index.html` contém:

- **Seção `<head>`**: Meta tags, imports de bibliotecas, Tailwind config
- **Seção `<body>`**: Toda a estrutura HTML com 5 seções principais
- **Seção `<script>`**: Toda a lógica JavaScript para parsing, cálculos e interatividade

Para customizar cores, edite a configuração Tailwind no `<head>` (cores prima, secondary, tertiary, etc).

## 📝 Estrutura de Dados

### globalData
Array de objetos contendo todos os registros do CSV parseado.

### filteredData
Array que reflete os dados atuais (após filtros aplicados).

### Funções Principais
- `parseCSV()`: Parse robusto do arquivo CSV
- `updateDashboard()`: Atualiza todos os componentes
- `updateCharts()`: Regenera os 4 gráficos
- `updateKPIs()`: Calcula métricas principais
- `updateStatsTable()`: Popula tabela com análises por modal

## 🐛 Troubleshooting

### "Nenhum dado está sendo exibido"
- Verifique se o navegador permite JavaScript
- Abra o console (F12) e procure por mensagens de erro
- Certifique-se de usar um navegador moderno

### "Gráficos aparecem em branco"
- Recarregue a página
- Verifique a conexão com internet (Plotly.js precisa ser carregado)

### "Filtro não está funcionando"
- Certifique-se de estar no Dashboard (seção inferior)
- Recarregue a página
- Tente limpar filtros e selecionar novamente

## 🚀 Melhorias Futuras Possíveis

- Exportação de dados em PDF
- Novos gráficos (tempo vs custo, análise por frequência)
- Comparações entre cursos
- Análise de problemas mais comuns
- Print/save de gráficos individuais

## 📧 Informações

**Dashboard**: Nebula Analytics Design System  
**Versão**: 2.0 (Now with Presentation)  
**Última atualização**: Março 2026  
**Compatibilidade**: Modern browsers (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)

---

**Desenvolvido com foco em apresentação profissional e análise de dados acessível.**
