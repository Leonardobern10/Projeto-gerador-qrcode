# Ferramentas de Gerador de QR Code e Senha

Este projeto é uma aplicação simples em Node.js que oferece duas ferramentas úteis: um gerador de QR Code e um gerador de senhas. O objetivo é fornecer uma interface de linha de comando interativa para gerar QR Codes a partir de links e criar senhas seguras com base em preferências definidas pelo usuário.

## Funcionalidades

1. **Gerador de QR Code**: Gera um QR Code a partir de um link fornecido pelo usuário. O usuário pode escolher entre dois tipos de QR Code: Normal ou Terminal.

2. **Gerador de Senhas**: Cria uma senha aleatória com base em parâmetros configuráveis, como comprimento da senha e tipos de caracteres permitidos (letras maiúsculas, minúsculas, números e caracteres especiais).

## Abordagem

- **Programação Assíncrona**: Utilização de funções assíncronas e `await` para gerenciar operações de entrada e saída.
- **Manipulação de Dados com Prompts**: Criação e validação de esquemas de prompts interativos para a entrada do usuário.
- **Gerenciamento de Dependências**: Uso de pacotes como `prompt`, `chalk` e `qrcode-terminal` para funcionalidades específicas.
- **Trabalho com Variáveis de Ambiente**: Configuração e uso de variáveis de ambiente para personalização da geração de senhas.
- **Criação de QR Codes**: Geração e exibição de QR Codes usando a biblioteca `qrcode-terminal`.
- **Geração de Senhas Seguras**: Implementação de lógica para gerar senhas seguras com base em configurações do usuário.
- **Estrutura de Projeto Modular**: Organização do código em módulos e serviços para melhor manutenção e reutilização.

## Instalação

Para começar a usar este projeto, siga estas etapas:

1. **Clone o Repositório**:
   ```bash
   git clone https://github.com/Leonardobern10/Projeto-gerador-qrcode.git
   cd Projeto-gerador-qrcode
   ```

2. **Instale as Dependências**:
   Certifique-se de ter o Node.js instalado. Então, execute:
   ```bash
   npm install
   ```

3. **Configure as Variáveis de Ambiente**:
   Crie um arquivo `.env` na raiz do projeto e defina as variáveis de ambiente necessárias:
   ```
   PASSWORD_LENGTH="tamanho_da_senha"
   UPPERCASE_LETTERS="true or false"
   LOWERCASE_LETTERS="true or false"
   NUMBERS="true or false"
   SPECIAL_CHARACTERS="true or false"
   ```

## Uso

1. **Inicie o Programa**:
   ```bash
   node src/index.js
   ```

2. **Escolha uma Ferramenta**:
   O programa irá pedir para você escolher entre gerar um QR Code ou uma senha.

   - **Para Gerar um QR Code**:
     - Insira o link que deseja codificar.
     - Escolha o tipo de QR Code (Normal ou Terminal).

   - **Para Gerar uma Senha**:
     - O programa irá gerar uma senha aleatória com base nas configurações definidas nas variáveis de ambiente.

## Estrutura do Projeto

- `index.js`: Ponto de entrada principal que gerencia o fluxo do programa e as escolhas do usuário.
- `services/qr-code/create.js`: Contém a lógica para gerar QR Codes.
- `services/password/create.js`: Contém a lógica para gerar senhas.
- `services/password/utils/permitted-characters.js`: Utilitário para determinar os caracteres permitidos na senha.
- `prompts-schema/schema-main.js`: Define o esquema de prompts principais para a escolha da ferramenta.
- `prompts-schema/schema-qrcode.js`: Define o esquema de prompts para gerar QR Codes.

## Contribuição

Sinta-se à vontade para abrir issues e enviar pull requests. Para contribuir com este projeto, siga estas etapas:

1. Fork o repositório.
2. Crie uma branch para sua alteração (`git checkout -b feature/nova-funcionalidade`).
3. Faça commit das suas alterações (`git commit -am 'Adiciona nova funcionalidade'`).
4. Envie para o repositório remoto (`git push origin feature/nova-funcionalidade`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

## Contato

Para mais informações, entre em contato com o autor:

- Nome: Leonardo de Almeida Bernardo
- Email: leonardo.bernardo2658@gmail.com
