# Trabalhando-com-Machine-Learning-na-Pr-tica-no-Azure-ML
Guia de Implantação do Azure Machine Learning com Automação

Bem-vindo ao Guia de Implantação do Azure Machine Learning com Automação! Este guia o ajudará a criar e implantar um trabalho de aprendizado de máquina automatizado para previsão de aluguel de bicicletas usando o Azure Machine Learning studio.

Passo 1: Criando o Trabalho de Aprendizado de Máquina Automatizado
No Azure Machine Learning studio, acesse a página "Automated ML" em Authoring.
Crie um novo trabalho de Aprendizado de Máquina Automatizado com as seguintes configurações:
Configurações Básicas:
Nome do trabalho: mslearn-bike-automl
Nome do experimento: mslearn-bike-rental
Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
Tags: Nenhum
Tipo de Tarefa e Dados:
Selecione o tipo de tarefa: Regressão
Selecione o conjunto de dados: Crie um novo conjunto de dados chamado bike-rentals com as configurações fornecidas.
Configurações da Tarefa:
Tipo de tarefa: Regressão
Conjunto de dados: bike-rentals
Coluna de destino: Aluguéis (inteiro)
Configurações adicionais:
Métrica principal: Erro quadrático médio normalizado
Explicar o melhor modelo: Não selecionado
Usar todos os modelos suportados: Não selecionado
Modelos permitidos: RandomForest e LightGBM
Limites:
Máximo de tentativas: 3
Máximo de tentativas concorrentes: 3
Máximo de nós: 3
Limiar da métrica: 0.085
Tempo limite: 15
Tempo limite da iteração: 15
Habilitar término antecipado: Selecionado
Validação e Teste:
Tipo de validação: Divisão de treinamento-validação
Porcentagem de dados de validação: 10
Conjunto de dados de teste: Nenhum
Computação:
Selecione o tipo de computação: Serverless
Tipo de máquina virtual: CPU
Nível da máquina virtual: Dedicado
Tamanho da máquina virtual: Standard_DS3_V2
Número de instâncias: 1
Envie o trabalho de treinamento. Ele começará automaticamente.
Passo 2: Revisando o Melhor Modelo
Aguarde o término do trabalho. Isso pode levar algum tempo.
Depois de concluído, revise o resumo do melhor modelo na guia Visão Geral.
Selecione o texto embaixo de "Nome do algoritmo" para ver os detalhes.
Vá para a guia Métricas e revise os gráficos de desempenho.
Passo 3: Implantação e Teste do Modelo
Na guia Modelo do melhor modelo, selecione "Implantar" e escolha a opção "Serviço da Web".
Configure as configurações de implantação:
Nome: predict-rentals
Descrição: Prever aluguéis de bicicletas
Tipo de computação: Instância do Contêiner do Azure
Habilitar autenticação: Selecionado
Aguarde o início e a conclusão da implantação.
Teste o serviço implantado navegando até Endpoints > ponto final em tempo real predict-rentals > guia Testar.
Substitua o JSON do modelo com os dados de entrada fornecidos.
Parabéns! Você criou, implantou e testou com sucesso um modelo de aprendizado de máquina automatizado para previsão de aluguel de bicicletas usando o Azure Machine Learning studio. Se tiver alguma dúvida ou problema, não hesite em nos contatar para obter assistência.
