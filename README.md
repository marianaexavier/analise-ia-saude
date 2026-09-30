# IA na Saúde: Equidade e Vieses
## Acesso e infraestrutura de dados: SUS × Saúde Suplementar

Análise exploratória de dados públicos sobre a desigualdade de infraestrutura entre o SUS e a saúde suplementar no Brasil: equipamentos de imagem, conectividade, leitos de UTI e adoção de inteligência artificial.

## 📌 Pergunta de Pesquisa
> *Se a IA aprende com dado, e a infraestrutura que gera dado está concentrada de um lado só, ela aprende sobre o Brasil inteiro ou só sobre um quarto dele?*

---

## 📖 Contexto e Autoria
Este repositório e notebook correspondem à **Parte 1 (Acesso e Infraestrutura)** do seminário *Equidade e Vieses: o impacto da IA no SUS vs. Saúde Privada no Brasil*, apresentado na disciplina de **Computadores e Sociedade** (Bacharelado em Ciência de Dados e Inteligência Artificial, UFPB, prof. Ed Porto). As partes seguintes do seminário (vieses algorítmicos e responsabilidade profissional) não se encontram neste notebook.

* **Autoria:**
  * Helena Couto dos Santos
  * Mariana Esthefany Xavier dos Santos
  * Vitória Maria da Silva

---

## 🗂️ Sumário do Notebook

0. **Configuração:** Definição da paleta de cores, estilo global e funções auxiliares.
1. **Contexto: um sistema de saúde dual:** Análise populacional e utilizadores do SUS vs. planos de saúde por UF/região.
2. **Parque tecnológico de imagem:** Densidade de equipamentos de imagem e indicadores de exames.
3. **Conectividade:** Infraestrutura digital nas instituições de saúde.
4. **Uso efetivo de IA:** Nível de adoção e tipos de IA aplicados.
5. **Iniciativas de IA no SUS:** Casos práticos e iniciativas de UTI inteligente no setor público.
6. **Saúde suplementar: pesquisa Anahp:** Mapeamento do uso de IA no setor privado.
7. **A dupla desigualdade: setorial e regional:** Distribuição de leitos de UTI e assimetrias regionais.
8. **Por que a distância persiste:** Análise dos fatores estruturais e orçamentários.
9. **Síntese: descompasso estrutural de dados:** Índice de concentração no setor privado.
10. **Conclusões:** Reflexões finais sobre equidade e representatividade dos dados.
11. **Notas metodológicas e limitações:** Considerações sobre as fontes e estimativas.
12. **Referências:** Fontes bibliográficas e dados utilizados.

---

## 📊 Fontes e Natureza dos Dados

| Seção | Dado | Fonte | Natureza |
|---|---|---|---|
| 1 | População, usuários do SUS e de planos por UF (2024) | Atlas da Radiologia no Brasil 2025 (CBR), adaptado; ANS/IBGE | Dado publicado |
| 2 | Densidade de equipamentos de imagem por 100 mil hab. | Estimativas de referência CNES/DATASUS · Atlas 2025 (CBR) | **Estimativa de referência** |
| 2 | Mamógrafos no Acre; IDPP geral de exames de imagem (2023) | Atlas 2025 (CBR); ContilNet (28/09/2025) | Dado publicado |
| 3, 4 | Infraestrutura digital; adoção e tipos de IA | TIC Saúde 2025 (Cetic.br/NIC.br), 3.270 gestores, fev.–nov. 2025 | Pesquisa amostral |
| 5 | Iniciativa de UTI inteligente no SUS | g1 Rio (27/06/2026); Rede CNT Brasil (set. 2026) | Reportagem |
| 6 | Uso de recursos de IA em instituições de saúde | Anahp em parceria com Wolters Kluwer (2025) | Pesquisa (base seletiva) |
| 7 | Leitos de UTI por 10 mil hab. por região | Padrões de distribuição regional CNES/DATASUS | **Estimativa ilustrativa** |
| 9 | Índice de concentração no setor privado | ANS/IBGE; Atlas 2025 (CBR); AMIB (2026) | **Síntese própria** |

---

## 🚀 Requisitos e Como Executar

### 1. Pré-requisitos
Certifique-se de ter o **Python 3.9+** e o **Jupyter Notebook** ou **VS Code** instalados na sua máquina.

### 2. Instalação das Bibliotecas
Instale as bibliotecas necessárias executando o seguinte comando no terminal:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Execução
1. Clone este repositório ou transfira os ficheiros para a sua máquina local:
   ```bash
   git clone https://github.com/marianaxavier/analise-ia-sus.git
   cd analise-ia-sus
   ```
2. Inicie o ambiente do Jupyter:
   ```bash
   jupyter notebook
   ```
3. Abra o ficheiro do notebook (`.ipynb`) e execute as células sequencialmente.
4. **Nota:** Todos os dados estão embutidos no próprio notebook, pelo que não é necessária a descarga de ficheiros de dados externos.
5. Os gráficos gerados serão gravados automaticamente na pasta local `figuras/`.