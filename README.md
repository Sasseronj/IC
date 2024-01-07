# CURRICULUM LEARNING E OUTRAS ESTRATÉGIAS DE TREINAMENTO PARA REMOÇÃO DE RUÍDOS EM IMAGENS

A construção de um Denoising Autoencoder (DAE) robusto é crucial para modelos de aprendizado de máquina eficazes, removendo ruídos nos dados de entrada por meio de uma função de reconstrução. A escolha precisa de hiperparâmetros e camadas é essencial para garantir representações significativas dos dados. Além do treinamento convencional, o Curriculum Learning (CL) pode aprimorar o desempenho, permitindo à rede aprender gradualmente.

No estudo, uma rede neural com 8 camadas e 8 filtros de tamanho 3x3 foi selecionada. O CL envolveu funções de pacing e scoring para incorporar dados de forma gradual. Foram testadas diferentes combinações de pacing e scoring, usando métricas como RMSE e CHISC (dos Santos and Ponti, 2019) durante 300 épocas, com 2000 iterações por época e taxa de aprendizado de 0.001.

Os resultados mostraram que o CL teve impacto positivo no aprendizado, especialmente na redução do RMSE, com melhorias de 0.014155 e 0.011966 para as métricas RMSE e CHISC, respectivamente, em níveis de ruído de 10. Em cenários de ruído mais alto (30), a métrica CHISC superou o desempenho do RMSE.

Em suma, o CL provou ser eficaz na remoção de ruídos em DAEs, superando ou igualando o método tradicional. A sensibilidade aos hiperparâmetros foi evidente, com o CHISC funcionando melhor em ruídos mais altos e o RMSE em ruídos mais baixos. Além disso, o CL reduziu o tempo de treinamento ao incorporar gradualmente os dados.
