| **Identificador**         | CT-01 - Registrar Nova Despesa Financeira          |
|---------------------------|----------------------------------------------------|
| **Descrição**             | Verificar se o sistema salva corretamente uma despesa com os dados fornecidos. |
| **Entradas**              | - Categoria: "Alimentação"                         |
|                           | - Valor: R$50,00                                   |
|                           | - Data: "2024-11-17"                               |
| **Resultados Esperados**  | - A despesa deve ser registrada na lista de transações com os detalhes fornecidos. |
|                           | - O valor deve ser contabilizado corretamente no total de despesas para a categoria correspondente. |
| **Critérios para Aprovação/Rejeição** | - **Aprovação:**                        |
|                           |     - A despesa é salva com todos os detalhes fornecidos. |
|                           |     - A transação aparece corretamente no gráfico de despesas, atualizando os valores totais. |
|                           | - **Rejeição:**                                    |
|                           |     - O sistema não salva os dados fornecidos.     |
|                           |     - Informações inconsistentes no gráfico ou na lista de transações. |
| **Recursos para o Caso de Teste** | - **Ambiente de Teste:** Banco de dados configurado com categorias predefinidas. |
|                           | - **Ferramentas:** Selenium para automação de testes de interface; Postman para verificar API de registro de despesas. |
| **Restrições de Uso**      | - Todos os campos obrigatórios (categoria, valor e data) devem ser preenchidos. |
|                           | - O valor da despesa deve ser maior que R$0,00.    |
| **Dependências**          | - Este caso de teste depende do caso de teste "Cadastrar Categoria de Despesa", garantindo que a categoria "Alimentação" esteja disponível no sistema. |
| **Observações Adicionais** | - Testar a funcionalidade com diferentes categorias, valores e datas para verificar a robustez do sistema. |
|                           | - Documentar quaisquer erros ou comportamentos inesperados, como sobreposição de dados ou falhas na atualização do gráfico. |
|                           | - Verificar a compatibilidade com diferentes formatos de data. |




| **Identificador**         | CT-02 - Criar Meta Financeira                      |
|---------------------------|----------------------------------------------------|
| **Descrição**             | Verificar se o sistema permite a criação de uma meta financeira. |
| **Entradas**              | - Meta: "Economizar para viagem"                   |
|                           | - Valor: R$5.000,00                                |
|                           | - Data Limite: "2024-12-31"                        |
| **Resultados Esperados**  | - A meta deve ser criada e exibida na lista de metas. |
|                           | - Os dados devem estar corretos e associados ao progresso financeiro. |
| **Critérios para Aprovação/Rejeição** | - **Aprovação:**                        |
|                           |     - A meta é registrada corretamente com os dados fornecidos. |
|                           |     - A meta aparece nas seções de progresso e os valores são calculados adequadamente. |
|                           | - **Rejeição:**                                    |
|                           |     - A meta não é registrada no sistema.          |
|                           |     - Aparecem erros ou inconsistências nos cálculos de progresso. |
| **Recursos para o Caso de Teste** | - **Ambiente de Teste:** Banco de dados configurado para armazenar metas financeiras. |
|                           | - **Ferramentas:** Selenium para automação de testes de interface; Postman para verificar API de criação de metas. |
| **Restrições de Uso**      | - A meta financeira deve ter um valor positivo maior que zero. |
|                           | - A data limite não pode ser anterior à data atual. |
| **Dependências**          | - Este caso de teste depende do caso de teste "Registrar Nova Despesa Financeira", garantindo que o progresso financeiro seja calculado corretamente. |
| **Observações Adicionais** | - Testar diferentes combinações de valores, metas e datas para garantir a consistência do sistema. |
|                           | - Documentar quaisquer falhas ou erros relacionados à criação de metas ou cálculos de progresso. |
|                           | - Verificar se o progresso é atualizado dinamicamente ao registrar despesas relacionadas à meta. |
