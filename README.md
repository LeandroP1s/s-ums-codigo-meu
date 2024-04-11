<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Landing Page - Venda de Livro</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            text-align: center;
            color: #333;
        }
        p {
            text-align: justify;
        }
        .book-cover {
            display: block;
            margin: 20px auto;
            max-width: 200px;
            height: auto;
        }
        .testimonial {
            margin-top: 30px;
            padding: 20px;
            background-color: #f9f9f9;
            border-left: 4px solid #007bff;
            border-radius: 5px;
        }
        .testimonial p {
            font-style: italic;
            color: #555;
        }
        form {
            margin-top: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
        }
        input[type="text"], input[type="email"], input[type="number"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
            box-sizing: border-box;
        }
        input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 3px;
            cursor: pointer;
            box-sizing: border-box;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Seja bem-vindo à nossa página de venda do livro!</h1>
        <img class="book-cover" src="book_cover.jpg" alt="Capa do Livro">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non neque ut libero iaculis facilisis. Cras ac nisl nec leo interdum egestas. Nulla facilisi. Nullam id erat vel justo dapibus semper vel non ex. Sed sed tincidunt magna. Integer volutpat laoreet sapien eget congue. Donec dapibus, felis a rhoncus tincidunt, velit justo bibendum urna, ac vulputate justo mi eget felis.</p>
        <h2>Informações do Livro</h2>
        <p><strong>Título:</strong> Título do Livro</p>
        <p><strong>Autor:</strong> Nome do Autor</p>
        <p><strong>Gênero:</strong> Gênero Literário</p>
        <h2>Descrição do Autor</h2>
        <p>Biografia do autor Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non neque ut libero iaculis facilisis.</p>
        <h2>Depoimentos de Leitores</h2>
        <div class="testimonial">
            <p>"Este livro mudou a minha vida! Recomendo a todos."</p>
            <p>- Nome do Leitor</p>
        </div>
        <div class="testimonial">
            <p>"Uma leitura envolvente e emocionante. Não consegui largar o livro até terminar!"</p>
            <p>- Nome do Leitor</p>
        </div>
        <form id="purchaseForm" onsubmit="return validateForm()">
            <h2>Registro de Compra</h2>
            <label for="buyerName">Nome do Comprador:</label>
            <input type="text" id="buyerName" name="buyerName" required>
            <label for="buyerEmail">Email do Comprador:</label>
            <input type="email" id="buyerEmail" name="buyerEmail" required>
            <label for="quantity">Quantidade de Livros:</label>
            <input type="number" id="quantity" name="quantity" min="1" required>
            <input type="submit" value="Registrar Compra">
        </form>
        <hr>
        <form id="entryForm" onsubmit="return validateForm()">
            <h2>Registro de Livro Entrado</h2>
            <label for="bookTitle">Título do Livro:</label>
            <input type="text" id="bookTitle" name="bookTitle" required>
            <label for="isbn">ISBN:</label>
            <input type="text" id="isbn" name="isbn" required>
            <label for="author">Autor:</label>
            <input type="text" id="author" name="author" required>
            <input type="submit" value="Registrar Livro">
        </form>
    </div>

    <script>
        function validateForm() {
            var forms = document.getElementsByTagName('form');
            for (var i = 0; i < forms.length; i++) {
                var form = forms[i];
                for (var j = 0; j < form.elements.length; j++) {
                    var element = form.elements[j];
                    if (element.hasAttribute('required') && element.value.trim() === '') {
                        alert('Por favor, preencha todos os campos obrigatórios.');
                        return false;
                    }
                }
            }
            return true;
        }
    </script>
</body>
</html>
