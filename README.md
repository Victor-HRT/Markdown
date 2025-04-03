# Victor Hugo

## Doctype

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial e Número Primo</title>
</head>
<body>

```
## Calculadora de Fatorial e Verificador de Número Primo
    
```html
    <!-- Campo de entrada para o usuário inserir um número -->
    <label for="numero">Digite um número:</label>
    <input type="number" id="numero">
    <button onclick="calcular()">Calcular</button>
    
    <!-- Parágrafo onde o resultado será exibido -->
    <p id="resultado"></p
```

## Função para calcular o fatorial de um número

```html
        <script>
        function calcularFatorial(n) {
            if (n === 0) {
                return 1; // O fatorial de 0 é sempre 1
            } else {
                return n * calcularFatorial(n - 1); // Recursão para calcular o fatorial
            }
        }
```

## Função para verificar se um número é primo

```h
        function verificarNumeroPrimo(numero) {
            if (numero <= 1) {
                return false; // Números menores ou iguais a 1 não são primos
            }
            for (let i = 2; i < numero; i++) {
                if (numero % i === 0) {
                    return false; // Se for divisível por algum número além de 1 e ele mesmo, não é primo
                }
            }
            return true; // Se não for divisível por nenhum número, é primo
        }

```

## Função principal que calcula fatorial e verifica se é primo

```h
        function calcular() {
            let numero = parseInt(document.getElementById("numero").value); // Obtém o valor inserido pelo usuário
            let fatorial = calcularFatorial(numero); // Calcula o fatorial
            let primo = verificarNumeroPrimo(numero); // Verifica se é primo

            // Exibe os resultados na página
            document.getElementById("resultado").innerHTML =  
                "O fatorial de " + numero + " é " + fatorial + "<br>" +
                "O número " + numero + (primo ? " é primo." : " não é primo.");
        }
    </script>
</body>
</html>
```

## Respostas
1. A indentação foi corrigida para melhor leitura e foram adicionados comentários explicando a função de cada trecho do código.
2. Permite que outros desenvolvedores compreendam rapidamente a lógica do código.
3. Uso de comentários explicativos em trechos essenciais, manutenção de uma boa indentação e estrutura organizacional.
4. Markdown permite criar documentação estruturada e legível, além do código ser facilmente visualizado em repositórios como GitHub.
5. Garantem que múltiplos desenvolvedores possam trabalhar no mesmo projeto de forma eficiente e reduzem o risco de introdução de erros e inconsistências no código.
