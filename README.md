# Zoologico API
API construída como projeto final do bootcamp Santander Dio Java Back end 2024

![Default_Gostaria_de_criar_uma_imagem_ilustrativa_para_uma_API_0](https://github.com/user-attachments/assets/c206a0f2-31f0-4911-aa48-e23d2c78e768)

🌿🦁📊 A API de Zoológico: Gerenciamento Eficiente e Divertido! 🚀🐾

A API de Zoológico é projetada para fornecer um sistema de gerenciamento eficiente para um zoológico fictício, permitindo a gestão de 🐒🐘🐧 animais deste zoológico fictício. Através desta API, é possível realizar operações de CRUD (Create, Read, Update, Delete) para manipular informações essenciais do zoológico. 🛠️💬

Recursos Principais 📋
1. Animais

O recurso de animais permite adicionar, atualizar, listar e remover informações sobre os animais residentes no zoológico. Cada animal é representado por um conjunto de atributos, incluindo nome, espécie e habitat. 🐾🌳

Exemplo de uso:

GET /api/animais: Retorna a lista de todos os animais no zoológico.
POST /api/animais: Adiciona um novo animal ao zoológico.
PUT /api/animais/{id}: Atualiza os detalhes de um animal específico.
DELETE /api/animais/{id}: Remove um animal do zoológico.

Pretendo realizar atualizações em breve do sistema, adicionando dois novos recursos: 

2. Visitantes
O recurso de visitantes permite o gerenciamento das pessoas que visitam o zoológico. Cada visitante é identificado por um nome e idade, e pode ser associado a eventos especiais ou promoções do zoológico. 🎟️👨‍👩‍👧‍👦

3. Funcionários
O recurso de funcionários permite o gerenciamento dos colaboradores que trabalham no zoológico. Cada funcionário possui um nome e cargo, e pode ser atribuído a diferentes áreas de responsabilidade dentro do zoológico. 🧑‍💻🔧

Estrutura da API 🏗️
A API de Zoológico é construída com base nos princípios RESTful, utilizando endpoints intuitivos e seguros para realizar operações sobre os recursos mencionados. 🔐🌐

## Diagrama de classes

``` mermaid

classDiagram
    class Zoo {
        -Long id
        -String nome
        -String localizacao
        +List<Animal> animais
        +void adicionarAnimal(Animal animal)
        +void removerAnimal(Animal animal)
        +List<Animal> listarAnimais()
    }
    class Animal {
        -Long id
        -String nome
        -String especie
        -String habitat
        +Long getId()
        +void setId(Long id)
        +String getNome()
        +void setNome(String nome)
        +String getEspecie()
        +void setEspecie(String especie)
        +String getHabitat()
        +void setHabitat(String habitat)
    }
    class Visitante {
        -Long id
        -String nome
        -int idade
        +Long getId()
        +void setId(Long id)
        +String getNome()
        +void setNome(String nome)
        +int getIdade()
        +void setIdade(int idade)
    }
    class Funcionario {
        -Long id
        -String nome
        -String cargo
        +Long getId()
        +void setId(Long id)
        +String getNome()
        +void setNome(String nome)
        +String getCargo()
        +void setCargo(String cargo)
    }
    Zoo -- Animal : possui
    Zoo "1" -- "0..*" Visitante : recebe
    Zoo "1" -- "0..*" Funcionario : emprega
```
