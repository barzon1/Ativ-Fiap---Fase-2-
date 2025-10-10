Sistema Agrotech para Minimização de Perdas por Estresse Hídrico no Feijão.

Do que se trata o projeto: 
    Este projeto implementa um sistema de apoio à decisão para o agronegócio, focado em mitigar o desperdício e a perda de produtividade na cultura do feijão (Setor de Produção) causados por períodos de seca e estresse hídrico.

O Problema a ser resolvido:
    O feijão sendo uma cultura altamente sensível ao estresse hídrico, sofre perdas de até 35% em estágios críticos. O sistema atua como uma Agrotech ao monitorar o nível de estresse e quantificar o prejuízo financeiro estimado, alertando o produtor para ações preventivas.

Linha Lógica:
    O sistema recebe dados de área e produtividade, aplica regras de perda lidas de um arquivo JSON e salva o histórico de monitoramento no banco de dados Oracle para rastreabilidade.

O que foi usado:
    Subalgoritmos - Uso de Funções (calcular_perda_estimada, conectar_oracle) e Procedimentos (gerar_relatorio, registrar_log_e_salvar)

    Estruturas de Dados - Uso de Listas (para TALHOES_MONITORADOS), Dicionários (dados de cada talhão e regras JSON) e Tuplas (Estágios Críticos Fenológicos).

    Manipulação de Arquivos - Leitura em JSON (config_perdas.json) e gravação do log em arquivo de Texto (registro_monitoramento.txt).

    Conexão com Banco de Dados - Historico de onitoramento na tabela HISTORICO_PLANTIO no banco de dados Oracle.