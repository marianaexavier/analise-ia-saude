# Seminário: IA na Saúde — Equidade e Vieses

## Tópico 1: Acesso e Infraestrutura (SUS vs. Saúde Suplementar)

Este repositório contém o Jupyter Notebook utilizado na preparação e apresentação da **Parte 1** do seminário sobre **Inteligência Artificial na Saúde**, com foco nas assimetrias de acesso, conectividade e infraestrutura tecnológica no sistema de saúde brasileiro.

### 📌 Contexto Acadêmico

* **Instituição:** Universidade Federal da Paraíba (UFPB)

* **Curso:** Bacharelado em Ciência de Dados e Inteligência Artificial

* **Disciplina:** Computadores e Sociedade

* **Docente:** Prof. Ed Porto

* **Integrantes do Grupo:**

  * Helena Couto dos Santos

  * Mariana Esthefany Xavier dos Santos

  * Vitória Maria da Silva

### 🎯 Pergunta-Guia do Seminário

> *"Quando um algoritmo de IA erra, ele erra igual para todo mundo, ou o erro pesa mais para quem já tem menos acesso?"*

### 🗺️ Mapeamento e Estrutura da Apresentação

O notebook está organizado seguindo estritamente a ordem dos slides e do roteiro de fala (duração estimada da etapa: 20 minutos):

| Bloco / Trecho | Tempo | Slides | Conteúdo no Notebook | 
 | ----- | ----- | ----- | ----- | 
| **0. Abertura do Grupo** | `0:00–1:00` | 1–2 | Guia de fala e contexto do grupo | 
| **1. Gancho & Enquadramento** | `1:00–2:00` | 3–6 | Tabela regional (Distribuição SUS × Saúde Suplementar) | 
| **2. Bloco 1: Parque Tecnológico** | `2:00–5:30` | 7–8 | Gráfico 1 (Equipamentos de imagem por 100 mil hab.) | 
| **3. Bloco 2: Conectividade** | `5:30–9:00` | 9 | Gráfico 2 (Acesso a dados e internet nos estabelecimentos) | 
| **4. Bloco 3: Uso Efetivo de IA** | `9:00–12:00` | 10–12 | Gráfico 3 (Adoção de IA e ritmos de implementação) | 
| **5. Bloco 4: A Dupla Desigualdade** | `12:00–15:00` | 13 | Gráfico 4 (Cruzamento setor público/privado e regiões) | 
| **6. Razões da Persistência** | `15:00–17:00` | 14 | Guia de fala e análise de gargalos | 
| **7. Síntese: Mismatch Estrutural** | `17:00–18:30` | 15 | Gráfico 5 (Descompasso estrutural) | 
| **8. Encerramento & Transição** | `18:30–20:00` | 16–17 | Guia de fala e passagem para a Pessoa 2 | 

### 📊 Fontes de Dados e Metodologia

Os dados e estimativas contidos no notebook foram extraídos das seguintes referências:

1. **TIC Saúde 2025** (*Cetic.br / NIC.br*): Pesquisa realizada com 3.270 gestores de estabelecimentos de saúde entre fevereiro e novembro de 2025. *(Base para os Gráficos 2 e 3)*.

2. **Atlas da Radiologia no Brasil 2025** (*Colégio Brasileiro de Radiologia - CBR*) e **CNES/DATASUS**. *(Base para a Tabela Regional e Gráfico 1)*.

3. **Síntese Própria e Estimativas Ilustrativas** com base em padrões regionais da ANS, CNES e DATASUS. *(Base para os Gráficos 4 e 5)*.

> ⚠️ **Nota metodológica:** Os Gráficos 1, 4 e 5 tratam-se de estimativas/sínteses analíticas de referência. Conforme indicado no roteiro, devem ser citados como *"estimativas com base no CNES/DATASUS/ANS"*.

### 🛠️ Tecnologias e Bibliotecas Utilizadas

O notebook utiliza a stack padrão de análise de dados em Python 3:

* [**Pandas**](https://pandas.pydata.org/?utm_source=gemini)**:** Manipulação e estruturação dos dados demográficos e de saúde por UF/Região.

* [**NumPy**](https://numpy.org/?utm_source=gemini)**:** Operações numéricas.

* [**Matplotlib**](https://matplotlib.org/?utm_source=gemini) **& [Seaborn](https://seaborn.pydata.org/?utm_source=gemini):** Visualização de dados e geração de gráficos com paleta de cores idêntica à dos slides (`#254370` para SUS e `#17947f` para setor Privado).

### 🚀 Como Executar o Notebook

1. **Clone o repositório:**

   ```
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   
   ```

2. **Crie um ambiente virtual (opcional, mas recomendado):**

   ```
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   # ou: venv\Scripts\activate # Windows
   
   ```

3. **Instale as dependências:**

   ```
   pip install pandas numpy matplotlib seaborn jupyter
   
   ```

4. **Inicie o Jupyter Notebook:**

   ```
   jupyter notebook
   
   ```

### 💡 Destaques do Código

* **Consulta rápida por UF:** O notebook possui a função `consulta_uf('Nome_da_UF')` para consultar rapidamente a distribuição entre SUS e planos de saúde durante o debate (ex: `consulta_uf('Paraíba')`).

* **Padronização visual:** Contém funções auxiliares (`fonte()`, `anotar_barras_v()`, `anotar_barras_h()`) configuradas para garantir que as figuras geradas sigam a identidade visual exata da apresentação.