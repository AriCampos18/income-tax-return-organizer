##### English Version Bellow


# Organizador de Declaração de Imposto de Renda

## Sobre o Projeto

O **Organizador de Declaração de Imposto de Renda** é uma ferramenta desenvolvida inteiramente no Microsoft Excel com o objetivo de facilitar a organização e a centralização de informações necessárias para a preparação da declaração de Imposto de Renda de Pessoa Física (IRPF).

O projeto funciona como um agregador de dados, permitindo registrar informações pessoais, organizar informes de rendimentos bancários e acompanhar entradas financeiras. A ferramenta utiliza recursos nativos do Excel para proporcionar uma experiência de uso mais organizada, prática e intuitiva.

A solução conta com campos estruturados, listas de seleção, fórmulas automáticas, links rápidos, navegação entre seções e um gráfico de pizza complementar para visualizar a distribuição dos valores registrados por banco.

## Objetivos

- Centralizar informações relevantes para a preparação da declaração de Imposto de Renda.
- Facilitar o preenchimento e a consulta de dados pessoais e financeiros.
- Reduzir erros de preenchimento por meio de validações de dados.
- Automatizar cálculos e a consolidação de valores.
- Melhorar a visualização e a organização das informações por meio de recursos gráficos.
- Proporcionar uma interface amigável, com navegação simplificada e funcionalidades de apoio.

## Funcionalidades

### 1. Dados do Titular

A seção de dados do titular permite registrar informações pessoais necessárias para a organização dos dados da declaração.

Entre os campos disponíveis estão:

- Nome completo;
- CPF;
- Data de nascimento;
- Título de eleitor;
- Cônjuge;
- Endereço;
- Endereço abreviado;
- CEP;
- Telefone;
- Celular;
- E-mail;
- Indicadores relacionados a alterações na declaração anterior, dependência do cônjuge e residência no exterior.

Os campos de respostas do tipo sim ou não utilizam listas de seleção para padronizar o preenchimento e evitar variações desnecessárias nas respostas.

O campo de e-mail também possui um link rápido que permite iniciar uma mensagem por meio do aplicativo de e-mail configurado no computador.

### 2. Informes de Rendimentos Bancários

Essa seção permite registrar informações dos bancos e os respectivos valores atuais, facilitando a organização dos informes de rendimentos bancários.

Para cada registro, a interface apresenta:

- **Banco:** instituição financeira selecionada;
- **Valor atual:** valor informado para a instituição;
- **Anexo:** referência ao arquivo correspondente, como um informe bancário em PDF.

A ferramenta também apresenta um campo de totalização que utiliza uma fórmula do Excel para somar os valores registrados nos campos financeiros.

A soma é calculada automaticamente, permitindo que o total seja atualizado quando os valores referenciados são alterados.

### 3. Gráfico de Distribuição por Banco

Como funcionalidade complementar, foi desenvolvido um gráfico de pizza para representar visualmente a distribuição dos valores registrados entre os bancos.

O gráfico permite identificar a participação relativa de cada instituição no conjunto de valores considerados, facilitando a interpretação das informações financeiras.

Para implementar essa funcionalidade, foi criada uma tabela auxiliar na própria aba `INFORMES`. Essa tabela utiliza fórmulas para referenciar os campos de banco e valor preenchidos na interface principal.

A tabela auxiliar funciona como fonte de dados do gráfico, evitando a necessidade de digitar novamente as mesmas informações.

Para manter a interface limpa, a formatação da tabela auxiliar utiliza cores de fundo e de fonte que a deixam visualmente discreta, fazendo com que ela sirva apenas como estrutura de apoio.

**Funcionamento técnico:**

- Os nomes dos bancos são referenciados a partir dos campos de seleção da interface.
- Os valores são vinculados aos respectivos campos de valor atual.
- O gráfico utiliza os dados dessa tabela auxiliar como origem.
- Quando os valores referenciados são modificados, o gráfico pode ser atualizado pelo Excel.

A configuração atual do gráfico utiliza três registros bancários. Para incluir mais bancos na visualização, é necessário ampliar a tabela auxiliar e ajustar a origem dos dados do gráfico para contemplar os novos registros.

### 4. Notas Bancárias e Entradas Financeiras

A seção de notas permite registrar entradas financeiras ao longo do tempo, auxiliando na organização dos dados relacionados às receitas.

Os campos disponíveis incluem:

- **Data:** data da entrada financeira;
- **Categoria:** classificação da entrada;
- **Valor:** valor correspondente à movimentação.

A categoria utiliza uma lista de seleção com opções predefinidas:

- Holerite;
- CNPJ;
- Freelance.

Essa validação padroniza as categorias e facilita a organização posterior das informações.

### 5. Tabela de Apoio de Bancos

O arquivo possui uma planilha auxiliar chamada `TABELA DE APOIO - BANCOS`, mantida oculta para não interferir na interface principal.

Essa planilha contém uma lista de instituições financeiras e seus respectivos códigos, utilizada como referência para listas suspensas e outros recursos de seleção do Excel.

Manter essa lista separada da interface principal ajuda a organizar os dados de referência e facilita a manutenção da ferramenta.

### 6. Navegação e Interface

A interface foi estruturada em seções numeradas, facilitando a identificação e a localização das funcionalidades.

O projeto também utiliza elementos visuais para diferenciar campos de preenchimento, informações calculadas e áreas de apoio.

A proposta é manter a experiência de uso simples e organizada, mesmo com diferentes tipos de informações concentrados em um único arquivo.

## Estrutura da Pasta de Trabalho

O arquivo está organizado nas seguintes planilhas:

| Planilha | Descrição |
|---|---|
| `TITULAR` | Cadastro das informações pessoais do titular. |
| `INFORMES` | Registro de bancos, valores atuais, referências de anexos, totalização e gráfico de distribuição. |
| `NOTAS` | Registro de entradas financeiras, datas, categorias e valores. |
| `TABELA DE APOIO - BANCOS` | Lista auxiliar de bancos e códigos, mantida oculta. |

## Recursos Técnicos do Excel

O projeto utiliza recursos nativos do Microsoft Excel para implementar suas funcionalidades.

- **Fórmulas:** cálculo automático do total dos valores bancários.
- **Referências entre células:** conexão entre os campos preenchidos e a tabela auxiliar do gráfico.
- **Validação de dados:** listas de seleção para padronizar respostas e categorias.
- **Hiperlinks:** acesso rápido ao envio de e-mails.
- **Gráficos:** visualização da distribuição dos valores por instituição financeira.
- **Planilha oculta:** armazenamento de dados de referência sem ocupar espaço na interface principal.
- **Formatação de células:** organização visual dos campos e identificação das áreas de preenchimento.

## Como Utilizar

1. Abra o arquivo `Income Tax Return Organizer.xlsx` no Microsoft Excel.
2. Na planilha `TITULAR`, preencha os dados pessoais com as informações desejadas.
3. Na planilha `INFORMES`, selecione os bancos disponíveis, informe os valores atuais e registre as referências dos documentos correspondentes.
4. Confira o total calculado automaticamente e consulte o gráfico para visualizar a distribuição dos valores.
5. Na planilha `NOTAS`, registre as entradas financeiras com suas respectivas datas, categorias e valores.
6. Atualize as informações sempre que necessário, verificando se as fórmulas e a origem dos dados do gráfico abrangem todos os registros utilizados.

## Dados de Demonstração

**Todos os dados presentes no arquivo são fictícios e foram utilizados exclusivamente para demonstrar as funcionalidades da ferramenta.** Nenhuma informação pessoal ou financeira real é necessária para utilizar o projeto como demonstração.

## Requisitos

- Microsoft Excel compatível com os recursos utilizados na pasta de trabalho.
- Conhecimentos básicos de preenchimento e navegação em planilhas.

## Observações Importantes

Este projeto é uma ferramenta de organização de informações e não substitui o programa oficial da Receita Federal, uma consultoria contábil ou a validação dos dados exigidos para a declaração de Imposto de Renda.

O arquivo não deve ser considerado um sistema de transmissão de declarações fiscais. Sua finalidade é auxiliar na organização dos dados e dos documentos necessários à preparação da declaração.

## Tecnologias e Recursos

- Microsoft Excel
- Fórmulas e referências entre células
- Validação de dados
- Hiperlinks
- Gráficos
- Planilhas auxiliares ocultas

## Autora

Projeto desenvolvido como uma solução prática de organização de dados no Microsoft Excel.

###### *Os dados apresentados são fictícios.
###### *Imagens de comprovação do funcionamento do sistema estão em main/images

###### English Version

# Income Tax Return Organizer

## About the Project

The **Income Tax Return Organizer** is a tool developed entirely in Microsoft Excel to help users organize and centralize information needed to prepare an Individual Income Tax Return (IRPF in Brazil).

The project works as a data aggregator, allowing users to record personal information, organize bank income statements, and track financial inflows. It uses native Excel features to provide a more organized, practical, and intuitive user experience.

The solution includes structured input fields, selection lists, automatic formulas, quick links, navigation between sections, and an additional pie chart for visualizing the distribution of recorded amounts by bank.

## Objectives

- Centralize information relevant to income tax return preparation.
- Simplify the entry and retrieval of personal and financial data.
- Reduce input errors through data validation.
- Automate calculations and value aggregation.
- Improve data visualization and organization through charts.
- Provide a user-friendly interface with simplified navigation and supporting features.

## Features

### 1. Taxpayer Information

The taxpayer information section allows users to record personal details needed to organize their tax return information.

Available fields include:

- Full name;
- Brazilian CPF taxpayer identification number;
- Date of birth;
- Voter registration number;
- Spouse;
- Address;
- Abbreviated address;
- Postal code;
- Telephone;
- Mobile phone;
- Email address;
- Indicators related to changes from the previous tax return, spouse dependency, and residence abroad.

Yes-or-no fields use selection lists to standardize input and prevent unnecessary variations in responses.

The email field also includes a quick link that opens a new message in the email application configured on the computer.

### 2. Bank Income Statements

This section allows users to record banks and their corresponding current amounts, helping organize bank income statements.

Each record includes:

- **Bank:** selected financial institution;
- **Current Amount:** amount entered for the institution;
- **Attachment:** reference to the corresponding file, such as a bank statement in PDF format.

The section also includes a total field that uses an Excel formula to add the values recorded in the financial fields.

The total is calculated automatically and can be updated when the referenced amounts change.

### 3. Bank Distribution Chart

As an additional feature, a pie chart was created to visually represent the distribution of recorded amounts among banks.

The chart helps users identify each institution's relative share of the amounts being considered, making the financial information easier to interpret.

To implement this feature, an auxiliary table was created within the `INFORMES` worksheet. This table uses formulas to reference the bank and amount fields entered in the main interface.

The auxiliary table serves as the chart's data source, eliminating the need to manually enter the same information again.

To keep the interface clean, the auxiliary table uses matching background and font colors, making it visually discreet and allowing it to serve as a supporting data structure.

**Technical implementation:**

- Bank names are referenced from the bank selection fields in the interface.
- Amounts are linked to their corresponding current amount fields.
- The chart uses the auxiliary table as its data source.
- When the referenced values change, Excel can update the chart accordingly.

The current chart configuration uses three bank records. To include additional banks in the visualization, the auxiliary table must be expanded and the chart's data source adjusted to cover the additional records.

### 4. Bank Notes and Financial Inflows

The notes section allows users to record financial inflows over time, helping organize revenue-related information.

Available fields include:

- **Date:** date of the financial inflow;
- **Category:** classification of the inflow;
- **Amount:** corresponding transaction value.

The category field uses a selection list with predefined options:

- Payslip;
- CNPJ (Brazilian corporate taxpayer identification number);
- Freelance.

This validation standardizes categories and makes it easier to organize the information later.

### 5. Bank Reference Table

The workbook includes an auxiliary worksheet named `TABELA DE APOIO - BANCOS`, which is kept hidden to avoid interfering with the main interface.

This worksheet contains a list of financial institutions and their respective codes, used as a reference for dropdown lists and other Excel selection features.

Keeping this list separate from the main interface helps organize reference data and makes the tool easier to maintain.

### 6. Navigation and Interface

The interface is organized into numbered sections, making features easier to identify and access.

Visual elements are also used to distinguish input fields, calculated information, and supporting areas.

The goal is to provide a simple and organized user experience, even when different types of information are consolidated into a single workbook.

## Workbook Structure

The workbook is organized into the following worksheets:

| Worksheet | Description |
|---|---|
| `TITULAR` | Stores the taxpayer's personal information. |
| `INFORMES` | Records banks, current amounts, attachment references, total calculations, and the distribution chart. |
| `NOTAS` | Records financial inflows, dates, categories, and amounts. |
| `TABELA DE APOIO - BANCOS` | Hidden reference list of banks and their codes. |

## Excel Features and Technical Implementation

The project uses native Microsoft Excel features to implement its functionality.

- **Formulas:** automatic calculation of total bank amounts.
- **Cell references:** connections between user-entered fields and the chart's auxiliary table.
- **Data validation:** selection lists to standardize responses and categories.
- **Hyperlinks:** quick access to email composition.
- **Charts:** visualization of the distribution of amounts by financial institution.
- **Hidden worksheet:** storage of reference data without occupying space in the main interface.
- **Cell formatting:** visual organization of fields and identification of input areas.

## How to Use

1. Open `Income Tax Return Organizer.xlsx` in Microsoft Excel.
2. In the `TITULAR` worksheet, enter the desired personal information.
3. In the `INFORMES` worksheet, select the available banks, enter their current amounts, and record the references to the corresponding documents.
4. Review the automatically calculated total and consult the chart to visualize the distribution of amounts.
5. In the `NOTAS` worksheet, record financial inflows along with their dates, categories, and amounts.
6. Update the information whenever necessary, checking that the formulas and chart data source cover all records being used.

## Sample Data

**All data included in the workbook is fictional and is used exclusively to demonstrate the tool's features.** No real personal or financial information is required to use the project as a demonstration.

## Requirements

- Microsoft Excel compatible with the features used in the workbook.
- Basic knowledge of spreadsheet navigation and data entry.

## Important Notes

This project is an information organization tool. It does not replace the official Brazilian Federal Revenue Service software, professional accounting advice, or the validation of information required for an income tax return.

The workbook is not a tax filing or submission system. Its purpose is to help organize data and supporting documents needed to prepare a tax return.

## Technologies and Features

- Microsoft Excel
- Formulas and cell references
- Data validation
- Hyperlinks
- Charts
- Hidden auxiliary worksheets

## Author

A practical data organization solution developed using Microsoft Excel.

###### *The data presented are fictitious.
###### *Images demonstrating the system's operation can be found in main/images.
