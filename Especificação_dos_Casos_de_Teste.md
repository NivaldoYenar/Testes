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
<br/>
<br/>
<br/>
---

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
<br/>
<br/>
<br/>
---


| **Identificador**         | CT-03 - Login com Dados Inválidos                  |
|---------------------------|----------------------------------------------------|
| **Descrição**             | Testar o comportamento do sistema ao realizar login com dados incorretos. |
| **Entradas**              | - E-mail: "usuario@exemplo.com"                    |
|                           | - Senha: "senhaerrada"                             |
| **Resultados Esperados**  | - O sistema deve exibir a mensagem "E-mail ou senha incorretos". |
| **Critérios para Aprovação/Rejeição** | - **Aprovação:**                        |
|                           |     - Mensagem de erro clara e sem acesso ao sistema. |
|                           | - **Rejeição:**                                    |
|                           |     - Sistema permite acesso indevido.             |
|                           |     - Mensagens de erro genéricas ou confusas.     |
| **Recursos para o Caso de Teste** | - **Ambiente de Teste:** Banco de dados com usuários cadastrados. |
|                           | - **Ferramentas:** Selenium para automação de testes de interface. |
| **Restrições de Uso**      | - O sistema deve bloquear múltiplas tentativas consecutivas de login falhas. |
| **Dependências**          | - Este caso de teste é independente de outros.     |
| **Observações Adicionais** | - Realizar testes com diferentes combinações de e-mails e senhas inválidas para maior cobertura. |
|                           | - Documentar quaisquer mensagens de erro fora do padrão esperado. |
<br/>
<br/>
<br/>
---

| **Identificador**         | CT-04 - Gerar Gráfico de Despesas Mensais          |
|---------------------------|----------------------------------------------------|
| **Descrição**             | Verificar se o gráfico de despesas mensais é gerado corretamente com base nos dados disponíveis. |
| **Entradas**              | - Transações: [R$200,00 - Alimentação, R$100,00 - Transporte]. |
| **Resultados Esperados**  | - O gráfico deve exibir os valores categorizados corretamente com barras ou fatias proporcionais. |
| **Critérios para Aprovação/Rejeição** | - **Aprovação:**                        |
|                           |     - Gráfico reflete as transações com categorização exata. |
|                           | - **Rejeição:**                                    |
|                           |     - Valores incorretos ou gráficos desproporcionais. |
| **Recursos para o Caso de Teste** | - **Ambiente de Teste:** Banco de dados com transações cadastradas. |
|                           | - **Ferramentas:** Selenium para automação de interface e análise visual. |
| **Restrições de Uso**      | - Gráficos devem ser gerados apenas com transações válidas e categorizadas. |
| **Dependências**          | - Este caso de teste depende do caso de teste "Registrar Nova Despesa Financeira". |
| **Observações Adicionais** | - Testar com diferentes combinações de valores e categorias para validar a geração correta. |
|                           | - Verificar a responsividade e a exibição em dispositivos móveis. |
<br/>
<br/>
<br/>
---

| **Identificador**         | CT-05 - Recuperação de Senha                       |
|---------------------------|----------------------------------------------------|
| **Descrição**             | Verificar se o sistema permite a recuperação de senha por e-mail. |
| **Entradas**              | - E-mail: "usuario@exemplo.com"                    |
| **Resultados Esperados**  | - O sistema envia um link de recuperação para o e-mail informado. |
| **Critérios para Aprovação/Rejeição** | - **Aprovação:**                        |
|                           |     - E-mail de recuperação enviado corretamente.  |
|                           |     - Link enviado funciona e permite redefinição de senha. |
|                           | - **Rejeição:**                                    |
|                           |     - Link não é enviado ou não funciona.          |
|                           |     - Mensagem de erro inadequada para e-mails inválidos. |
| **Recursos para o Caso de Teste** | - **Ambiente de Teste:** Banco de dados com usuários cadastrados. |
|                           | - **Ferramentas:** Postman para verificar envio de e-mails; Selenium para validação da interface. |
| **Restrições de Uso**      | - O sistema deve validar o formato do e-mail antes de tentar envio. |
|                           | - Links de recuperação devem expirar após um tempo configurado. |
| **Dependências**          | - Este caso de teste é independente de outros.     |
| **Observações Adicionais** | - Verificar o comportamento do sistema com e-mails inexistentes ou não cadastrados. |
|                           | - Documentar problemas de latência no envio de e-mails. |
<br/>
<br/>
<br/>
---
