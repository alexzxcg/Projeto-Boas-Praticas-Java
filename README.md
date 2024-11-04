# Adopet Console Application - Projeto de Refatoração

**Adopet Console Application** é uma aplicação Java para interação com um sistema de abrigos de animais via linha de comando (CLI). Este projeto visa a refatoração de um código legado, originalmente desenvolvido sem boas práticas de programação, transformando-o em um sistema modular, fácil de manter e estender.

## Problemas Identificados

Na análise do código atual, foram detectados os seguintes problemas principais:

1. **Acoplamento excessivo e falta de modularização**: Todas as funcionalidades estão no método `main`, dificultando manutenção e extensibilidade.
2. **Mistura de responsabilidades**: A aplicação mistura lógica de negócios, controle de fluxo e manipulação de dados, violando o princípio de responsabilidade única (SRP).
3. **Repetição de código**: Uso redundante de instâncias e operações, como `Scanner` e `HttpClient`, resultando em duplicação desnecessária.
4. **Falta de separação de camadas**: Não há divisão clara entre interface de usuário, lógica de negócios e acesso a dados.
5. **Tratamento de erros genérico**: Exceções são capturadas sem tratamento específico, dificultando a detecção e a recuperação de erros.

## Objetivos da Refatoração

Este projeto aplica os princípios da programação orientada a objetos e SOLID, resultando em um sistema mais organizado e modular:

### Princípios SOLID Aplicados

1. **Single Responsibility Principle (SRP)**: Divisão em classes especializadas para manipulação de dados de abrigos e pets, interface de usuário e controle de regras de negócios.
2. **Open/Closed Principle (OCP)**: Estrutura de código preparada para extensões, especialmente para novas funcionalidades e integrações com APIs.
3. **Liskov Substitution Principle (LSP)**: Uso de interfaces e abstrações para assegurar que classes derivadas substituam superclasses sem alterar o comportamento.
4. **Interface Segregation Principle (ISP)**: Interfaces específicas para funções distintas, evitando a implementação de métodos desnecessários.
5. **Dependency Inversion Principle (DIP)**: Classes de alto nível dependem de abstrações em vez de implementações concretas, permitindo testes e troca de componentes.

## Benefícios Esperados

Após a refatoração, o Adopet Console Application deverá ser:

- **Mais legível e organizado**: Código modular e fácil de seguir, com classes especializadas.
- **Extensível**: Estrutura pronta para a adição de novas funcionalidades e interfaces.
- **Fácil de manter**: Com menor acoplamento e maior clareza de responsabilidades, será mais simples realizar melhorias.
- **Testável**: A separação em camadas facilita testes unitários e de integração, melhorando a confiabilidade.

---

Esse projeto de refatoração transformará o Adopet Console Application em uma base de código mais sólida, moderna e pronta para futuras evoluções.
