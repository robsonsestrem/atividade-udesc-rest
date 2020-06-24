## Objetivo
Criar uma aplicação web que implemente um CRUD de veículos com atributos como Montadora, Modelo, Cor, Quilometragem, Motor e Tipo.
A aplicação é apenas uma API REST utilizando JPA como persistência de dados e 
que atenda as operações de pesquisa, inserção, edição e exclusão.
A instituição adaptou o projeto dado como desafio da empresa VivaDecora para avaliar a contratação de
desenvolvedores backend (disponível em https://github.com/vivadecora/backend-teste).

### Testes com URL's da API
#### GET <br>
Acesso de teste sem comunicação com banco de dados:<br>
http://localhost:8080/atividade-udesc-rest/webresources/vehicle/teste

Busca por Id:<br>
http://localhost:8080/atividade-udesc-rest/webresources/vehicle/getId/1

Filtrado por três atributos(tipo, montadora e km):<br>
http://localhost:8080/atividade-udesc-rest/webresources/vehicle/filtros/carro/ford/1000

#### POST <br>
Inserção de dados: <br>
http://localhost:8080/atividade-udesc-rest/webresources/vehicle/add 
<br>
    {
        "montadora": "FORD",
        "modelo": "KA",
        "cor": "BRANCO",
        "km": 1000,
        "motor": "1.4",
        "tipo": "CARRO"
    }

#### PUT <br>
Alteração de dados: <br>
http://localhost:8080/atividade-udesc-rest/webresources/vehicle/edit
<br>
    {
        "id":"1",
        "montadora": "FORD",
        "modelo": "KA",
        "cor": "PRETO",        
        "km": 1000,
        "motor": "1.4",
        "tipo": "CARRO"
    }

#### DELETE <br>
Exclusão de dados por Id: <br>
http://localhost:8080/atividade-udesc-rest/webresources/vehicle/delete/1
