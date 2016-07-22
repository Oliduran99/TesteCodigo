# TesteCodigo
Codigo
<!DOCTYPE html>
<html ng-app="Teste">
<head>
    <meta charset="UTF-8">
    <title>Teste Programa</title>
    <link rel="stylesheet" type="text/css" href="Models/bootstrap.css">
   
    <style>
        .jumbotron {
            width: 600px;
            text-align: center;
            margin-left: auto;
            margin-right: auto;
            margin-top: 20px;
        }

        .table {
            margin-top: 20px;
            text-align: left;
        }

        .form-control {
            margin-bottom: 5px;
        }

        .selecionado {
            background-color: dodgerblue;
        }

        .negrito {
            font-weight: bold;
        }
    </style>
    <script src="Angular/angular.js"></script>
    <script>
            angular.module("Teste",[]);
            angular.module("Teste").controller("Testecontrol",function ($scope) {
                $scope.app =" Sistema de Recados ";

            });
    </script>
</head>
<body ng-controller="Testecontrol">
    <div class="jumbotron">
        <h3>{{app}}</h3>
        <table class="table table-striped">
            <tr></tr>
        </table>
        <input class="form-control" type="text" ng-model="usuario.cpf" placeholder="CPF" />
        <input class="form-control" type="text" ng-model="usuario.mail" placeholder="E-mail" />
        <input class="form-control" type="password" ng-model="usuario.senha" placeholder="Senha">
        <form method="get" action="Page2.html">
            <input class="btn bg-primary" type="submit" value="Deixar seu Recado" ng-disabled="!usuario.mail || !usuario.senha">
        </form>
        <br />
        <Form method="get" action="Angular/ValudaCpf.php">
            <input class="btn bg-danger" type="submit" value="Valida CPF" ng-disabled="!usuario.cpf">
        </Form>

        <a href="Registos.html">Voltar</a>
    </div>
        

</body>
</html>

