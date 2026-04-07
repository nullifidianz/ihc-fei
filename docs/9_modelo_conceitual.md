1. **Cenários de Interação**

   > **_NOTE:_**: destacar em negrito o texto alterado entre Cenário Problema e Cenário de Interação

2. **Design Centrado na Comunicação**

**Nome do Cenário: XXXXXX**

| tópico \> subtópico (diálogo) | falas e signos                     |
| :---------------------------- | :--------------------------------- |
|                               | U: Preciso …                       |
| \>                            | U: Quero … D: Aqui está o mapa     |
|                               | U:                                 |
|                               | U:                                 |
|                               | D: Aqui está a informação filtrada |

3. **Mapa de Objetivos**

   > **_NOTE:_**: cada um coloca seu mapa de objetivos e deverá ter um diagrama de consolidação

4. **Esquema Conceitual de Signos**

> **_NOTE:_**: fazer a junção das 3 tabelas abaixo em uma única

| Credenciais (C) \- credenciais para acesso ao sistema |            |                 |
| :---------------------------------------------------- | :--------- | :-------------- |
| **signo**                                             | **origem** | **observações** |
| usuário                                               | domínio    |                 |
| senha                                                 | domínio    |                 |

| Credenciais (C) \- credenciais para acesso ao sistema |                      |                              |                   |
| :---------------------------------------------------- | :------------------- | :--------------------------- | :---------------- |
| **signo**                                             | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** |
| usuário                                               | texto                | não pode ser nulo            | —                 |
| senha                                                 | texto                | não pode ser nulo            | —                 |

| Credenciais (C) \- credenciais para acesso ao sistema |                       |                 |
| :---------------------------------------------------- | :-------------------- | :-------------- |
| **signo**                                             | **prevenção**         | **recuperação** |
| usuário                                               | PP: campo obrigatório | RA              |
| senha                                                 | PP campo obrigatório  | RA              |
