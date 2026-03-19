# 📊 Dashboard de Meios de Transporte - Ciesa

Um dashboard web **interativo e dinâmico** para visualizar dados coletados sobre os meios de transporte utilizados pelos alunos do Ciesa.

## 🚀 Como Usar

### 1. **Exportar Dados do Google Formulários**

#### Passo a passo:

1. Abra o seu Google Formulário
2. Clique em **"Respostas"** no topo da página
3. Clique no ícone de **planilha** (Google Sheets) para criar uma nova planilha
4. Na planilha criada, selecione todos os dados (Ctrl+A)
5. Copie (Ctrl+C)
6. Cole em um arquivo de texto e salve como **`.csv`**

**OU**, exporte diretamente:

1. No Google Forms, vá para **Respostas**
2. Clique no ícone ⋮ (três pontos)
3. Selecione **"Descarregar respostas (.csv)"**

### 2. **Preparar o Arquivo CSV**

O arquivo CSV deve ter uma coluna chamada **"Meios de transporte"** (ou similar).

**Exemplo de formato esperado:**

```csv
Timestamp,Meios de transporte,Observações
2024-01-15 10:23:00,Ônibus,Transporte coletivo
2024-01-15 10:25:00,Carro próprio,Veículo particular
2024-01-15 10:27:00,Ônibus,Transporte coletivo
2024-01-15 10:29:00,Bicicleta,Transporte sustentável
2024-01-15 10:31:00,A pé,Mobilidade local
```

### 3. **Usar o Dashboard**

1. Abra o arquivo **`index.html`** no navegador
2. Clique em **"Carregar Dados"** ou **"Baixar Exemplo CSV"**
3. Selecione o seu arquivo CSV
4. Clique em **"Carregar Dados"** novamente
5. **Pronto!** O dashboard mostrará:
   - ✅ Estatísticas gerais
   - 📊 Gráfico de Pizza (distribuição percentual)
   - 📊 Gráfico de Barras (frequência)
   - 📊 Ranking (classificação ordenada)
   - 📋 Tabela detalhada com todos os dados

## 📈 Funcionalidades

- **Estatísticas Resumidas**: Total de respostas, tipos de transportes, transporte mais comum
- **Gráfico de Pizza**: Visualização percentual da distribuição
- **Gráfico de Barras**: Frequência absoluta por tipo de transporte
- **Ranking Interativo**: Classificação ordenada dos meios de transporte
- **Tabela Detalhada**: Dados específicos com contagem e percentuais
- **Responsivo**: Funciona em desktop e mobile
- **Interativo**: Passe o mouse para ver detalhes, clique nos gráficos para interagir

## 🎨 Tecnologias Utilizadas

- **HTML5**: Estrutura da página
- **CSS3**: Estilização moderna com gradientes
- **JavaScript (Vanilla)**: Lógica e processamento de dados
- **Plotly.js**: Bibliotecas para gráficos interativos

## 📝 Exemplo de Dados

```csv
Timestamp,Meios de transporte
2024-01-15 10:00,Ônibus
2024-01-15 10:05,Carro próprio
2024-01-15 10:10,Ônibus
2024-01-15 10:15,Bicicleta
2024-01-15 10:20,A pé
2024-01-15 10:25,Ônibus
2024-01-15 10:30,Moto
2024-01-15 10:35,Carro próprio
2024-01-15 10:40,Ônibus
2024-01-15 10:45,A pé
```

## ⚙️ Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Conexão com internet (para carregar a biblioteca Plotly.js)
- Arquivo CSV com a coluna "Meios de transporte"

## 🐛 Solução de Problemas

### "Coluna 'transporte' não encontrada"

- Verifique se o seu CSV tem uma coluna com nome similar a "Meios de transporte", "Transporte" ou "Meio"
- Certifique-se de que o arquivo foi exportado corretamente do Google Formulários

### "Nenhum dado de transporte encontrado"

- Verifique se o CSV não está vazio
- Confirme que a coluna de transporte tem dados preenchidos

### Gráficos em branco

- Recarregue a página
- Verifique se sua conexão com a internet está funcionando (para carregar Plotly.js)

## 📌 Personalização

Você pode editar o arquivo `index.html` para:

- Alterar as cores dos gráficos (linha ~150 no CSS)
- Mudar o título e descrição (linhas ~65-67)
- Adicionar novos gráficos ou filtros

## 📧 Suporte

Se tiver dúvidas, verifique o arquivo CSV e certifique-se de que:

1. ✅ A coluna de transporte existe
2. ✅ Os dados estão preenchidos
3. ✅ O arquivo está em formato `.csv` (não `.xlsx`)

---

**Versão**: 1.0  
**Última atualização**: Março 2026
