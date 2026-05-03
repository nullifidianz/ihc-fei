# Avaliação de IHC através de Inspeção Heurística

1. **Avaliação de IHC através de inspeção HEURÍSTICA \[1 solução completa por pessoa da equipe \- todas as telas do projeto\]**

> **_NOTE:_**: SOMENTE VIOLAÇÕES

Dez Heurísticas de Nielsen

**Descrição da avaliação**

Avaliação heurística, definida por Nielsen e Molich (1994), é um método de avaliação de usabilidade onde um avaliador procura problemas de usabilidade numa interface com o usuário através da análise e interpretação de um conjunto de princípios ou heurísticas. Este método de avaliação é baseado no julgamento do avaliador.

1\. Primeiramente, leia e analise as dez heurísticas (ver Tabela 1).

**Tabela 1 \- Conjunto de heurísticas de Nielsen (1994)**

| 1\. | Visibilidade do status do sistema: |
| :---- | :---- |
| O sistema deve sempre manter os usuários informados sobre o que está acontecendo através de feedback apropriado, em um tempo razoável. |  |
| **2\.** | **Compatibilidade entre sistema e mundo real:** |
| O sistema deve utilizar a linguagem do usuário, com palavras, frases e conceitos familiares para ele, ao invés de termos específicos de sistemas. Seguir convenções do mundo real, fazendo com que a informação apareça em uma ordem lógica e natural. |  |
| **3\.** | **Controle e liberdade para o usuário:** |
| Estão relacionados à situação em que os usuários frequentemente escolhem as funções do sistema por engano e então necessitam de "uma saída de emergência" claramente definida para sair do estado não desejado sem ter que percorrer um longo diálogo, ou seja, é necessário suporte a *undo* e *redo*. |  |
| **4\.** | **Consistência e padrões:** |
| Referem-se ao fato de que os usuários não deveriam ter acesso a diferentes situações, palavras ou ações representando a mesma coisa. A interface deve ter convenções não-ambíguas. |  |
| **5\.** | **Prevenção de erros:** |
| Os erros são as principais fontes de frustração, ineficiência e ineficácia durante a utilização do sistema. |  |
| **6\.** |  **Reconhecimento em lugar de lembrança:** |
| Tornar objetos, ações, opções visíveis e coerentes. O usuário não deve ter que lembrar informações de uma parte do diálogo para outra. Instruções para o uso do sistema devem estar visíveis ou facilmente acessíveis. |  |
| **7\.** | **Flexibilidade e eficiência de uso:** |
| A ineficiência nas tarefas pode reduzir a eficácia do usuário e causar-lhes frustração. O sistema deve ser adequado tanto para usuários inexperientes quanto para usuários experientes. |  |
| **8\.** | **Projeto minimalista e estético:** |
| Os diálogos não devem conter informações irrelevantes ou raramente necessárias. Cada unidade extra de informação em um diálogo compete com unidades relevantes e diminui sua visibilidade relativa. |  |
| **9\.** | **Auxiliar os usuários a reconhecer, diagnosticar e recuperar erros:** |
| Mensagens de erro devem ser expressas em linguagem natural (sem códigos), indicando precisamente o erro e sugerindo uma solução. |  |
| **10\.** | **Ajuda e documentação:** |
| Mesmo que seja melhor que o sistema possa ser usado sem documentação, pode ser necessário fornecer ajuda e documentação. Tais informações devem ser fáceis de encontrar, ser centradas na tarefa do usuário, listar passos concretos a serem seguidos e não ser muito grandes. A ajuda deve estar facilmente acessível e on-line. |  |

2\. A seguir, avalie o sistema procurando possíveis problemas de usabilidade.   
3\. Quando um problema qualquer for detectado, classifique-o em uma das dez heurísticas de Nielsen, anotando o problema na tabela correspondente e atribuindo o **grau de severidade** (0 até 4\) para este problema (dado pela tabela 2\) e recomece novamente até não encontrar mais problemas de usabilidade.

**Tabela 2 \- Grau de severidade dos problemas de usabilidade**

| Grau de severidade | Tipo | Descrição |
| ----- | :---- | :---- |
| 0 | Sem importância | Não afeta a operação da interface |
| 1 | Cosmético | Não há necessidade imediata de solução |
| 2 | Simples | Problema de baixa prioridade (pode ser reparado) |
| 3 | Grave | Problema de alta prioridade (deve ser reparado) |
| 4 | Catastrófico | Muito grave, deve ser reparado de qualquer forma. |

---

## Tabela Padrão de Declaração de Violação (adotada pela equipe)

> **_NOTE:_**: Formato padrão adotado pela equipe para registro de todas as violações heurísticas encontradas.

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| — | — | — | — | — |

---

## H1 — Visibilidade do Status do Sistema

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Emissão em Lote — Tela de Processamento Blockchain | Durante o processamento assíncrono dos registros na blockchain, o sistema não exibe o status individual de cada diploma no lote (ex: "Registro 43/200 — falhou"). O usuário (Maria Eduarda) não consegue acompanhar o progresso detalhado e não sabe se o processo está travado ou apenas lento. | 3 | Implementar uma barra de progresso com contador de registros processados ("Emitindo diploma 43 de 200…") e um log em tempo real listando o status de cada registro (sucesso/falha) à medida que é processado pela blockchain. |
| 2 | Listagem de Diplomas — Painel do Estudante | O status do diploma (Válido, Pendente, Inválido) não é apresentado de forma visualmente destacada na listagem. O estudante (Lucas) precisa abrir cada diploma individualmente para verificar sua situação atual, sem qualquer indicador de estado na visão geral. | 2 | Adicionar um badge/etiqueta colorida visível diretamente na listagem para cada diploma: verde (Válido), amarelo (Pendente), vermelho (Inválido), seguindo o padrão de sistemas de gerenciamento de documentos como o e-diploma e o Credly. |

---

## H2 — Compatibilidade entre Sistema e Mundo Real

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Tela de Validação de Diploma (pública, sem login) | O campo de entrada para a recrutadora (Ana Carolina) é rotulado como "Insira a hash do diploma". O termo "hash" é um conceito técnico de computação e não faz parte do vocabulário de uma profissional de RH sem formação técnica, gerando confusão sobre o que deve ser inserido. | 3 | Substituir o rótulo do campo por "Insira o código de autenticidade do diploma" e adicionar um texto explicativo discreto abaixo: "O código pode ser encontrado no QR Code ou no rodapé do diploma digital enviado pelo estudante." |
| 2 | Tela de Detalhes do Diploma — visão da recrutadora | Após a validação, o resultado exibe o identificador do contrato inteligente na blockchain (ex: `0x3A4f…cB91`) como dado de confirmação da autenticidade, sem qualquer explicação contextual. O dado é irrelevante e incompreensível para a recrutadora. | 2 | Substituir ou ocultar o endereço do contrato. Exibir em destaque apenas: nome do formando, curso, instituição, data de colação e o texto "Diploma autenticado e registrado na blockchain em [data]". Disponibilizar os detalhes técnicos em uma seção expansível "Ver detalhes técnicos" para quem necessitar. |

---

## H3 — Controle e Liberdade para o Usuário

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Tela de Confirmação — Emissão em Lote | Após clicar em "Confirmar Emissão", o processamento na blockchain é iniciado imediatamente e de forma irreversível, sem nenhuma etapa intermediária de confirmação ou aviso explícito sobre a imutabilidade da operação. A analista (Maria Eduarda) não tem saída de emergência após este ponto. | 3 | Inserir um modal de confirmação explícita antes do disparo do processo, com texto claro: "Após confirmar, os diplomas serão registrados permanentemente na blockchain e não poderão ser desfeitos. Você revisou todos os dados?" com botões "Cancelar" e "Confirmar definitivamente". |
| 2 | Fluxo de Importação de CSV — Etapa de Revisão | Ao revisar as inconsistências detectadas na importação do CSV, não há botão "Voltar" que retorne à etapa anterior (seleção do arquivo) sem perder todo o progresso de revisão. O usuário é obrigado a cancelar toda a operação e recomeçar do início. | 2 | Implementar navegação em etapas (stepper) com botões "Voltar" e "Próximo" em todas as etapas do fluxo de emissão em lote, preservando os dados já revisados ao navegar entre as etapas. |

---

## H4 — Consistência e Padrões

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Múltiplas telas do sistema | O sistema usa "diploma" e "certificado" de forma intercambiável em diferentes telas e mensagens, sendo que os dois documentos têm natureza jurídica e contextos de uso distintos. Isso gera ambiguidade para a analista e para o estudante, que não sabem se estão interagindo com o mesmo tipo de documento. | 2 | Definir e aplicar um glossário de termos padrão em toda a interface. "Diploma" refere-se exclusivamente ao documento de conclusão de curso de graduação (sujeito à Portaria MEC nº 554/2019); "Certificado" refere-se a cursos de extensão, especializações e outras formações não reguladas pelo mesmo ato. |
| 2 | Botões de ação primária em diferentes telas | O botão de ação principal (call-to-action) apresenta variações de estilo e posicionamento: em algumas telas aparece como "Confirmar", em outras como "Prosseguir" e em outras como "Avançar", todos representando o mesmo tipo de ação (avançar na navegação). | 1 | Padronizar o texto e a posição dos botões de ação primária em todo o sistema. Adotar "Continuar" para avançar entre etapas e "Confirmar" exclusivamente para ações irreversíveis, sempre posicionados à direita inferior do formulário. |

---

## H5 — Prevenção de Erros

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Tela de Validação — Campo de Hash | O campo de inserção da hash não realiza validação em tempo real do formato do código digitado. A recrutadora (Ana Carolina) pode inserir uma string em formato incorreto (ex: com espaços, caracteres especiais ou tamanho errado) e só receberá o feedback de erro após submeter o formulário e aguardar o processamento. | 3 | Implementar validação em tempo real (on-blur/on-change) no campo de hash, verificando o formato esperado (ex: string hexadecimal de 64 caracteres com prefixo "0x") imediatamente após o usuário terminar de digitar, antes da submissão. |
| 2 | Tela de Importação de CSV | O sistema não apresenta um modelo (template) para download do arquivo CSV com o formato correto esperado. A analista (Maria Eduarda) pode preparar o arquivo no formato errado e só descobrir o problema ao tentar importar, gerando retrabalho. | 3 | Disponibilizar na tela de importação um botão "Baixar modelo CSV" que entrega um arquivo pré-formatado com os cabeçalhos corretos e linhas de exemplo, além de exibir as regras de preenchimento (campos obrigatórios, formatos de data, limites de caracteres) antes do upload. |

---

## H6 — Reconhecimento em Lugar de Lembrança

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Painel da Analista — Gestão de Diplomas | A interface não oferece filtros ou indicadores visuais na listagem de diplomas que permitam distinguir rapidamente entre diplomas emitidos, pendentes de correção e inválidos. A analista (Maria Eduarda) precisa lembrar quais registros foram tratados em sessões anteriores, pois o sistema não mantém o contexto visível. | 2 | Adicionar filtros rápidos por status (Todos / Emitidos / Pendentes / Com erro / Invalidados) no topo da listagem, além de uma coluna "Status" claramente visível na tabela, eliminando a necessidade de memorização entre sessões de trabalho. |
| 2 | Fluxo de Validação — Tela de Resultado | Após concluir a validação de um diploma, o resultado não persiste na tela: ao pressionar "Voltar" ou recarregar a página, o resultado é perdido e a recrutadora (Ana Carolina) precisa lembrar e reinserir a hash para obter o resultado novamente. | 2 | Manter o resultado da última validação visível na tela ou oferecer opção de salvar/exportar o resultado como PDF, permitindo que a recrutadora retome o contexto sem precisar reinserir dados. |

---

## H7 — Flexibilidade e Eficiência de Uso

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Painel da Analista — Gestão de Diplomas | Não há suporte a ações em massa (bulk actions) na tabela de diplomas. A analista (Maria Eduarda), que gerencia centenas de registros diariamente, precisa selecionar e executar ações (ex: invalidar, reenviar notificação) individualmente em cada registro, tornando o fluxo ineficiente para usuários experientes. | 2 | Implementar seleção múltipla (checkbox) na tabela de diplomas com menu de ações em massa: "Invalidar selecionados", "Reenviar notificação para selecionados" e "Exportar selecionados", seguindo padrões de interfaces de gestão como o Google Admin ou sistemas ERP. |
| 2 | Sistema em geral | Nenhuma ação comum do fluxo de emissão possui atalho de teclado ou atalho de acesso rápido. Um usuário experiente como a analista não tem como acelerar tarefas repetitivas (ex: confirmar etapa, ir para a próxima linha de pendência) sem recorrer ao mouse em cada interação. | 1 | Implementar atalhos de teclado para ações frequentes (ex: Enter para confirmar, Esc para cancelar, Tab para navegar entre campos do formulário de correção) e documentá-los em tooltip sobre os botões correspondentes. |

---

## H8 — Projeto Minimalista e Estético

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Tela de Confirmação de Emissão — Pós-processamento | A tela de sucesso exibe dados técnicos da transação blockchain (Transaction Hash, Block Number, Gas Used, Nonce) em destaque na interface principal, informações irrelevantes para as três personas do sistema. Esses dados competem visualmente com a informação realmente importante: "X diplomas emitidos com sucesso". | 2 | Remover os dados técnicos da transação da visão principal. Exibir em destaque apenas o resumo operacional: quantidade de diplomas emitidos com sucesso, quantidade com falha e próximos passos. Os dados técnicos podem ser acessados em "Ver detalhes da transação" para fins de auditoria. |
| 2 | Tela de Perfil do Estudante | A tela exibe simultaneamente todas as informações dos diplomas (dados pessoais, dados do curso, histórico de emissões, dados da blockchain, link de compartilhamento, QR Code e botões de ação) em uma única visão não organizada, sobrecarregando o estudante (Lucas) com informações em excesso. | 2 | Reorganizar o conteúdo em seções expansíveis (accordions) ou abas: "Meu diploma", "Compartilhar" e "Detalhes técnicos", mostrando por padrão apenas as informações essenciais e progressivamente revelando detalhes conforme o interesse do usuário. |

---

## H9 — Auxiliar os Usuários a Reconhecer, Diagnosticar e Recuperar Erros

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Tela de Resultado — Emissão em Lote com Falha | Quando ocorre uma falha no registro de um diploma na blockchain, a mensagem exibida reproduz o código de erro técnico da EVM: "Transaction reverted: execution reverted". Esta mensagem é incompreensível para a analista (Maria Eduarda) e não indica o que causou o erro nem como corrigi-lo. | 3 | Substituir códigos técnicos por mensagens em linguagem natural, específicas por tipo de falha. Ex: "Não foi possível registrar o diploma de [Nome do Formando] — o CPF informado já está associado a outro registro. Acesse 'Corrigir Pendência' para resolver." Cada mensagem deve indicar o problema e sugerir a ação de recuperação. |
| 2 | Tela de Validação — Hash não encontrada | Quando a recrutadora (Ana Carolina) insere uma hash válida em formato, mas que não corresponde a nenhum diploma registrado, o sistema exibe apenas "Diploma não encontrado" sem nenhuma orientação sobre o que fazer a seguir — se a hash está incorreta, se o diploma ainda não foi emitido ou se é um possível diploma fraudulento. | 3 | Enriquecer a mensagem de erro com contexto e orientação: "Nenhum diploma foi encontrado com este código. Possíveis causas: (1) o código foi digitado com erro — verifique os caracteres; (2) o diploma ainda não foi emitido pela instituição; (3) o documento pode não ser autêntico. Em caso de dúvida, entre em contato com a instituição emissora." |

---

## H10 — Ajuda e Documentação

> **_NOTE:_**: **colocar o print**

| # | Tela / Local | Descrição da Violação | Severidade | Recomendação de Correção |
| :---: | :--- | :--- | :---: | :--- |
| 1 | Sistema em geral — Primeiro acesso da recrutadora | O sistema não oferece nenhum fluxo de onboarding ou tutorial para novos usuários do perfil recrutador. A recrutadora (Ana Carolina) que acessa a plataforma pela primeira vez, ao seguir um link de validação enviado por um candidato, não recebe nenhuma orientação sobre como a validação funciona ou o que o resultado significa no contexto de autenticidade de diplomas via blockchain. | 2 | Implementar um tour guiado (tooltip walkthrough) exibido no primeiro acesso do perfil recrutador, com no máximo 3 etapas: (1) "Insira o código do diploma aqui"; (2) "Clique em Validar para consultar a blockchain"; (3) "O resultado confirma se o diploma é autêntico". Deve ser dispensável por um "x" no canto superior. |
| 2 | Tela de Importação de CSV — Painel da Analista | Não existem tooltips, dicas contextuais ou links para documentação nos campos do formulário de importação. A analista (Maria Eduarda), ao encontrar mensagens de erro de validação dos dados do CSV (ex: "CPF inválido na linha 37"), não tem acesso imediato a orientações sobre o formato correto esperado sem sair da tela atual. | 2 | Adicionar ícones de ajuda (?) ao lado de cada campo e campo de erro com link "O que significa esse erro?" que expande uma explicação inline sem redirecionar o usuário para outra página. Adicionalmente, criar uma página de FAQ acessível pelo menu lateral com os erros mais comuns de importação e suas soluções. |

---

2. **INDICAÇÃO DE BOAS PRÁTICAS DE HEURÍSTICA \- HEURÍSTICAS NÃO VIOLADAS \[1 solução completa por pessoa da equipe\]**

> **_NOTE:_**: **1 EXEMPLO DO SEU SISTEMA ONDE A HEURÍSTICA FOI ATENDIDA (ISSO NÃO É USADO NO MERCADO, SERVE APENAS PARA APRENDIZADO)**

---

### BP-H1 — Visibilidade do Status do Sistema 

**Tela:** Emissão em Lote — Progresso da emissão  
**Boa prática identificada:** Durante o processamento em lote, o sistema exibe uma barra de progresso com o percentual concluído ("Processando… 67%") e o número total de registros submetidos à blockchain. Ao finalizar, é exibido automaticamente um relatório resumo com os totais de diplomas emitidos com sucesso, falhas e pendentes — mantendo a analista (Maria Eduarda) informada do estado completo da operação durante toda a execução.

> **_NOTE:_**: **colocar o print**

---

### BP-H2 — Compatibilidade entre Sistema e Mundo Real 

**Tela:** Painel da Analista — Menu de navegação lateral  
**Boa prática identificada:** O menu de navegação utiliza terminologia familiar ao contexto acadêmico da analista (Maria Eduarda): "Emitir Diplomas", "Formandos", "Histórico de Emissões", "Corrigir Pendências" — sem exposição de jargões técnicos como "smart contract", "ledger" ou "nó da rede". A organização segue a lógica do fluxo real de trabalho da secretaria acadêmica, do recebimento dos dados à emissão e correção.

> **_NOTE:_**: **colocar o print**

---

### BP-H3 — Controle e Liberdade para o Usuário 

**Tela:** Fluxo de Importação — Etapa de revisão de inconsistências  
**Boa prática identificada:** Na etapa de revisão de dados inconsistentes do CSV, o sistema oferece ao usuário (Maria Eduarda) a escolha explícita entre "Prosseguir apenas com os registros válidos" ou "Cancelar e corrigir o arquivo". Nenhuma das opções é executada automaticamente — o sistema aguarda a decisão consciente da analista, garantindo que ela mantenha o controle total sobre o que será enviado para emissão.

> **_NOTE:_**: **colocar o print**

---

### BP-H4 — Consistência e Padrões 

**Tela:** Todos os modais de confirmação do sistema  
**Boa prática identificada:** Todos os modais de confirmação de ações críticas no sistema (confirmar emissão, invalidar diploma, reenviar notificação) seguem o mesmo padrão visual e estrutural: ícone de aviso, título descritivo da ação, texto explicativo das consequências, e dois botões no rodapé — "Cancelar" (esquerda, estilo secundário) e "Confirmar" (direita, estilo primário). Essa consistência reduz a curva de aprendizado e evita que o usuário cometa erros por falta de familiaridade com o padrão da interface.

> **_NOTE:_**: **colocar o print**

---

### BP-H5 — Prevenção de Erros 

**Tela:** Emissão em Lote — Etapa de Revisão do Lote  
**Boa prática identificada:** Antes de confirmar a emissão, o sistema exibe uma tela de revisão com uma amostra dos diplomas a serem emitidos (nome, CPF, curso, data de colação) e um resumo estatístico do lote (total de registros válidos, total de pendências, cursos envolvidos). Isso permite que a analista (Maria Eduarda) identifique visualmente qualquer anomalia — como um curso errado ou uma data inconsistente — antes de iniciar o processo irreversível de registro na blockchain.

> **_NOTE:_**: **colocar o print**

---

### BP-H6 — Reconhecimento em Lugar de Lembrança 

**Tela:** Fluxo de Validação — Tela pública de validação de diploma  
**Boa prática identificada:** A tela de validação pública (acessada pela recrutadora Ana Carolina) apresenta instruções visíveis diretamente na tela sem necessidade de consultar documentação externa: um ícone indicando onde encontrar o código de validação no diploma digital e o botão de ação claramente rotulado. O fluxo completo — "inserir código → validar → ver resultado" — é compreensível em uma única visão sem que o usuário precise lembrar etapas aprendidas anteriormente.

> **_NOTE:_**: **colocar o print**

---

### BP-H7 — Flexibilidade e Eficiência de Uso 

**Tela:** Sistema — Diferentes pontos de entrada por perfil de usuário  
**Boa prática identificada:** O sistema oferece diferentes níveis de complexidade de acesso por perfil: a recrutadora (Ana Carolina) acessa um fluxo simplificado de validação público sem necessidade de cadastro, com apenas 1 campo e 1 botão; o estudante (Lucas) tem uma interface pessoal de autoatendimento focada em visualização e compartilhamento; e a analista (Maria Eduarda) tem acesso a um painel completo com recursos avançados de gestão em lote. Cada perfil tem a complexidade adequada à sua necessidade, sem sobrecarregar os usuários menos experientes.

> **_NOTE:_**: **colocar o print**

---

### BP-H8 — Projeto Minimalista e Estético 

**Tela:** Tela de Validação Pública — Resultado positivo  
**Boa prática identificada:** A tela de resultado de uma validação bem-sucedida exibe apenas as informações essenciais para a decisão da recrutadora (Ana Carolina): nome completo do formando, curso, instituição emissora, data de colação e um selo visual claro de "Diploma Autêntico ✓". Não são exibidos campos desnecessários, menus laterais, propagandas ou outras informações que possam distrair do objetivo central da tela.

> **_NOTE:_**: **colocar o print**

---

### BP-H9 — Auxiliar os Usuários a Reconhecer, Diagnosticar e Recuperar Erros 

**Tela:** Tela de Importação de CSV — Relatório de inconsistências  
**Boa prática identificada:** Quando o arquivo CSV contém erros de formatação, o sistema exibe uma tabela com todas as linhas problemáticas, indicando para cada uma: o número da linha, o campo com problema ("CPF — formato inválido"), o valor que foi encontrado e o formato esperado ("Esperado: 000.000.000-00"). Essa mensagem em linguagem natural, com localização precisa e formato esperado, permite que a analista (Maria Eduarda) corrija o arquivo de forma eficiente sem tentativa e erro.

> **_NOTE:_**: **colocar o print**

---

### BP-H10 — Ajuda e Documentação 

**Tela:** Tela de Visualização de Diploma — Painel do Estudante  
**Boa prática identificada:** Na tela de visualização do diploma, o estudante (Lucas) encontra um botão "Como compartilhar meu diploma?" que expande inline (sem sair da página) um guia passo a passo com 3 opções de compartilhamento: (1) copiar link de validação pública, (2) baixar PDF com QR Code embutido, e (3) adicionar ao LinkedIn. As instruções são centradas na tarefa do usuário, com linguagem simples, sem jargões técnicos e com ícones visuais para cada opção.

> **_NOTE:_**: **colocar o print**
