A superglobal `$_FILES` é uma variável em PHP que é utilizada para manipular arquivos enviados através de um formulário HTML com o atributo `enctype` definido como `multipart/form-data`. Quando um formulário é enviado com este tipo de atributo, o PHP armazena as informações sobre os arquivos enviados nesta superglobal para que possam ser processadas pelo script PHP.

Veja uma visão geral dos principais elementos da superglobal `$_FILES`:

1. **Nome do Campo**: Cada arquivo enviado é identificado pelo nome do campo no formulário HTML que o enviou. Por exemplo:
   ```php
   // Acessando o arquivo enviado pelo campo "file_upload"
   $_FILES['file_upload']
   ```

2. **Nome do Arquivo Original**: `$_FILES['nome_do_campo']['name']` fornece o nome original do arquivo no computador do usuário.

3. **Tipo de Arquivo**: `$_FILES['nome_do_campo']['type']` contém o tipo MIME do arquivo enviado.

4. **Tamanho do Arquivo**: `$_FILES['nome_do_campo']['size']` fornece o tamanho do arquivo em bytes.

5. **Nome Temporário**: Durante o upload, o PHP armazena temporariamente o arquivo em um local temporário no servidor. Por exemplo:
   ```php
   // Acessando o nome temporário do arquivo enviado
   $_FILES['nome_do_campo']['tmp_name']
   ```

6. **Código de Erro**: `$_FILES['nome_do_campo']['error']` fornece um código indicando se ocorreu algum erro durante o upload do arquivo.

É fundamental validar os arquivos recebidos pela superglobal `$_FILES` para garantir segurança e integridade. Por exemplo, você pode verificar o tipo MIME, o tamanho máximo permitido e realizar outras verificações para prevenir vulnerabilidades, como ataques de injeção de código ou o upload de arquivos maliciosos para o servidor.

## Exemplos:

Aqui está um exemplo básico de como você pode utilizar a superglobal `$_FILES` em um script PHP para manipular arquivos enviados por um formulário HTML:

```php
<!DOCTYPE html>
<html>
<head>
    <title>Upload de Arquivos</title>
</head>
<body>

<form action="upload.php" method="post" enctype="multipart/form-data">
    Selecione um arquivo para fazer upload:
    <input type="file" name="file_upload">
    <input type="submit" value="Enviar Arquivo">
</form>

</body>
</html>
```

Agora, vamos criar o script PHP (`upload.php`) para processar o arquivo enviado:

```php
<?php
// Verificando se o arquivo foi enviado corretamente
if(isset($_FILES['file_upload'])) {
    $file = $_FILES['file_upload'];

    // Informações sobre o arquivo enviado
    $file_name = $file['name'];
    $file_type = $file['type'];
    $file_size = $file['size'];
    $file_tmp_name = $file['tmp_name'];
    $file_error = $file['error'];

    // Movendo o arquivo temporário para um local permanente no servidor
    $destination = 'uploads/' . $file_name;
    if(move_uploaded_file($file_tmp_name, $destination)) {
        echo "Arquivo enviado com sucesso!";

        // Aqui você pode fazer mais operações com o arquivo, se necessário
    } else {
        echo "Ocorreu um erro ao enviar o arquivo.";
    }
} else {
    echo "Nenhum arquivo foi enviado.";
}
?>
```

Neste exemplo, quando um arquivo é enviado através do formulário HTML, o script PHP (`upload.php`) verifica se um arquivo foi enviado corretamente usando `isset($_FILES['file_upload'])`. Em seguida, ele acessa as informações sobre o arquivo através da superglobal `$_FILES` e move o arquivo temporário para um diretório permanente no servidor usando `move_uploaded_file()`. O código também lida com erros que podem ocorrer durante o processo de envio.


## 3 Perguntas sobre FILES
1. Como você pode verificar se um arquivo foi enviado com sucesso através da superglobal `$_FILES` em PHP?
2. Quais são os principais elementos da superglobal `$_FILES` e o que eles representam?
3. Qual é a importância de validar os arquivos recebidos através da superglobal `$_FILES` em termos de segurança e integridade?

#### Respostas:
1. Para verificar se um arquivo foi enviado com sucesso através da superglobal `$_FILES` em PHP, você pode utilizar a função `isset()` para verificar se o índice correspondente ao nome do campo do arquivo está presente na superglobal `$_FILES`. Por exemplo:
```php
if(isset($_FILES['nome_do_campo'])) {
    // O arquivo foi enviado com sucesso
} else {
    // Nenhum arquivo foi enviado
}
```

2. Os principais elementos da superglobal `$_FILES` são:
   - `name`: O nome original do arquivo no computador do usuário.
   - `type`: O tipo MIME do arquivo enviado pelo usuário.
   - `size`: O tamanho do arquivo em bytes.
   - `tmp_name`: O nome temporário do arquivo durante o upload, armazenado no servidor.
   - `error`: Um código que indica se ocorreu algum erro durante o upload do arquivo.

3. Validar os arquivos recebidos através da superglobal `$_FILES` é fundamental para garantir a segurança e a integridade do sistema. Isso inclui verificar o tipo MIME do arquivo, o tamanho máximo permitido, além de realizar outras verificações de segurança, como verificar se o arquivo é realmente o tipo esperado e não um arquivo malicioso disfarçado com uma extensão falsa. A validação adequada dos arquivos ajuda a prevenir vulnerabilidades, como ataques de injeção de código ou o upload de arquivos maliciosos para o servidor.








