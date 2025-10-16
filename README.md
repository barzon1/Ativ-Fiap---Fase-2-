Sistema Agrotech para Minimização de Perdas por Estresse Hídrico no Feijão

FIAP - Faculdade de Informática e Administração Paulista

Nome do Projeto
Sistema Agrotech para Minimização de Perdas por Estresse Hídrico no Feijão

Nome do Grupo
Grupo 70

👨‍🎓 Integrantes:
Lucas Rodrigues Barzon

👩‍🏫 Professores:
Tutor(a): Sabrina Otoni

Coordenador(a): Anddré Godoi

📜 Descrição
Este projeto visa implementar uma solução de Agrotech robusta, funcionando como um sistema de apoio à decisão crucial para o setor de produção de feijão. O foco principal é a mitigação do alto desperdício e da perda de produtividade causados por períodos de seca e pelo consequente estresse hídrico na cultura.

O problema central a ser resolvido reside na alta sensibilidade do feijão ao déficit de água, uma condição que pode levar a perdas de até 35% da safra, especialmente durante seus estágios de desenvolvimento mais críticos (fenológicos). O sistema atua como uma ferramenta de gestão de riscos ao:

Monitorar o nível de estresse hídrico em diferentes talhões.

Quantificar o prejuízo financeiro estimado com base nesse estresse e no estágio da cultura.

Alertar o produtor para a necessidade de ações preventivas ou corretivas imediatas.

Linha Lógica e Fluxo de Dados:
O funcionamento do sistema segue uma linha lógica clara e rastreável:

Entrada de Dados: Recebimento de informações essenciais da lavoura (área, produtividade esperada e o nível de estresse hídrico detectado para cada talhão).

Processamento: Aplicação de regras de perda previamente definidas, que são lidas e carregadas dinamicamente a partir de um arquivo de configuração JSON (config_perdas.json).

Saída e Persistência: O histórico de cada monitoramento, incluindo as perdas estimadas e alertas, é salvo em um banco de dados Oracle na tabela HISTORICO_PLANTIO, garantindo total rastreabilidade do manejo. Adicionalmente, logs de execução são gravados em um arquivo de texto (registro_monitoramento.txt).


Tecnologias e Estruturas Utilizadas:
O código é estruturado com o uso de:

Subalgoritmos: Implementação através de Funções (e.g., calcular_perda_estimada, conectar_oracle) e Procedimentos (e.g., gerar_relatorio, registrar_log_e_salvar).

Estruturas de Dados: Uso estratégico de Listas (TALHOES_MONITORADOS), Dicionários (para dados dos talhões e regras do JSON) e Tuplas (para representar os Estágios Críticos Fenológicos, garantindo imutabilidade).

Manipulação de Arquivos: Leitura de dados de configuração em formato JSON e gravação de logs em arquivo de Texto.

Conexão com Banco de Dados: Utilização do Oracle para armazenamento do histórico.


📁 Estrutura de Pastas
Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

.github: Nesta pasta ficarão os arquivos de configuração específicos do GitHub que ajudam a gerenciar e automatizar processos no repositório.

assets: aqui estão os arquivos relacionados a elementos não-estruturados deste repositório, como imagens.

config: Posicione aqui arquivos de configuração que são usados para definir parâmetros e ajustes do projeto. O arquivo config_perdas.json deve residir aqui.

document: aqui estão todos os documentos do projeto que as atividades poderão pedir. Na subpasta "other", adicione documentos complementares e menos importantes.

scripts: Posicione aqui scripts auxiliares para tarefas específicas do seu projeto. Exemplo: deploy, migrações de banco de dados, backups.

src: Todo o código fonte criado para o desenvolvimento do projeto ao longo das 7 fases. O código principal do sistema Agrotech deve residir aqui.

README.md: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).


🔧 Como executar o código
Pré-Requisitos:

IDE/Ambiente: Python 3.12.3, Visual Studio Code

Banco de Dados: Acesso a uma instância do Oracle Database e credenciais configuradas.

Bibliotecas: Necessário instalar a biblioteca de conexão com Oracle (e.g., cx_Oracle ou similar) e qualquer biblioteca necessária para manipulação de JSON e logs.


Passo a Passo (Exemplo):

Clonar o Repositório:

Bash

git clone https://www.youtube.com/watch?v=6YQIWRyPxnk
cd sistema_monitoramento_feijao.py

Instalar Dependências:

Bash

pip install -r requirements.txt
# ou instale manualmente: pip install cx_Oracle
Configuração do Banco de Dados:

Garanta que a tabela HISTORICO_PLANTIO esteja criada em seu schema Oracle.

Verifique se as credenciais de acesso ao Oracle estão corretamente configuradas (provavelmente em um arquivo de configuração dentro da pasta config ou diretamente no código em src).

Executar o Script Principal:

Execute o arquivo principal que inicia o fluxo de monitoramento e cálculo.

Bash

python src/main_agrotech.py

Verificação:

Após a execução, verifique se o arquivo de log (registro_monitoramento.txt) foi criado/atualizado.

Verifique a tabela HISTORICO_PLANTIO no Oracle para confirmar o registro dos dados.

🗃 Histórico de Lançamentos
0.5.0 - 15/10/2025 - Entrega final do projeto.

0.4.0 - 10/10/2025 - Implementação da conexão e registro no Banco de Dados Oracle.

0.3.0 - 10/10/2025 - Finalização da lógica de cálculo de perda e alerta com base no JSON de regras.

0.2.0 - 10/10/2025 - Estruturação de dados (Listas, Dicionários, Tuplas) e manipulação do arquivo config_perdas.json.

0.1.0 - 07/10/2025 - Criação da estrutura base do projeto e definição dos subalgoritmos.

📋 Licença
MODELO GIT FIAP por Fiap está licenciado sobre Attribution 4.0 International.
