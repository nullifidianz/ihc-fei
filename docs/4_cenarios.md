# Cenários de Análise/Problema

## Cenário 1 — Persona Primária 1: Analista de Emissão de Diplomas

**Responsável:** Leandro de Brito Alencar

---

### Narrativa: Emissão de diplomas após colação de grau com dados inconsistentes e notificação de formandos

Na segunda-feira seguinte à colação de grau de dezembro, Maria Eduarda Santos, analista de emissão de diplomas da Universidade Privada Horizonte, precisa cadastrar e emitir os diplomas digitais dos 238 alunos que colaram grau na sexta-feira anterior. O processo começa quando a secretaria acadêmica envia por e-mail um arquivo CSV exportado do sistema acadêmico da universidade (SIGA) com os dados dos formandos.

Ao tentar importar o arquivo no sistema de emissão de diplomas, Maria recebe uma mensagem de erro informando que o formato do CSV não é compatível. O sistema acadêmico e o sistema de diplomas foram desenvolvidos por fornecedores diferentes e não compartilham o mesmo padrão de exportação. Maria abre o arquivo no Excel, renomeia manualmente as colunas para o padrão esperado e remove a formatação dos campos de CPF antes de tentar a importação novamente.

Com o arquivo corrigido, o sistema aceita os registros, mas Maria percebe que vários campos obrigatórios para emissão — como data de ingresso, turno e habilitação do curso — não estavam no CSV enviado pela secretaria. Esses campos precisam ser preenchidos manualmente, um a um, para cada formando. Para cada aluno, Maria precisa abrir o SIGA em outra aba do navegador, buscar o cadastro pelo CPF, consultar as informações e voltar ao sistema de diplomas para digitá-las. Ela repete essa sequência 238 vezes ao longo do dia.

Durante o preenchimento, Maria nota que o aluno João Pedro Santos tem data de nascimento registrada no CSV como 1952. Como o SIGA não está integrado ao sistema de diplomas, ela não consegue acessar o cadastro correto de dentro do sistema — precisa sair da tela em que está trabalhando, buscar o aluno no SIGA separadamente, confirmar que a data correta é 2002 e retornar ao cadastro para corrigir. Ao voltar, percebe que o sistema exibiu uma mensagem de sessão expirada e não salvou o trabalho dos últimos três alunos preenchidos. Ela refaz os registros.

Ao acionar a emissão dos diplomas ao final do dia, o sistema processa os registros sem exibir nenhum indicativo de progresso. A tela permanece carregando por catorze minutos. Quando a tela atualiza, o sistema informa que 236 diplomas foram emitidos, mas não indica quais dois registros apresentaram falha nem o motivo. Maria precisa comparar manualmente a lista dos 238 nomes com os registros emitidos no sistema para identificar os casos de Lucas Mendes e Rodrigo Carvalho como os que falharam.

Para avisar os formandos de que seus diplomas estão disponíveis, Maria tenta usar o botão "Notificar Alunos" do sistema, que exibe a mensagem de que o módulo de e-mail não está configurado. Ela então abre o Outlook e começa a enviar os avisos individualmente. Como o sistema de diplomas não armazena o e-mail dos alunos, ela precisa buscar cada endereço no SIGA em outra aba e copiá-lo para o Outlook a cada envio. Ao tentar notificar a aluna Fernanda Oliveira, o e-mail é devolvido por endereço inválido. Maria anota o caso num post-it para resolver no dia seguinte.

Ao encerrar o expediente, Maria ainda não havia notificado 35 dos 236 formandos com diplomas emitidos. Os dois diplomas com falha — Lucas e Rodrigo — permanecem sem resolução, pois o sistema não oferece informações sobre o motivo das falhas e ela não conseguiu identificar a causa apenas pela comparação manual dos registros.

---

### Elementos do Cenário

| Elemento | Descrição |
|---|---|
| **Ambiente** | Setor de emissão de diplomas de universidade privada em SP; escritório calmo e bem iluminado; múltiplos sistemas abertos em paralelo |
| **Atores** | Maria Eduarda Santos (analista de emissão de diplomas); secretaria acadêmica (fornecedora dos dados); formandos (238 alunos aguardando diploma) |
| **Objetivos** | Cadastrar e emitir 238 diplomas digitais; notificar os formandos sobre a disponibilidade do documento |
| **Planejamento** | Receber CSV da secretaria, importar no sistema, completar dados faltantes, emitir em lote, notificar alunos |
| **Ações** | Correção manual do CSV; busca individual de dados no SIGA; preenchimento manual de campos para cada formando; comparação manual para identificar falhas; envio de e-mails pelo Outlook com endereços buscados no SIGA |
| **Eventos** | Erro de incompatibilidade do CSV; sessão expirada sem aviso prévio; emissão concluída sem indicação de progresso nem detalhamento das falhas; módulo de e-mail desconfigurado; e-mail inválido devolvido |
| **Avaliação** | Expediente encerrado com trabalho incompleto: 2 diplomas sem emissão por motivo desconhecido, 35 notificações pendentes, nenhuma resposta sobre os problemas técnicos reportados ao setor de TI |

---

## Cenário 2

**Responsável:** Thales Clemente Pasquotto

---

### Narrativa: Validação de diplomas por recrutadora de empresa interessada

### Atores: Ana Carolina Ferreira (recrutadora) e Lucas Mendes (estudante)

Ana Carolina Ferreira é recrutadora em uma empresa de tecnologia de médio porte. Em seu dia a dia, ela analisa dezenas de currículos para vagas que exigem formação superior específica. Um dos candidatos finalistas para a vaga de Desenvolvedor Backend, Lucas Mendes, afirma possuir diploma de Bacharelado em Ciência da Computação.

Ana Carolina já enfrentou situações anteriores em que candidatos apresentaram diplomas falsificados ou certificados de instituições não reconhecidas. Em processos tradicionais, a verificação exige contato com a universidade por e-mail ou telefone, o que leva dias — às vezes semanas — para confirmação, ou solicita ao candidato Lucas que envie o histórico da Universidade. Isso atrasa o processo seletivo e compromete prazos internos.

Após receber a solicitação, Lucas Mendes busca sua Universidade e solicita o histórico afim de comprovar seus estudos, o que pode demorar até um semana de acordo com a própria instituição - isso deixa Lucas Mendes apreensivo de perder a vaga. Após receber o documento, Lucas Mendes envia-o à Ana Carolina Ferreira.

Após receber o documento de Lucas Mendes (ou confirmação de validade da Instituição de Ensino), Ana Carolina Ferreira registra isso em sistema e prossegue com os devidos trâmites referente à contratação ou prosseguimento das fases de entrevista.

---

### Perguntas de refinamento

| Elemento | Pergunta |
|---|---|
| **[1] Ambiente ou Contexto** | A empresa possui prazo formal para fechamento da vaga? |
| **[2] Atores** | Quais são as expectativas emocionais de Lucas (ansiedade, urgência, insegurança)? |
| **[3] Objetivos** | Lucas Mendes vê a validação como etapa burocrática ou decisiva? |
| **[4] Planejamento** | Existe planejamento de contingência caso a universidade não responda? |
| **[5] Ações** | Lucas envia o histórico por e-mail ou plataforma da empresa? |
| **[6] Eventos** | O sistema interno da empresa gera alerta de pendência? |
| **[7] Avaliação** | Lucas interpreta a exigência como desconfiança ou procedimento padrão? |

---

### Narrativa revisada

### Atores: Ana Carolina Ferreira (recrutadora) e Lucas Mendes (estudante)

Ana Carolina Ferreira é recrutadora em uma empresa de tecnologia de médio porte. Em seu dia a dia, ela analisa dezenas de currículos para vagas que exigem formação superior específica. Um dos candidatos finalistas para a vaga de Desenvolvedor Backend, Lucas Mendes, afirma possuir diploma de Bacharelado em Ciência da Computação.

Ana Carolina já enfrentou situações anteriores em que candidatos apresentaram diplomas falsificados ou certificados de instituições não reconhecidas. Em processos tradicionais, a verificação exige contato com a universidade por e-mail ou telefone, o que leva dias — às vezes semanas — para confirmação, ou solicita ao candidato Lucas que envie o histórico da Universidade. Isso atrasa o processo seletivo e compromete prazos internos, que para o caso é de 1 (uma) semana[1], sendo que no 5º (quinto) dia, o sistema da empresa gera um alerta de pendência de documentação[6].

Após receber a solicitação, Lucas Mendes busca sua Universidade e solicita o histórico afim de comprovar seus estudos, o que pode demorar até um semana de acordo com a própria instituição - isso deixa Lucas Mendes apreensivo de perder a vaga[2], afinal, ele acredita que essa validação se trata de um processo padrão[7] e decisivo[3]. Caso a Universidade demore mais que 4 dias, Lucas planeja ir presencialmente verificar a situação[4], para garantir que não perca o prazo e que tudo corre bem. Após receber o documento, Lucas Mendes envia-o à Ana Carolina Ferreira via e-mail[5], solicitando também confirmação de recebimento.

Após receber o documento de Lucas Mendes (ou confirmação de validade da Instituição de Ensino), Ana Carolina Ferreira registra isso em sistema e prossegue com os devidos trâmites referente à contratação ou prosseguimento das fases de entrevista.
