# Exercícios Resolvidos - Python Básico

## Índice

* **[Introdução e Olá Mundo](#introdução-e-olá-mundo)**
* **[Variáveis e Operações](#variáveis-e-operações)**
* **[Listas, Tuplas, Dicionários](#listas-tuplas-dicionários)**
* **[Condicionais e Loops](#condicionais-e-loops)**
* **[Funções](#funções)**

## Introdução e Olá Mundo

* Exercício 1: Escreva um programa que mostre "Olá, mundo!" na tela.

```py
print("Olá, mundo!")  # Saída simples usando a função print()
```

---

## Variáveis e Operações

* Exercício 2: Peça ao usuário que digite o nome e mostre uma mensagem de boas-vindas.

```py
nome = input("Digite seu nome: ")
print(f"Bem-vindo(a), {nome}!")
```

* Exercício 3: Solicite dois números e exiba a soma.

```py
a = int(input("Digite o primeiro número: "))
b = int(input("Digite o segundo número: "))
print("A soma é:", a + b)
```

* Exercício 4: Calcule a média entre 4 notas.

```py
notas = []
for i in range(4):
    nota = float(input(f"Digite a nota {i+1}: "))
    notas.append(nota)
media = sum(notas) / len(notas)
print(f"Média final: {media:.2f}")
```

* Exercício 5: Converta Celsius para Fahrenheit.

```py
celsius = float(input("Informe a temperatura em Celsius: "))
fahrenheit = celsius * 9/5 + 32
print(f"{celsius}C é igual a {fahrenheit}F")
```

* Exercício 6: Verifique se um número é par ou ímpar.

```py
n = int(input("Digite um número: "))
if n % 2 == 0:
    print("O número é par.")
else:
    print("O número é ímpar.")
```

* Exercício 7: Calcule o produto de três números inteiros.

```py
num1 = int(input("Digite o primeiro número inteiro: "))
num2 = int(input("Digite o segundo número inteiro: "))
num3 = int(input("Digite o terceiro número inteiro: "))
produto = num1 * num2 * num3
print(f"O produto dos três números é: {produto}")
```

* Exercício 8: Peça ao usuário sua idade e imprima quantos anos faltam para ele se aposentar (considere 65 anos para aposentadoria).

```py
idade = int(input("Digite sua idade: "))
anos_para_aposentar = 65 - idade
if anos_para_aposentar > 0:
    print(f"Faltam {anos_para_aposentar} anos para você se aposentar.")
else:
    print("Você já pode se aposentar ou já se aposentou!")
```

* Exercício 9: Solicite o raio de um círculo e calcule sua área ($A = \pi r^2$). Use $\pi$ como 3.14.

```py
raio = float(input("Digite o raio do círculo: "))
pi = 3.14
area = pi * (raio ** 2)
print(f"A área do círculo é: {area:.2f}")
```

* Exercício 10: Receba um valor em reais e converta para dólares (considere 1 dólar = 5.00 reais).

```py
reais = float(input("Digite o valor em reais (R$): "))
cotacao_dolar = 5.00
dolares = reais / cotacao_dolar
print(f"R${reais:.2f} equivalem a US${dolares:.2f}")
```

* Exercício 11: Calcule o IMC (Índice de Massa Corporal) de uma pessoa. Peça peso (kg) e altura (m). ($IMC = \frac{peso}{altura^2}$)

```py
peso = float(input("Digite seu peso em kg: "))
altura = float(input("Digite sua altura em metros: "))
imc = peso / (altura ** 2)
print(f"Seu IMC é: {imc:.2f}")
```

* Exercício 12: Determine se um número é positivo, negativo ou zero.

```py
numero = int(input("Digite um número: "))
if numero > 0:
    print("O número é positivo.")
elif numero < 0:
    print("O número é negativo.")
else:
    print("O número é zero.")
```

* Exercício 13: Peça dois números e imprima o maior entre eles.

```py
num1 = float(input("Digite o primeiro número: "))
num2 = float(input("Digite o segundo número: "))
if num1 > num2:
    print(f"O maior número é: {num1}")
else:
    print(f"O maior número é: {num2}")
```

* Exercício 14: Peça ao usuário uma palavra e verifique se ela é um palíndromo (lê-se igual de trás para frente).

```py
palavra = input("Digite uma palavra para verificar se é um palíndromo: ")
palavra_formatada = palavra.lower().replace(" ", "")
if palavra_formatada == palavra_formatada[::-1]:
    print(f"'{palavra}' é um palíndromo.")
else:
    print(f"'{palavra}' não é um palíndromo.")
```

* Exercício 15: Peça a altura e largura de um retângulo e calcule sua área.

```py
altura = float(input("Digite a altura do retângulo: "))
largura = float(input("Digite a largura do retângulo: "))
area = altura * largura
print(f"A área do retângulo é: {area}")
```

* Exercício 16: Peça o nome completo do usuário e imprima apenas o primeiro nome.

```py
nome_completo = input("Digite seu nome completo: ")
primeiro_nome = nome_completo.split(" ")[0]
print(f"Seu primeiro nome é: {primeiro_nome}")
```

* Exercício 17: Calcule a porcentagem de um valor. Peça o valor total e a porcentagem.

```py
valor_total = float(input("Digite o valor total: "))
porcentagem = float(input("Digite a porcentagem a ser calculada (%): "))
valor_calculado = (porcentagem / 100) * valor_total
print(f"{porcentagem}% de R${valor_total:.2f} é R${valor_calculado:.2f}")
```

* Exercício 18: Dada uma string, imprima ela invertida.

```py
texto_original = input("Digite uma frase ou palavra: ")
texto_invertido = texto_original[::-1]
print(f"Texto invertido: {texto_invertido}")
```

* Exercício 19: Peça ao usuário para digitar uma frase e conte quantas vogais (a, e, i, o, u) ela contém.

```py
frase = input("Digite uma frase: ")
vogais = "aeiouAEIOU"
contador_vogais = 0
for caractere in frase:
    if caractere in vogais:
        contador_vogais += 1
print(f"A frase contém {contador_vogais} vogais.")
```

* Exercício 20: Solicite o nome de um produto e seu preço. Em seguida, calcule e imprima o preço com 10% de desconto.

```py
produto = input("Digite o nome do produto: ")
preco_original = float(input(f"Digite o preço de {produto}: "))
desconto = 0.10
preco_com_desconto = preco_original * (1 - desconto)
print(f"O preço de {produto} com 10% de desconto é R${preco_com_desconto:.2f}")
```

* Exercício 21: Peça ao usuário dois números inteiros e realize todas as quatro operações básicas (soma, subtração, multiplicação, divisão).

```py
num1 = int(input("Digite o primeiro número inteiro: "))
num2 = int(input("Digite o segundo número inteiro: "))

soma = num1 + num2
subtracao = num1 - num2
multiplicacao = num1 * num2

print(f"Soma: {soma}")
print(f"Subtração: {subtracao}")
print(f"Multiplicação: {multiplicacao}")

if num2 != 0:
    divisao = num1 / num2
    print(f"Divisão: {divisao:.2f}")
else:
    print("Não é possível dividir por zero.")
```

* Exercício 22: Peça ao usuário o tempo gasto em uma viagem (em horas) e a velocidade média (em km/h). Calcule a distância percorrida.

```py
tempo = float(input("Digite o tempo gasto na viagem (em horas): "))
velocidade = float(input("Digite a velocidade média (em km/h): "))
distancia = tempo * velocidade
print(f"A distância percorrida foi de {distancia:.2f} km.")
```

## Listas, Tuplas, Dicionários

* Exercício 23: Armazene 5 nomes em uma lista e imprima-os em ordem.

```py
nomes = []
for i in range(5):
    nomes.append(input("Digite um nome: "))
nomes.sort()
print("Nomes em ordem alfabética:", nomes)
```

* Exercício 24: Crie uma tupla com os dias da semana e mostre o último.

```py
dias = ("Segunda", "Terça", "Quarta", "Quinta", "Sexta", "Sábado", "Domingo")
print("O último dia é:", dias[-1])
```

* Exercício 25: Dicionário com nome e idade.

```py
pessoa = {"nome": "Ana", "idade": 25}
print(f"{pessoa['nome']} tem {pessoa['idade']} anos.")
```

* Exercício 26: Lista de números e soma dos pares.

```py
numeros = [1, 2, 3, 4, 5, 6]
soma_pares = sum(n for n in numeros if n % 2 == 0)
print("Soma dos pares:", soma_pares)
```

* Exercício 27: Crie uma lista com 5 números inteiros e calcule a soma de todos eles.

```py
lista_numeros = [10, 20, 30, 40, 50]
soma_total = sum(lista_numeros)
print(f"A soma de todos os números na lista é: {soma_total}")
```

* Exercício 28: Dada uma lista de frutas, adicione uma nova fruta e remova uma existente.

```py
frutas = ["maçã", "banana", "cereja", "damasco"]
print(f"Lista original: {frutas}")
frutas.append("manga")
print(f"Lista após adicionar 'manga': {frutas}")
frutas.remove("banana")
print(f"Lista após remover 'banana': {frutas}")
```

* Exercício 29: Crie uma tupla com as coordenadas (latitude, longitude) e acesse cada elemento.

```py
coordenadas = (-23.5505, -46.6333) # Exemplo: São Paulo
latitude = coordenadas[0]
longitude = coordenadas[1]
print(f"Latitude: {latitude}, Longitude: {longitude}")
```

* Exercício 30: Crie um dicionário para armazenar informações de um livro: título, autor e ano de publicação. Acesse e imprima cada informação.

```py
livro = {
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano_publicacao": 1899
}
print(f"Título: {livro['titulo']}")
print(f"Autor: {livro['autor']}")
print(f"Ano de Publicação: {livro['ano_publicacao']}")
```

* Exercício 31: Dada uma lista de números, encontre o maior e o menor valor.

```py
lista = [5, 12, 3, 8, 20, 1]
maior = max(lista)
menor = min(lista)
print(f"O maior número na lista é: {maior}")
print(f"O menor número na lista é: {menor}")
```

* Exercício 32: Crie uma lista com 3 cores e imprima cada cor em uma linha diferente usando um loop `for`.

```py
cores = ["vermelho", "azul", "verde"]
for cor in cores:
    print(cor)
```

* Exercício 33: Dada uma lista de palavras, conte quantas vezes uma palavra específica aparece.

```py
palavras = ["banana", "maçã", "banana", "laranja", "banana"]
palavra_procurada = "banana"
contagem = palavras.count(palavra_procurada)
print(f"A palavra '{palavra_procurada}' aparece {contagem} vezes.")
```

* Exercício 34: Crie um dicionário com nomes de alunos e suas respectivas notas. Adicione um novo aluno e atualize a nota de outro.

```py
notas_alunos = {
    "Alice": 8.5,
    "Bruno": 7.0,
    "Carla": 9.2
}
print(f"Notas iniciais: {notas_alunos}")
notas_alunos["Diego"] = 6.8  # Adiciona um novo aluno
notas_alunos["Bruno"] = 7.5  # Atualiza a nota de Bruno
print(f"Notas atualizadas: {notas_alunos}")
```

* Exercício 35: Combine duas listas em uma nova lista.

```py
lista1 = [1, 2, 3]
lista2 = [4, 5, 6]
lista_combinada = lista1 + lista2
print(f"Lista combinada: {lista_combinada}")
```

* Exercício 36: Dada uma tupla de números, calcule a média.

```py
numeros_tupla = (10, 20, 30, 40, 50)
media_tupla = sum(numeros_tupla) / len(numeros_tupla)
print(f"A média dos números na tupla é: {media_tupla:.2f}")
```

* Exercício 37: Crie uma lista com números duplicados e remova todas as duplicatas, mantendo apenas os valores únicos.

```py
lista_com_duplicatas = [1, 2, 2, 3, 4, 4, 5, 1]
lista_sem_duplicatas = list(set(lista_com_duplicatas))
print(f"Lista original: {lista_com_duplicatas}")
print(f"Lista sem duplicatas: {lista_sem_duplicatas}")
```

* Exercício 38: Crie um dicionário que mapeie nomes de países para suas capitais. Peça ao usuário para digitar um país e imprima sua capital.

```py
capitais = {
    "Brasil": "Brasília",
    "Argentina": "Buenos Aires",
    "Chile": "Santiago",
    "Canadá": "Ottawa",
    "Japão": "Tóquio"
}
pais = input("Digite o nome de um país para saber sua capital: ")
if pais in capitais:
    print(f"A capital de {pais} é {capitais[pais]}.")
else:
    print("País não encontrado no dicionário.")
```

* Exercício 39: Dada uma lista de strings, ordene-as em ordem alfabética.

```py
frutas_nao_ordenadas = ["banana", "maçã", "abacaxi", "uva", "laranja"]
frutas_nao_ordenadas.sort()
print(f"Frutas em ordem alfabética: {frutas_nao_ordenadas}")
```

* Exercício 40: Crie uma lista de números e remova o elemento na segunda posição.

```py
numeros_remocao = [10, 20, 30, 40, 50]
print(f"Lista original: {numeros_remocao}")
numeros_remocao.pop(1) # Remove o elemento no índice 1 (segunda posição)
print(f"Lista após remoção: {numeros_remocao}")
```

* Exercício 41: Crie um dicionário com 3 itens e depois limpe-o completamente.

```py
meu_dicionario = {"chave1": "valor1", "chave2": "valor2", "chave3": "valor3"}
print(f"Dicionário antes de limpar: {meu_dicionario}")
meu_dicionario.clear()
print(f"Dicionário depois de limpar: {meu_dicionario}")
```

* Exercício 42: Crie uma tupla aninhada (tupla de tuplas) representando coordenadas 2D. Acesse um elemento específico.

```py
pontos = ((1, 2), (3, 4), (5, 6))
print(f"O segundo ponto é: {pontos[1]}")
print(f"A coordenada y do terceiro ponto é: {pontos[2][1]}")
```

## Condicionais e Loops

* Exercício 43: Verificar maior de idade.

```py
idade = int(input("Qual sua idade? "))
if idade >= 18:
    print("Você é maior de idade.")
else:
    print("Você é menor de idade.")
```

* Exercício 44: Tabuada de um número

```py
n = int(input("Digite um número: "))
for i in range(1, 11):
    print(f"{n} x {i} = {n*i}")
```

* Exercício 45: Adivinhe o número

```py
import random
secreto = random.randint(1, 10)
chute = int(input("Adivinhe o número de 1 a 10: "))
if chute == secreto:
    print("Acertou!")
else:
    print(f"Errou! O certo era {secreto}.")
```

* Exercício 46: Contagem regressiva de 10 a 0

```py
for i in range(10, -1, -1):
    print(i)
```

* Exercício 47: Somar até digitar 0

```py
soma = 0
while True:
    n = int(input("Digite um número (0 para sair): "))
    if n == 0:
        break
    soma += n
print("Soma total:", soma)
```

* Exercício 48: Peça um número e imprima todos os números de 1 até ele.

```py
num_limite = int(input("Digite um número inteiro positivo: "))
for i in range(1, num_limite + 1):
    print(i)
```

* Exercício 49: Verifique se um número está entre 10 e 20 (inclusive).

```py
numero_verificar = int(input("Digite um número: "))
if 10 <= numero_verificar <= 20:
    print("O número está entre 10 e 20.")
else:
    print("O número não está entre 10 e 20.")
```

* Exercício 50: Imprima os números pares de 1 a 10.

```py
for i in range(2, 11, 2):
    print(i)
```

* Exercício 51: Peça a senha ao usuário até que ele digite "python123".

```py
senha_correta = "python123"
senha_digitada = ""
while senha_digitada != senha_correta:
    senha_digitada = input("Digite a senha: ")
    if senha_digitada != senha_correta:
        print("Senha incorreta. Tente novamente.")
print("Login bem-sucedido!")
```

* Exercício 52: Calcule a soma dos números de 1 a 100.

```py
soma_cem = 0
for i in range(1, 101):
    soma_cem += i
print(f"A soma dos números de 1 a 100 é: {soma_cem}")
```

* Exercício 53: Crie um programa que determine se um ano é bissexto. (Um ano é bissexto se for divisível por 4, exceto se for divisível por 100 mas não por 400).

```py
ano = int(input("Digite um ano: "))
if (ano % 4 == 0 and ano % 100 != 0) or (ano % 400 == 0):
    print(f"O ano {ano} é bissexto.")
else:
    print(f"O ano {ano} não é bissexto.")
```

* Exercício 54: Imprima os primeiros 5 múltiplos de 7.

```py
for i in range(1, 6):
    print(i * 7)
```

* Exercício 55: Peça uma letra e diga se é uma vogal ou uma consoante.

```py
letra = input("Digite uma letra: ").lower()
if letra in "aeiou":
    print("É uma vogal.")
elif 'a' <= letra <= 'z':
    print("É uma consoante.")
else:
    print("Não é uma letra do alfabeto.")
```

* Exercício 56: Crie um loop que continue pedindo números até que a soma deles ultrapasse 100.

```py
soma_acumulada = 0
while soma_acumulada <= 100:
    num = int(input(f"Soma atual: {soma_acumulada}. Digite um número para adicionar: "))
    soma_acumulada += num
print(f"A soma ultrapassou 100. Soma final: {soma_acumulada}")
```

* Exercício 57: Dada uma lista de números, imprima apenas os que são maiores que 10.

```py
lista_numeros = [5, 12, 8, 25, 3, 15, 7]
print("Números maiores que 10:")
for numero in lista_numeros:
    if numero > 10:
        print(numero)
```

* Exercício 58: Verifique se um triângulo é equilátero (todos os lados iguais), isósceles (dois lados iguais) ou escaleno (todos os lados diferentes). Peça os 3 lados.

```py
lado1 = float(input("Digite o comprimento do primeiro lado: "))
lado2 = float(input("Digite o comprimento do segundo lado: "))
lado3 = float(input("Digite o comprimento do terceiro lado: "))

if lado1 == lado2 == lado3:
    print("É um triângulo equilátero.")
elif lado1 == lado2 or lado1 == lado3 or lado2 == lado3:
    print("É um triângulo isósceles.")
else:
    print("É um triângulo escaleno.")
```

* Exercício 59: Imprima o padrão de asteriscos:

```
*
**
***
****
*****
```

```py
for i in range(1, 6):
    print("*" * i)
```

* Exercício 60: Peça um número ao usuário e imprima a sequência de Fibonacci até aquele número. (0, 1, 1, 2, 3, 5, 8...)

```py
n_fib = int(input("Digite um número para a sequência de Fibonacci: "))
a, b = 0, 1
print("Sequência de Fibonacci:")
while a <= n_fib:
    print(a)
    a, b = b, a + b
```

* Exercício 61: Use um loop `for` para iterar sobre uma string e contar o número de espaços em branco.

```py
frase_espacos = "Esta é uma frase com alguns espaços."
contador_espacos = 0
for caractere in frase_espacos:
    if caractere == " ":
        contador_espacos += 1
print(f"A frase tem {contador_espacos} espaços em branco.")
```

* Exercício 62: Simule um caixa eletrônico: peça ao usuário o valor a ser sacado e diga quantas notas de 100, 50, 20, 10, 5 e 1 serão necessárias.

```py
valor = int(input("Digite o valor a ser sacado (apenas notas inteiras): "))

notas_100 = valor // 100
valor %= 100

notas_50 = valor // 50
valor %= 50

notas_20 = valor // 20
valor %= 20

notas_10 = valor // 10
valor %= 10

notas_5 = valor // 5
valor %= 5

notas_1 = valor // 1

print("Notas necessárias:")
if notas_100 > 0:
    print(f"{notas_100} nota(s) de R$100")
if notas_50 > 0:
    print(f"{notas_50} nota(s) de R$50")
if notas_20 > 0:
    print(f"{notas_20} nota(s) de R$20")
if notas_10 > 0:
    print(f"{notas_10} nota(s) de R$10")
if notas_5 > 0:
    print(f"{notas_5} nota(s) de R$5")
if notas_1 > 0:
    print(f"{notas_1} nota(s) de R$1")
if notas_100 == 0 and notas_50 == 0 and notas_20 == 0 and notas_10 == 0 and notas_5 == 0 and notas_1 == 0:
    print("Nenhuma nota necessária para o valor digitado.")
```

* Exercício 63: Crie um loop `while` que imprima os números de 10 a 1 em ordem decrescente.

```py
contador_decrescente = 10
while contador_decrescente >= 1:
    print(contador_decrescente)
    contador_decrescente -= 1
```

* Exercício 64: Peça um número e determine se ele é primo ou não. (Um número primo é divisível apenas por 1 e por ele mesmo).

```py
num_primo = int(input("Digite um número inteiro para verificar se é primo: "))
if num_primo < 2:
    print(f"{num_primo} não é primo.")
else:
    eh_primo_flag = True
    for i in range(2, int(num_primo**0.5) + 1):
        if num_primo % i == 0:
            eh_primo_flag = False
            break
    if eh_primo_flag:
        print(f"{num_primo} é primo.")
    else:
        print(f"{num_primo} não é primo.")
```

## Funções

* Exercício 65: Função que retorna o quadrado de um número

```py
def quadrado(n):
    return n ** 2
print(quadrado(5))  # Saída: 25
```

* Exercício 66: Função que recebe nome e idade e imprime mensagem

```py
def saudacao(nome, idade):
    print(f"Olá {nome}, você tem {idade} anos!")
saudacao("João", 30)
```

* Exercício 67: Função que soma elementos de uma lista

```py
def soma_lista(lista):
    return sum(lista)
print(soma_lista([1, 2, 3]))  # Saída: 6
```

* Exercício 68: Função que verifica se número é primo

```py
def eh_primo(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True
print(eh_primo(7))  # Saída: True
```

* Exercício 69: Função que retorna fatorial de um número

```py
def fatorial(n):
    resultado = 1
    for i in range(2, n+1):
        resultado *= i
    return resultado
print(fatorial(5))  # Saída: 120
```

* Exercício 70: Crie uma função que receba uma lista de números e retorne o maior valor.

```py
def encontrar_maior(lista):
    return max(lista)

numeros_maior = [10, 5, 20, 8, 15]
print(f"O maior número na lista é: {encontrar_maior(numeros_maior)}")
```

* Exercício 71: Crie uma função que receba uma string e retorne o número de caracteres dela.

```py
def contar_caracteres(texto):
    return len(texto)

frase = "Programação em Python"
print(f"A frase '{frase}' tem {contar_caracteres(frase)} caracteres.")
```

* Exercício 72: Escreva uma função que receba um valor e uma taxa de juros anual, e calcule o valor final após um ano de juros simples. ($ValorFinal = ValorInicial * (1 + Taxa)$)

```py
def juros_simples(valor_inicial, taxa_anual):
    return valor_inicial * (1 + taxa_anual)

valor_inicial_ex = 1000
taxa_anual_ex = 0.05 # 5%
print(f"Valor final com juros: R${juros_simples(valor_inicial_ex, taxa_anual_ex):.2f}")
```

* Exercício 73: Crie uma função que receba um nome e um sobrenome e retorne o nome completo formatado.

```py
def nome_completo(nome, sobrenome):
    return f"{nome} {sobrenome}"

print(nome_completo("Maria", "Silva"))
```

* Exercício 74: Escreva uma função que receba um número inteiro e retorne `True` se for par e `False` se for ímpar.

```py
def eh_par(numero):
    return numero % 2 == 0

print(f"10 é par? {eh_par(10)}")
print(f"7 é par? {eh_par(7)}")
```

* Exercício 75: Crie uma função que receba uma lista de palavras e retorne uma nova lista com as palavras em maiúsculas.

```py
def maiusculas(lista_palavras):
    return [palavra.upper() for palavra in lista_palavras]

palavras_ex = ["python", "programacao", "desafio"]
print(f"Palavras em maiúsculas: {maiusculas(palavras_ex)}")
```

* Exercício 76: Escreva uma função que simule um "cara ou coroa" e retorne "Cara" ou "Coroa".

```py
import random

def cara_ou_coroa():
    resultado = random.choice(["Cara", "Coroa"])
    return resultado

print(f"Você jogou a moeda e deu: {cara_ou_coroa()}")
```

* Exercício 77: Crie uma função que receba uma temperatura em Fahrenheit e retorne a temperatura em Celsius. ($C = (F - 32) * 5/9$)

```py
def fahrenheit_para_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

temp_f = 68
print(f"{temp_f}F é igual a {fahrenheit_para_celsius(temp_f):.2f}C")
```

* Exercício 78: Escreva uma função que receba uma lista de strings e retorne a string mais longa.

```py
def string_mais_longa(lista_strings):
    if not lista_strings:
        return ""
    mais_longa = lista_strings[0]
    for s in lista_strings:
        if len(s) > len(mais_longa):
            mais_longa = s
    return mais_longa

palavras_longas = ["sol", "lua", "estrela", "universo"]
print(f"A string mais longa é: '{string_mais_longa(palavras_longas)}'")
```

* Exercício 79: Crie uma função que calcule a média de uma lista de números.

```py
def calcular_media(lista_numeros):
    if not lista_numeros:
        return 0
    return sum(lista_numeros) / len(lista_numeros)

notas_media = [7.5, 8.0, 6.5, 9.0]
print(f"A média das notas é: {calcular_media(notas_media):.2f}")
```

* Exercício 80: Escreva uma função que receba um número e imprima a tabuada daquele número (de 1 a 10).

```py
def tabuada(numero):
    print(f"Tabuada do {numero}:")
    for i in range(1, 11):
        print(f"{numero} x {i} = {numero * i}")

tabuada(7)
```

* Exercício 81: Crie uma função que receba dois números e retorne o resultado da divisão, tratando o caso de divisão por zero.

```py
def divisao_segura(dividendo, divisor):
    if divisor == 0:
        return "Erro: Divisão por zero!"
    return dividendo / divisor

print(f"10 dividido por 2: {divisao_segura(10, 2)}")
print(f"5 dividido por 0: {divisao_segura(5, 0)}")
```

* Exercício 82: Crie uma função que receba um dicionário e imprima todas as chaves e seus respectivos valores.

```py
def imprimir_dicionario(dicionario):
    for chave, valor in dicionario.items():
        print(f"Chave: {chave}, Valor: {valor}")

info_pessoal = {"nome": "Carlos", "idade": 35, "cidade": "Rio de Janeiro"}
imprimir_dicionario(info_pessoal)
```

* Exercício 83: Escreva uma função que receba um número e retorne `True` se ele for um número perfeito (a soma de seus divisores próprios é igual ao próprio número, ex: 6 = 1+2+3) e `False` caso contrário.

```py
def eh_numero_perfeito(numero):
    if numero < 1:
        return False
    soma_divisores = 1 # 1 é sempre um divisor próprio
    for i in range(2, int(numero**0.5) + 1):
        if numero % i == 0:
            soma_divisores += i
            if i * i != numero: # Adiciona o par do divisor se não for a raiz quadrada
                soma_divisores += numero // i
    return soma_divisores == numero

print(f"6 é um número perfeito? {eh_numero_perfeito(6)}")
print(f"28 é um número perfeito? {eh_numero_perfeito(28)}")
print(f"10 é um número perfeito? {eh_numero_perfeito(10)}")
```

* Exercício 84: Crie uma função que receba uma lista de números e retorne uma nova lista contendo apenas os números pares.

```py
def extrair_pares(lista_numeros):
    pares = [num for num in lista_numeros if num % 2 == 0]
    return pares

numeros_mistos = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(f"Números pares: {extrair_pares(numeros_mistos)}")
```

* Exercício 85: Escreva uma função que receba uma string e retorne o número de vogais (a, e, i, o, u) na string (ignorando maiúsculas/minúsculas).

```py
def contar_vogais(texto):
    vogais = "aeiou"
    contador = 0
    for char in texto.lower():
        if char in vogais:
            contador += 1
    return contador

frase_vogais = "Hello World Python"
print(f"Número de vogais em '{frase_vogais}': {contar_vogais(frase_vogais)}")
```

* Exercício 86: Crie uma função que simule um cronômetro regressivo. Receba o tempo inicial em segundos e imprima a contagem a cada segundo até chegar a zero.

```py
import time

def cronometro_regressivo(segundos):
    while segundos > 0:
        print(segundos)
        time.sleep(1) # Pausa por 1 segundo
        segundos -= 1
    print("Tempo esgotado!")

# Descomente a linha abaixo para testar (irá aguardar 5 segundos)
# cronometro_regressivo(5)
```
