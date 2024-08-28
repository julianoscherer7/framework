# Documentação do Programa de Gerenciamento de Biblioteca

## 1. Visão Geral
Esse programa foi feito para gerenciar uma biblioteca simples. Dá pra cadastrar livros e usuários, ver a lista de livros e de usuários, e tem uma interface gráfica feita com Tkinter.

## 2. Classes do Programa

### ItemBiblioteca
- **Descrição:** É a classe base. Todos os itens na biblioteca, tipo livros e usuários, vão herdar dessa classe.
- **Atributo:** 
  - titulo: O nome do item (tipo o nome do livro ou do usuário).

### Livro
- **Descrição:** Herda de ItemBiblioteca. É a classe que representa os livros na biblioteca.
- **Atributos:**
  - titulo: Título do livro.
  - autor: Quem escreveu o livro.
  - isbn: O número ISBN do livro.

### Usuario
- **Descrição:** Herda de ItemBiblioteca. Representa os usuários que podem pegar livros.
- **Atributos:**
  - titulo: Nome do usuário.
  - matricula: Número de matrícula do usuário.

### Biblioteca
- **Descrição:** Essa classe guarda as listas de livros e usuários.
- **Atributos:**
  - livros: Lista de livros cadastrados.
  - usuarios: Lista de usuários cadastrados.
- **Métodos:**
  - adicionar_livro(livro): Adiciona um livro na lista de livros.
  - adicionar_usuario(usuario): Adiciona um usuário na lista de usuários.

### GerenciadorDePedidos
- **Descrição:** Essa classe cuida de quando um usuário quer pegar um livro emprestado.
- **Atributos:**
  - biblioteca: Instância da biblioteca usada no gerenciamento.
  - pedidos: Lista dos pedidos de livros.
- **Métodos:**
  - solicitar_livro(usuario, livro): Adiciona um pedido se o livro estiver disponível.

### BibliotecaApp
- **Descrição:** Essa é a interface gráfica do programa, feita com Tkinter.
- **Atributos:**
  - root: A janela principal do Tkinter.
  - biblioteca: Instância da classe Biblioteca.
  - main_frame: A tela principal com os botões de navegação.
  - `cadastro_livro_button, cadastro_usuario_button, visualizar_livros_button, visualizar_usuarios_button: Botões para navegar entre as telas.
- **Métodos:**
  - __init__(root): Inicializa a interface e cria os botões.
  - cadastro_livro(): Abre a tela de cadastro de livros.
  - cadastro_usuario(): Abre a tela de cadastro de usuários.
  - visualizar_livros(): Mostra a lista de livros cadastrados.
  - visualizar_usuarios(): Mostra a lista de usuários cadastrados.
  - voltar(frame): Volta para a tela principal.

## 3. Funcionalidades

- **Cadastrar Livro:** Abre uma tela onde você pode colocar o título, autor e ISBN para cadastrar um novo livro.
- **Cadastrar Usuário:** Abre uma tela onde você pode cadastrar um novo usuário com nome e matrícula.
- **Visualizar Livros:** Mostra uma lista de todos os livros cadastrados.
- **Visualizar Usuários:** Mostra uma lista de todos os usuários cadastrados.
- **Navegação:** Você pode navegar entre as telas com os botões e voltar para a tela principal.

## 4. Como o Programa Funciona

1. **Inicialização:** Quando você abre o programa, ele cria a janela principal com os botões.
2. **Cadastro de Livros/Usuários:** Clicando nos botões, você pode cadastrar novos livros ou usuários.
3. **Visualização:** Dá pra ver as listas de livros e usuários cadastrados.
4. **Voltar:** Tem um botão de "Voltar" em todas as telas para voltar para a tela principal.

## 5. Como Instalar e Usar

### Dependências:
- Você precisa do `tkinter`, mas ele já vem com o Python na maioria das vezes.

### Instalação:
- Se por acaso precisar instalar tkinter, use:
  ```bash
  sudo apt-get install python3-tk
