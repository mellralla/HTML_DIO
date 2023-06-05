# Trabalhando com formulários

## Tag **`<form>`**
A tag **`<form>`** é usada em HTML para criar formulários interativos que permitem aos usuários enviar dados para o servidor. São alguns atributos comumente usados dentro da tag **`<form>`**:

- **`action`**: Especifica a URL ou o arquivo de script para onde os dados do formulário serão enviados quando o formulário for submetido.
- **`method`**: Define o método HTTP usado para enviar os dados do formulário ao servidor. Os valores comuns são `GET` e `POST`. O método GET é recomendado para recuperar dados e exibir informações, enquanto o método POST é recomendado para enviar dados ao servidor e realizar operações que alteram o estado do servidor.
- **`name`**: Define um nome para o formulário, que pode ser usado para referenciá-lo em scripts ou estilização.
- **`target`**: Especifica o destino em que a resposta do servidor será exibida. Os valores comuns são `_blank`, `_self`, `_parent` e `_top`.
- **`autocomplete`**: Indica se o recurso de preenchimento automático do navegador deve ser ativado para os campos do formulário. Os valores são `on` e `off`.
- **`enctype`**: Define a codificação usada para enviar os dados do formulário. Comumente usado quando há envio de arquivos. Os valores comuns são `application/x-www-form-urlencoded` e `multipart/form-data`.
- **`novalidate**: Indica ao navegador para não validar os campos do formulário antes de enviá-lo ao servidor.
- **`onsubmit`**: Especifica um script ou função JavaScript que será executado quando o formulário for submetido.

Exemplo de uso da tag `<form>` com alguns atributos:

```html
<form action="/submit" method="POST" name="myForm" target="_blank" autocomplete="on">
  <!-- Campos do formulário aqui -->
  Nome: <input type="text" name="name"><br>
  Idade: <input type="number" name="age"><br>
  Senha: <input type="password" name="password"><br>
  <button type="submit">Enviar!</button>
</form>
```

## Tag `<input>`
A tag `<input>` é usada em HTML para criar campos de entrada interativos em formulários. Aqui estão alguns atributos comumente usados dentro da tag `<input>`:

- **`type`**: Especifica o tipo de campo de entrada. Incluem:
    - `text`: Cria um campo de texto simples para entrada de texto.
    - `password`: Cria um campo de senha onde os caracteres digitados são mascarados.
    - `number`: Cria um campo numérico onde apenas valores numéricos são permitidos.
    - `email`: Cria um campo para entrada de endereço de e-mail com validação básica.
    - `url`: Cria um campo para entrada de URLs (endereços de sites) com validação básica.
    - `checkbox`: Cria uma caixa de seleção que permite ao usuário selecionar uma ou várias opções.
    - `radio`: Cria botões de rádio onde apenas uma opção pode ser selecionada.
    - `file`: Cria um campo para seleção de arquivos a serem enviados para o servidor.
    - `submit`: Cria um botão de envio para enviar o formulário.
    - `reset`: Cria um botão de redefinição que redefine os valores do formulário para os valores padrão.
    - `date`: Cria um campo de entrada de data.
    - `time`: Cria um campo de entrada de hora.
    - `color`: Cria um campo para seleção de cores.
    - `range`: Cria um controle deslizante para selecionar um valor em um intervalo.
    - `search`: Cria um campo de pesquisa com funcionalidade adicional.
- **`name`**: Define o nome do campo de entrada, que é usado para identificar o valor do campo quando o formulário é enviado.
- **`value`**: Define o valor inicial do campo de entrada.
  - Para campos de texto, senha, número, e-mail, URL, data, hora, cor e outros tipos de entrada de texto:
    - `value="texto"`: Define um valor de texto inicial para o campo.
  - Para caixas de seleção (checkbox) e botões de rádio:
    - `value="valor"`: Define o valor associado ao campo de seleção ou botão de rádio. Quando o formulário é enviado, o valor associado ao campo selecionado é enviado.
  - Para campos de arquivo (file):
    - O atributo `value` não é aplicável a campos de arquivo. O valor exibido é determinado pelo navegador e não pode ser manipulado por esse atributo.
  > **⚠️** É importante observar que o atributo `value` define apenas o valor inicial do campo de entrada e não é atualizado automaticamente à medida que o usuário interage com o campo. Para capturar o valor atual do campo quando o formulário é enviado, é necessário utilizar uma linguagem de programação no lado do servidor ou JavaScript no lado do cliente.
- **`placeholder`**: Fornece um texto de dica dentro do campo de entrada que desaparece quando o usuário começa a digitar.
- **`required`**: Indica que o campo de entrada é obrigatório e deve ser preenchido antes do envio do formulário.
- **`disabled`**: Desativa o campo de entrada, impedindo que o usuário interaja com ele.
- **`readonly`**: Torna o campo de entrada somente leitura, permitindo que o usuário visualize o valor, mas não faça alterações.
- **`maxlength`**: Define o número máximo de caracteres permitidos no campo de texto.
- **`min`** e **`max`**: Especifica o valor mínimo e máximo permitido para campos numéricos.
- **`pattern`**: Define uma expressão regular que o valor do campo de entrada deve corresponder.
- **`autofocus`**: Faz com que o campo de entrada receba o foco automaticamente quando a página é carregada.

Exemplo de uso da tag `<input>` com alguns atributos:

```html
<input type="text" name="username" placeholder="Digite seu nome de usuário" required>
<input type="password" name="password" minlength="8" required>
<input type="number" name="age" min="18" max="99" required>
<input type="email" name="email" required>
```

## Tag `<button>`
A tag `<button>` é usada para criar um botão interativo em uma página HTML. Os botões podem ser usados para executar ações quando são clicados pelo usuário.

Exemplo de uso:

```html
<button>Click me!</button>
```
A tag `<button>` pode usar vários atributos para definir seu comportamento e aparência. Alguns dos atributos mais comuns incluem:

- **`type`**: Especifica o tipo de botão. Alguns valores possíveis são:
  - **`submit`**: Envia os dados do formulário ao servidor quando o botão é clicado.
  - **`reset`**: Reseta os campos do formulário para seus valores padrão quando o botão é clicado.
  - **`button`**: Comportamento padrão de um botão normal. Não executa ações específicas.
- **`name`**: Define o nome do botão, que é usado para identificar o valor do botão quando o formulário é enviado.
- **`value`**: Define o valor do botão, que é enviado junto com o formulário quando o botão é clicado.
- **`disabled`**: Desabilita o botão, tornando-o não interativo.
- **`onclick`**: Especifica um script a ser executado quando o botão é clicado.
- **`form`**: Especifica o ID do formulário ao qual o botão pertence.
- **`autofocus`**: Define que o botão deve receber o foco automaticamente quando a página é carregada.
- **`formaction`**: Especifica a URL do script ou arquivo que será acionado quando o botão é clicado.
- **`formmethod`**: Especifica o método de envio do formulário (GET ou POST) quando o botão é clicado.
- **`formtarget`**: Especifica onde abrir o resultado do envio do formulário quando o botão é clicado.

```html
<button type="submit" name="submitBtn" disabled>Enviar</button>
```
