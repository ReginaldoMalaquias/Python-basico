
# Conhecimentos Básicos de Python

Este repositório contém informações essenciais para quem está começando a aprender Python. Navegue pelas seções abaixo para explorar diferentes tópicos.

## Índice

- [Introdução](#introdução)
- [Variáveis](#variáveis)
- [Tipos de Dados](#tipos-de-dados)
- [Operadores](#operadores)
- [Controle de Fluxo](#controle-de-fluxo)
- [Funções](#funções)
- [Módulos](#módulos)
- [Manipulação de Arquivos](#manipulação-de-arquivos)
- [Tratamento de Erros](#tratamento-de-erros)
- [Projetos Práticos](#projetos-práticos)

## Introdução
Uma visão geral sobre Python e suas aplicações.

## Variáveis
Como declarar e usar variáveis em Python.
1.  Enviar código para o repositório do GitHub
```
git push -u origin main 
```

## Tipos de Dados   
[⬆](https://github.com/ReginaldoMalaquias/Python-basico/blob/main/README.md#%C3%ADndice)
Tipos de Dados Principais em Python:

Tipos Numéricos:
int (inteiro): Representa números inteiros, tanto positivos quanto negativos, sem casas decimais.  
A precisão é arbitrária, o que significa que podem ser tão grandes quanto a memória do seu computador permitir.

```
idade = 30
saldo = -100
ano = 2025
numero_gigante = 99999999999999999999999999999999999999
```


Inteiro (int): Representa números inteiros, positivos ou negativos, sem casas decimais, de tamanho ilimitado.
Exemplo: idade = 30, quantidade = -5, ano = 2025

Ponto Flutuante (float): Representa números reais, ou seja, números com casas decimais.
Exemplo: preco = 19.99, altura = 1.75, pi = 3.14159

Complexo (complex): Representa números complexos, que possuem uma parte real e uma parte imaginária (geralmente indicada com j).
Exemplo: z = 2 + 3j, numero_complexo = -1j

Tipo Booleano (bool):
Representa um de dois valores: True (verdadeiro) ou False (falso). Eles são frequentemente o resultado de operações de comparação ou lógicas.
Exemplo: ativo = True, maior_de_idade = (idade >= 18)
Tipos de Sequência: São coleções ordenadas de itens.

String (str): Usada para representar dados textuais. É uma sequência imutável de caracteres Unicode. Strings podem ser definidas usando aspas simples ('...'), duplas ("...") ou triplas ('''...''' ou """...""" para múltiplas linhas).
Exemplo: nome = "Maria", mensagem = 'Olá, mundo!', texto_longo = """Esta é uma string que ocupa várias linhas."""

Lista (list): Uma coleção ordenada e mutável de itens. Isso significa que você pode adicionar, remover ou alterar itens após a criação da lista. Itens em uma lista podem ser de tipos diferentes. São definidas por colchetes [].
Exemplo: numeros = [1, 2, 3, 4, 5], misturado = [1, "Python", 3.14, True]
Operações comuns: append(), insert(), remove(), pop(), sort().

Tupla (tuple): Uma coleção ordenada e imutável de itens. Uma vez criada, você não pode alterar seus elementos. São definidas por parênteses ().
Exemplo: coordenadas = (10, 20), cores_rgb = ("vermelho", "verde", "azul")
Geralmente usadas para coleções de itens que não devem ser modificados, como coordenadas ou registros fixos.

Tipo de Mapeamento:
Dicionário (dict): Uma coleção não ordenada (nas versões de Python anteriores à 3.7, a partir da 3.7 são ordenados por inserção) de pares chave-valor. Cada chave deve ser única e imutável (como strings, números ou tuplas), e é usada para acessar seu valor correspondente. Dicionários são mutáveis e definidos por chaves {}.
Exemplo: pessoa = {"nome": "Carlos", "idade": 42, "cidade": "Salvador"}, estoque = {"maca": 10, "banana": 25}
Acesso: pessoa["nome"] (retorna "Carlos")
Tipos de Conjunto (Set):

Conjunto (set): Uma coleção não ordenada de itens únicos e mutáveis. Não permite elementos duplicados. Útil para operações matemáticas de conjuntos como união, interseção, diferença, etc. Definidos por chaves {} ou pela função set(). Para criar um conjunto vazio, você deve usar set(), pois {} cria um dicionário vazio.
Exemplo: numeros_unicos = {1, 2, 3, 3, 4}, letras = set("abracadabra") (resultaria em {'a', 'b', 'r', 'c', 'd'})

Conjunto Congelado (frozenset): Similar ao set, mas é imutável. Uma vez criado, seus elementos não podem ser alterados. Pode ser usado como chave em um dicionário, pois é imutável. Criado com a função frozenset().
Exemplo: conjunto_fixo = frozenset([1, 2, 3])
Tipos Binários: Usados para manipular dados binários.

Bytes (bytes): Sequência imutável de bytes (números entre 0 e 255). Usado para dados binários brutos, como arquivos de imagem ou dados de rede.
Exemplo: dados_binarios = b'hello'

Bytearray (bytearray): Sequência mutável de bytes. Similar ao bytes, mas pode ser modificado após a criação.
Exemplo: dados_mutaveis = bytearray(b'world'), dados_mutaveis[0] = 119 (troca 'w' por 'W' se 'w' for 119 em ASCII)

Memoryview (memoryview): Fornece uma visão da memória de outros objetos binários sem copiar os dados. Permite acesso eficiente a dados em buffers de protocolo binário.

Tipo Nulo (NoneType):
None: Representa a ausência de valor ou um valor nulo. É o único valor do tipo NoneType. Frequentemente usado para indicar que uma variável ainda não tem um valor atribuído ou que uma função não retorna nada explicitamente.
Exemplo: resultado = None

Como Verificar o Tipo de um Dado:
Você pode usar a função embutida type() para descobrir o tipo de uma variável ou valor: 
Python

x = 10
print(type(x))  # Saída: <class 'int'>

nome = "Python"
print(type(nome))  # Saída: <class 'str'>

lista_exemplo = [1, 2]
print(type(lista_exemplo))  # Saída: <class 'list'>
Tipagem Dinâmica:

Python é uma linguagem de tipagem dinâmica. Isso significa que você não precisa declarar explicitamente o tipo de uma variável ao criá-la. O tipo da variável é determinado em tempo de execução com base no valor atribuído a ela. Uma mesma variável pode, inclusive, referenciar objetos de tipos diferentes em momentos diferentes (embora isso nem sempre seja uma boa prática).

Python

variavel = 100      # variavel é do tipo int
print(type(variavel))
variavel = "Agora sou uma string"  # variavel agora é do tipo str
print(type(variavel))
Entender os tipos de dados é fundamental para programar em Python, pois eles definem como os dados são armazenados e quais operações você pode realizar com eles.  
[⬆](https://github.com/ReginaldoMalaquias/Python-basico/blob/main/README.md#%C3%ADndice)  
## Operadores
Explicação dos operadores aritméticos, lógicos, de comparação, etc.

## Controle de Fluxo
Como usar estruturas de controle como `if`, `for`, `while`, etc.

## Funções
Definição e uso de funções em Python.

## Módulos
Como importar e usar módulos em Python.

## Manipulação de Arquivos
Leitura e escrita de arquivos em Python.

## Tratamento de Erros
Como tratar exceções e erros em Python.

## Projetos Práticos
Exemplos de projetos práticos para aplicar os conhecimentos adquiridos.
[⬆](https://github.com/ReginaldoMalaquias/Python-basico/blob/main/README.md#%C3%ADndice)

