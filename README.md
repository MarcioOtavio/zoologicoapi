# Zoologico API
API construída como projeto final do bootcamp Santander Dio Java Back end 2024

![Default_Gostaria_de_criar_uma_imagem_ilustrativa_para_uma_API_0](https://github.com/user-attachments/assets/c206a0f2-31f0-4911-aa48-e23d2c78e768)

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
