<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prova JS</title>
</head>

<body>

</body>
<script>
    var demanda = 1;
    alert("Bem-vindo!");
    
    var prod = parseInt(prompt("Qual o saldo de peças no estoque?"));
    var soma = prod;

    while (demanda != 0) {
        var escolha = parseInt(prompt("Quer adicionar ao estoque(1) ou vender peças(2)? "));

        if (escolha == 1) {
            soma = soma + parseInt(prompt("Com quantas peças quer abastecer o estoque?"));
            alert("Saldo atual: " + soma);
            var continuar = parseInt(prompt("Gostaria de continuar as modificações(1) ou não(2)?"))

            if (continuar == 2) {
                demanda = 0
            }

        }
        else if (escolha == 2) {
            venda = parseInt(prompt("Quantas peças deseja vender?"));
            if (venda <= soma) {
                soma = soma - venda;
                alert("Saldo atual: " + soma);
                var continuar = parseInt(prompt("Gostaria de continuar as modificações(1) ou não(2)?"))

                if (continuar == 2) {
                    demanda = 0
                }
            }

            else {
                alert("Saldo insuficiente!");
                var continuar = parseInt(prompt("Gostaria de continuar as modificações(1) ou não(2)?"))

                if (continuar == 2) {
                    demanda = 0
                }
            }
        }
        else {
            demanda = 0
        }
    } 
    alert("Processo finalizado!")
</script>

</html>
