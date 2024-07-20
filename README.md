# JM-octo-waffle
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Sonhador small que se torna um Tall</title>
    <style>
        body {
            background-color: green;
            color: white;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .container {
            border: 5px solid red;
            padding: 20px;
            margin: 50px;
        }
        a {
            color: white;
            text-decoration: none;
            font-size: 20px;
            display: inline-block;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>O Sonhador small que se torna um Tall</h1>
        <a href="formulario.html" target="_blank">Clique aqui para preencher o formulário</a>
    </div>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Cadastro</title>
    <style>
        body {
            background-color: green;
            color: white;
            font-family: Arial, sans-serif;
        }
        .form-container {
            width: 80%;
            max-width: 500px;
            margin: auto;
            padding: 20px;
            border: 5px solid red;
            margin-top: 50px;
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input, textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border-radius: 5px;
            border: none;
        }
        button {
            background-color: white;
            color: black;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Formulário de Cadastro</h2>
        <form id="cadastroForm">
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" required>

            <label for="apelido">Apelido:</label>
            <input type="text" id="apelido" name="apelido">

            <label for="numero">Número:</label>
            <input type="text" id="numero" name="numero">

            <label for="dataNascimento">Data de Nascimento:</label>
            <input type="date" id="dataNascimento" name="dataNascimento" required>

            <label for="bi">Bilhete de Identidade:</label>
            <input type="text" id="bi" name="bi">

            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" required>

            <label for="nuit">NUIT:</label>
            <input type="text" id="nuit" name="nuit" maxlength="17">

            <label for="assunto">Assunto:</label>
            <input type="text" id="assunto" name="assunto">

            <label for="mensagem">Mensagem:</label>
            <textarea id="mensagem" name="mensagem" rows="4"></textarea>

            <button type="button" onclick="submeterFormulario()">Submeter</button>
        </form>
    </div>

    <script>
        function submeterFormulario() {
            // Coleta os dados do formulário
            const nome = document.getElementById("nome").value;
            const apelido = document.getElementById("apelido").value;
            const numero = document.getElementById("numero").value;
            const dataNascimento = document.getElementById("dataNascimento").value;
            const bi = document.getElementById("bi").value;
            const email = document.getElementById("email").value;
            const nuit = document.getElementById("nuit").value;
            const assunto = document.getElementById("assunto").value;
            const mensagem = document.getElementById("mensagem").value;

            // Exibe os dados no console (ou pode ser modificado para exibir em uma nova página)
            const dados = `
                Nome: ${nome}
                Apelido: ${apelido}
                Número: ${numero}
                Data de Nascimento: ${dataNascimento}
                Bilhete de Identidade: ${bi}
                E-mail: ${email}
                NUIT: ${nuit}
                Assunto: ${assunto}
                Mensagem: ${mensagem}
            `;

            alert("Dados confirmados:\n" + dados);

            // Calcula a idade a partir da data de nascimento
            const nascimento = new Date(dataNascimento);
            const hoje = new Date();
            const idade = hoje.getFullYear() - nascimento.getFullYear();
            const m = hoje.getMonth() - nascimento.getMonth();
            if (m < 0 || (m === 0 && hoje.getDate() < nascimento.getDate())) {
                idade--;
            }

            // Abre uma nova janela com base na idade
            if (idade >= 18) {
                window.open('candidato.html', '_blank');
            } else {
                window.open('recusado.html', '_blank');
            }
        }
    </script>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Candidato</title>
    <style>
        body {
            background-color: green;
            color: white;
            text-align: center;
            padding: 50px;
        }
        .container {
            border: 5px solid red;
            padding: 20px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bem-vindo, Candidato!</h1>
        <p>Você foi aceito como candidato.</p>
    </div>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recusado</title>
    <style>
        body {
            background-color: green;
            color: white;
            text-align: center;
            padding: 50px;
        }
        .container {
            border: 5px solid red;
            padding: 20px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Desculpe, Recusado!</h1>
        <p>Você não tem idade suficiente para ser candidato.</p>
    </div>
</body>
</html><!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Sonhador small que se torna um Tall</title>
    <style>
        body {
            background-color: green;
            color: white;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .container {
            border: 5px solid red;
            padding: 20px;
            margin: 50px;
        }
        a {
            color: white;
            text-decoration: none;
            font-size: 20px;
            display: inline-block;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>O Sonhador small que se torna um Tall</h1>
        <a href="formulario.html" target="_blank">Clique aqui para preencher o formulário</a>
    </div>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Cadastro</title>
    <style>
        body {
            background-color: green;
            color: white;
            font-family: Arial, sans-serif;
        }
        .form-container {
            width: 80%;
            max-width: 500px;
            margin: auto;
            padding: 20px;
            border: 5px solid red;
            margin-top: 50px;
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input, textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border-radius: 5px;
            border: none;
        }
        button {
            background-color: white;
            color: black;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Formulário de Cadastro</h2>
        <form id="cadastroForm">
            <label for="nome">Nome:</label>
            <input type="text" id="nome" name="nome" required>

            <label for="apelido">Apelido:</label>
            <input type="text" id="apelido" name="apelido">

            <label for="numero">Número:</label>
            <input type="text" id="numero" name="numero">

            <label for="dataNascimento">Data de Nascimento:</label>
            <input type="date" id="dataNascimento" name="dataNascimento" required>

            <label for="bi">Bilhete de Identidade:</label>
            <input type="text" id="bi" name="bi">

            <label for="email">E-mail:</label>
            <input type="email" id="email" name="email" required>

            <label for="nuit">NUIT:</label>
            <input type="text" id="nuit" name="nuit" maxlength="17">

            <label for="assunto">Assunto:</label>
            <input type="text" id="assunto" name="assunto">

            <label for="mensagem">Mensagem:</label>
            <textarea id="mensagem" name="mensagem" rows="4"></textarea>

            <button type="button" onclick="submeterFormulario()">Submeter</button>
        </form>
    </div>

    <script>
        function submeterFormulario() {
            // Coleta os dados do formulário
            const nome = document.getElementById("nome").value;
            const apelido = document.getElementById("apelido").value;
            const numero = document.getElementById("numero").value;
            const dataNascimento = document.getElementById("dataNascimento").value;
            const bi = document.getElementById("bi").value;
            const email = document.getElementById("email").value;
            const nuit = document.getElementById("nuit").value;
            const assunto = document.getElementById("assunto").value;
            const mensagem = document.getElementById("mensagem").value;

            // Exibe os dados no console (ou pode ser modificado para exibir em uma nova página)
            const dados = `
                Nome: ${nome}
                Apelido: ${apelido}
                Número: ${numero}
                Data de Nascimento: ${dataNascimento}
                Bilhete de Identidade: ${bi}
                E-mail: ${email}
                NUIT: ${nuit}
                Assunto: ${assunto}
                Mensagem: ${mensagem}
            `;

            alert("Dados confirmados:\n" + dados);

            // Calcula a idade a partir da data de nascimento
            const nascimento = new Date(dataNascimento);
            const hoje = new Date();
            const idade = hoje.getFullYear() - nascimento.getFullYear();
            const m = hoje.getMonth() - nascimento.getMonth();
            if (m < 0 || (m === 0 && hoje.getDate() < nascimento.getDate())) {
                idade--;
            }

            // Abre uma nova janela com base na idade
            if (idade >= 18) {
                window.open('candidato.html', '_blank');
            } else {
                window.open('recusado.html', '_blank');
            }
        }
    </script>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Candidato</title>
    <style>
        body {
            background-color: green;
            color: white;
            text-align: center;
            padding: 50px;
        }
        .container {
            border: 5px solid red;
            padding: 20px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bem-vindo, Candidato!</h1>
        <p>Você foi aceito como candidato.</p>
    </div>
</body>
</html>



<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recusado</title>
    <style>
        body {
            background-color: green;
            color: white;
            text-align: center;
            padding: 50px;
        }
        .container {
            border: 5px solid re
