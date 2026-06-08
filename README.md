# Conversor Numérico

Aplicação desktop desenvolvida em **Java + Swing** que realiza conversões entre as principais bases numéricas: **Binário**, **Octal**, **Decimal** e **Hexadecimal**, com suporte a números fracionários.

> Trabalho acadêmico desenvolvido para a disciplina de **Exploração Digital e Fundamentos Tecnológicos** no curso de Ciência da Computação.

---

## Funcionalidades

- Conversão em tempo real entre as bases:
  - **Binário** (Base 2)
  - **Octal** (Base 8)
  - **Decimal** (Base 10)
  - **Hexadecimal** (Base 16)
- Suporte a **números fracionários** (separador: vírgula `,`)
- Interface gráfica intuitiva construída com **Java Swing**
- Sincronização automática dos campos: ao editar qualquer campo, os demais são atualizados instantaneamente

---

## Tecnologias

| Tecnologia | Versão mínima |
|---|---|
| Java (JDK) | 17+ |
| Java Swing | Incluso no JDK |
| Maven | 3.8+ |

---

## Estrutura do Projeto

```
ConversorNumerico/
├── src/
│   └── main/
│       └── java/
│           └── com/
│               └── ...          # Classes Java (conversores, UI)
├── pom.xml                      # Configuração Maven
├── .gitignore
├── LICENSE
└── README.md
```

---

## Como Executar

### Pré-requisitos

- [JDK 17+](https://adoptium.net/) instalado
- [Maven 3.8+](https://maven.apache.org/) instalado
- Variável de ambiente `JAVA_HOME` configurada corretamente

### Clonando o repositório

```bash
git clone https://github.com/Arthur-Kroth/ConversorNumerico.git
cd ConversorNumerico
```

### Executando com Maven

```bash
mvn clean package exec:java
```

### Executando no NetBeans

1. Abra o NetBeans e vá em **File → Open Project**
2. Navegue até a pasta do repositório clonado e selecione-a (o NetBeans reconhece projetos Maven automaticamente)
3. Aguarde o NetBeans indexar e baixar as dependências do `pom.xml`
4. Clique com o botão direito no projeto no painel **Projects** e selecione **Run** (ou pressione `F6`)

### Executando no VS Code

1. Abra a pasta do projeto no VS Code
2. Certifique-se de ter a extensão **Extension Pack for Java** instalada
3. Use o terminal integrado e execute: `mvn clean package exec:java`

### Executando no IntelliJ IDEA

1. Abra o projeto via **File → Open** selecionando o `pom.xml`
2. Aguarde o Maven sincronizar as dependências
3. Clique com o botão direito na classe `Main` e selecione **Run**

---

## Como Funciona

A aplicação usa o **Decimal como base intermediária** para todas as conversões:

```
Qualquer Base  →  Decimal  →  Qualquer Base
```

Para **números fracionários**, a conversão é feita separando a parte inteira da parte fracionária:

- **Parte inteira:** divisões sucessivas pela base de destino
- **Parte fracionária:** multiplicações sucessivas pela base de destino

O separador decimal utilizado é a **vírgula** (`,`), seguindo o padrão brasileiro.

---

## Detalhes de Implementação

- Os campos de entrada utilizam **listeners em tempo real** para disparar conversões automaticamente
- Um flag `isUpdating` evita loops infinitos de atualização entre os campos
- As conversões são implementadas como métodos estáticos puros, sem dependência de bibliotecas externas

---

## Contexto Acadêmico

Este projeto foi desenvolvido como trabalho prático para demonstrar o domínio de:

- Representação de números em diferentes bases numéricas
- Algoritmos de conversão entre bases (inteiros e fracionários)
- Desenvolvimento de interfaces gráficas com Java Swing
- Boas práticas de orientação a objetos em Java
- Controle de versão com Git e GitHub

---

## Autores

| Nome Completo                         | GitHub                                           | RA          |
| ------------------------------------- |--------------------------------------------------| ----------- |
| Arthur Kroth Posselt                  | [@Arthur-Kroth](https://github.com/Arthur-Kroth) | 10725115044 |
| Gabriel Machado da Fonseca            | [@Machadox18](https://github.com/Machadox18)     | 10725115066 |
