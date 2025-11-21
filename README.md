# Projeto de Formulários PHP Simples

## Descrição
Este projeto demonstra a utilização básica de formulários HTML e processamento de dados com PHP. Consiste em três funcionalidades distintas, cada uma processada por um script PHP dedicado:
1.  **Saudação Personalizada:** Recebe um nome e exibe uma mensagem de boas-vindas.
2.  **Classificação de Idade:** Recebe uma idade e classifica a pessoa como Criança, Adolescente ou Adulto.
3.  **Verificação de Password:** Recebe uma password e classifica a sua força (Fraca, Média, Forte) com base no seu comprimento.

## Estrutura do Projeto

O projeto é composto pelos seguintes ficheiros:

| Ficheiro | Descrição |
| :--- | :--- |
| `form.html` | Contém os três formulários HTML para recolha de dados (Nome, Idade, Password). |
| `resultado.php` | Processa o formulário de **Nome** e exibe uma saudação personalizada. |
| `resultado_idade.php` | Processa o formulário de **Idade** e classifica a idade. |
| `resultado_password.php` | Processa o formulário de **Password** e avalia a sua força. |

## Funcionalidades Detalhadas

### 1. Saudação Personalizada
- **Ficheiro:** `resultado.php`
- **Lógica:** Recebe o valor do campo `nome` via método `POST` e exibe a string "Olá, [Nome]! Seja bem-vindo.".

### 2. Classificação de Idade
- **Ficheiro:** `resultado_idade.php`
- **Lógica:** Recebe o valor do campo `idade` via método `POST` e aplica a seguinte lógica:
    - Idade `< 12`: "👶 Criança"
    - Idade `12` a `17`: "🧒 Adolescente"
    - Idade `>= 18`: "🧑 Adulto"

### 3. Verificação de Força da Password
- **Ficheiro:** `resultado_password.php`
- **Lógica:** Recebe o valor do campo `pass` via método `POST` e avalia o seu comprimento (`strlen`):
    - Comprimento `< 5`: "Password fraca" (em vermelho)
    - Comprimento `5` a `8`: "Password média" (em laranja)
    - Comprimento `> 8`: "Password forte" (em verde)

## Como Executar o Projeto

Para executar este projeto, é necessário um ambiente de servidor web que suporte PHP (por exemplo, XAMPP, WAMP, MAMP ou um servidor Apache/Nginx com PHP instalado).

1.  **Configuração do Servidor:** Certifique-se de que o seu servidor web está a funcionar e que o PHP está ativado.
2.  **Colocação dos Ficheiros:** Coloque todos os ficheiros (`form.html`, `resultado.php`, `resultado_idade.php`, `resultado_password.php`) no diretório raiz do seu servidor web (por exemplo, `htdocs` no XAMPP).
3.  **Acesso:** Abra o seu navegador e navegue para o URL do ficheiro `form.html`. Se estiver a usar um servidor local, será algo como:
    ```
    http://localhost/form.html
    ```
4.  **Teste:** Preencha e submeta cada um dos três formulários para testar as diferentes funcionalidades.

## Requisitos
- Servidor Web (Apache, Nginx, etc.)
- PHP (versão 5.x ou superior)
