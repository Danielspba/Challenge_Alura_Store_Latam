🛒 Alura Store Latam: Data Engineering & Retail Analytics | Challenge Data Science

📌 Sobre o Projeto
Este projeto integra o Challenge Data Science da Alura, com foco na Alura Store, uma rede de varejo com múltiplas filiais na América Latina. O objetivo principal deste repositório é construir um pipeline de ponta a ponta: desde a extração e consolidação de dados brutos e fragmentados, até a geração de insights estratégicos para as áreas de Vendas e Marketing Digital.

O grande diferencial desta análise é a aplicação de técnicas de engenharia de dados (ETL) para contornar problemas de sistemas legados (arquivos em formatos distintos como JSON e CSV) e a construção de KPIs financeiros que direcionam campanhas de aquisição e retenção.

🎯 Desafios de Negócio e Objetivos
Integração de Dados (ETL): Unificar bases de dados dispersas das filiais Latam em um único DataFrame mestre, lidando com diferentes extensões e estruturas.

Higienização Financeira: Tratar sujeiras tipográficas em variáveis monetárias (remoção de símbolos, ajustes de separadores decimais via Regex) e converter strings em formatos temporais utilizáveis.

Inteligência de Varejo (BI): Mapear a saúde do negócio através de indicadores como Faturamento por Filial, Ticket Médio, Sazonalidade e Curva ABC de produtos.

Estratégia Orientada a Dados: Traduzir os números em planos de ação focados em otimização de estoque e campanhas de conversão.

🛠️ Pipeline e Metodologia
Extração Automática (Extract): Script desenvolvido para ler os dados diretamente do formato Raw do GitHub, varrendo iterativamente arquivos .json e .csv e identificando a filial de origem de cada venda.

Transformação e Limpeza (Transform): * Padronização de colunas para snake_case.

Tratamento de strings financeiras corrompidas e conversão para float.

Conversão de datas pontuais para objetos datetime, permitindo análises de coorte mensal e diária.

Criação da métrica primária: faturamento_total = quantidade * preço.

Análise Exploratória (EDA): Geração de relatórios visuais utilizando a biblioteca seaborn para investigar a dispersão de preços, sazonalidade semanal e volume absoluto de vendas por região.

💡 Principais Insights e Decisões Estratégicas
A consolidação dos dados revelou gargalos operacionais e oportunidades de alavancagem de receita:

Curva ABC e Risco de Stockout: Uma fração muito pequena do portfólio de produtos (Top 5) sustenta a maior parte da receita. Ação: Otimização da cadeia de suprimentos para evitar a falta desses itens críticos e implementação de campanhas de cross-sell (venda cruzada) para dar tração aos produtos de cauda longa (Curvas B e C).

Sazonalidade e Mídia Paga: Foi identificado um padrão claro de picos de conversão em dias específicos da semana. Ação: O orçamento de marketing digital (Ads) e os disparos de campanhas promocionais devem ser concentrados nas janelas de maior propensão à compra, elevando o Retorno sobre Investimento (ROI).

Ticket Médio x Volume: Algumas filiais apresentam menor tráfego absoluto, mas compensam com um Ticket Médio superior. Ação: Investigar as práticas de upsell dessas unidades e replicar o treinamento para as filiais de alto volume e baixo ticket.

💻 Como executar o projeto
Clone o repositório para a sua máquina local:

Bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
Abra o arquivo .ipynb no Jupyter Notebook, Google Colab ou na sua IDE de preferência.

Instale as dependências necessárias (caso não esteja num ambiente na nuvem):

Bash
pip install pandas numpy matplotlib seaborn requests
Execute as células em ordem. O script está configurado para puxar a base de dados em tempo real do repositório original, garantindo a reprodutibilidade completa da análise.
