<!DOCTYPE html>
<html>
<head>
    <title>Página Protegida</title>
    <style>
        body {
            text-align: center;
        }
        #content {
            display: none;
        }
    </style>
</head>
<body>
    <h1>Bem-vindo à página protegida</h1>
    
    <div id="access-form">
        <label for="access-key">Insira a chave de acesso:</label>
        <input type="password" id="access-key" />
        <button id="access-button">Acessar</button>
    </div>
    
    <div id="content">
        <h2>O CURSO</h2>
        <p>Aqui está o Curso.</p>
    </div>
    
    <script>
        const accessKey = 'Cursorobuxinf'; // Substitua 'sua_chave_aqui' pela chave desejada
        const accessButton = document.getElementById('access-button');
        const accessForm = document.getElementById('access-form');
        const content = document.getElementById('content');
        
        accessButton.addEventListener('click', function() {
            const enteredKey = document.getElementById('access-key').value;
            if (enteredKey === accessKey) {
                accessForm.style.display = 'none';
                content.style.display = 'block';
            } else {
                alert('Chave incorreta. Tente novamente.');
            }
        });
    </script>
</body>
</html>
