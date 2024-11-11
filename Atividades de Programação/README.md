## Sistema de Pets

### Descrição

Criar um sistema simples para uma clínica veterinária que gerencie pets e seus donos.

### Exemplo de Diagrama


![[https://raw.githubusercontent.com/informaticaseed/LTP32024/refs/heads/main/Atividades%20de%20Programa%C3%A7%C3%A3o/Pet.png]]

Exemplo de Implementação em Java

```java
// Classe Pet
public class Pet {
    private String nome;
    private String especie;
    private int idade;
    private double peso;
    
    public Pet(String nome, String especie, int idade, double peso) {
        this.nome = nome;
        this.especie = especie;
        this.idade = idade;
        this.peso = peso;
    }
    
    public void atualizarPeso(double novoPeso) {
        this.peso = novoPeso;
    }
    
    public int getIdade() {
        return idade;
    }
}

// Classe Dono
public class Dono {
    private String nome;
    private String cpf;
    private String telefone;
    private List<Pet> pets;
    
    public Dono(String nome, String cpf, String telefone) {
        this.nome = nome;
        this.cpf = cpf;
        this.telefone = telefone;
        this.pets = new ArrayList<>();
    }
    
    public void cadastrarPet(Pet pet) {
        pets.add(pet);
    }
    
    public List<Pet> listarPets() {
        return pets;
    }
}

```


Atividade 2: Sistema de E-commerce

### Descrição

Desenvolver um sistema básico de e-commerce com produtos, carrinho e pedidos.

![[https://github.com/informaticaseed/LTP32024/blob/main/Atividades%20de%20Programa%C3%A7%C3%A3o/Ecomerce.png?raw=true]]

Exemplo de Implementação

```java
public class Produto {
    private String nome;
    private double preco;
    private int estoque;
    
    public Produto(String nome, double preco, int estoque) {
        this.nome = nome;
        this.preco = preco;
        this.estoque = estoque;
    }
    
    public void atualizarEstoque(int quantidade) {
        this.estoque += quantidade;
    }
    
    public double getPreco() {
        return preco;
    }
}

public class Carrinho {
    private List<ItemCarrinho> itens;
    private double total;
    
    public Carrinho() {
        this.itens = new ArrayList<>();
        this.total = 0.0;
    }
    
    public void adicionarItem(Produto produto, int quantidade) {
        itens.add(new ItemCarrinho(produto, quantidade));
        calcularTotal();
    }
    
    public double calcularTotal() {
        total = 0;
        for(ItemCarrinho item : itens) {
            total += item.getSubTotal();
        }
        return total;
    }
}
```

## Atividade 3: Sistema Bancário

### ### Descrição

Implementar um sistema bancário básico com diferentes tipos de contas e transações.

![[https://github.com/informaticaseed/LTP32024/blob/main/Atividades%20de%20Programa%C3%A7%C3%A3o/Banc%C3%A1rio.png?raw=true]]

Atividades

1. **Semana 1**:
    - Revisar os conceitos básicos de POO usando o Anki
    - Implementar o Sistema de Pets (mais simples)
    - Exercício: Adicionar funcionalidades como vacinas e histórico médico
2. **Semana 2**:
    - Trabalhar com o Sistema de E-commerce
    - Exercício: Adicionar sistema de desconto e cupons
3. **Semana 3**:
    - Desenvolver o Sistema Bancário
    - Exercício: Implementar transferências entre contas

## Exercícios Adicionais Propostos

1. **Sistema de Biblioteca**
    - Gerenciar livros, empréstimos e usuários
    - Aplicar multas por atraso
    - Reservar livros
2. **Sistema de Academia**
    - Cadastro de alunos e professores
    - Controle de presença
    - Avaliações físicas
3. **Sistema de Escola**
    - Gerenciar alunos, professores e turmas
    - Controle de notas e frequência
    - Boletins e histórico escolar

## Dicas para os Alunos

1. Sempre começar pelo diagrama de classes
2. Implementar primeiro as classes básicas e depois adicionar funcionalidades
3. Testar cada classe separadamente
4. Usar os exemplos como referência, mas não copiar exatamente
5. Documentar o código usando comentários
6. Utilizar os princípios de POO:
    - Encapsulamento
    - Herança
    - Polimorfismo
    - Abstração

## Critérios de Avaliação Sugeridos

1. Diagrama de Classes (30%)
2. Implementação do Código (40%)
3. Funcionalidades Extras (20%)
4. Documentação (10%)