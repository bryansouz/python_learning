## Python

---

- Python Variáveis & Tipos de Dados
    - Introdução ao Google Colab
        - pelo que eu entendi google colab é um pagina web para desenvolver codigos python
        - com a vantagem de poder usar codigo, texto e imagem. nao sei bem como
        - tem alguma coisa de GPU e TPU que não sei o que é
        - e da pra integrar com o drive
    - Variáveis
        - explica o que é variaveis(q eu ja sei)
        - tipos nativos, boolean, string, NoneType e falou sobre “type”
    - Numéros
        - nada de novo
    - String
        
        ```
        palavras = "aqui tem um texto"
        print(palavras.replace('tem', 'nao tem'))
        print(palavras.find('tem'))
        print(palavras.upper())
        
        *// aqui nao tem um texto
        // 5
        // AQUI TEM UM TEXTO*
        ```
        
        ```
        latlong = '523;435'
        corte = latlong.find(';')
        lat = latlong[1+corte:len(latlong)]
        log = latlong[0:corte]
        
        print('latutude: |'+lat+'| longitude: |'+ log+'|')
        
        ```
        
        - upper(), replece, find(), esses eu usei pouco
    - Booleano
        
        ```
        senha_cartao = 1234
        senha_digitada = 1334
        verificar = senha_cartao == senha_digitada
        print(verificar)
        ```
        
        - nada de novo
- Python Estruturas de Dados
    - Listas
        - indexação
            
            ```
            lista = ['a', 'b', 'c', 'd']
            print(lista[0])  # saída: 'a'
            ```
            
        - slicing
            
            ```
            lista = ['a', 'b', 'c', 'd']
            print(lista[1:3])  # saída: ['b', 'c']
            ```
            
        - adição
            
            ```
            lista = ['a', 'b', 'c']
            lista.append('d')
            print(lista)  # saída: ['a', 'b', 'c', 'd']
            ```
            
        - remoção
            
            ```
            lista = ['a', 'b', 'c', 'd']
            lista.remove('c')
            print(lista)  # saída: ['a', 'b', 'd']
            ```
            
        - ordenação
            
            ```
            lista = [3, 2, 1, 4]
            lista.sort()
            print(lista)  # saída: [1, 2, 3, 4]
            ```
            
    - Conjuntos
        - União
            
            ```
            conjunto1 = {1, 2, 3}
            conjunto2 = {2, 3, 4}
            uniao = conjunto1 | conjunto2
            print(uniao)  # saída: {1, 2, 3, 4}
            ```
            
        - Interseção
            
            ```
            conjunto1 = {1, 2, 3}
            conjunto2 = {2, 3, 4}
            intersecao = conjunto1 & conjunto2
            print(intersecao)  # saída: {2, 3}
            ```
            
        - Diferença
            
            ```
            conjunto1 = {1, 2, 3}
            conjunto2 = {2, 3, 4}
            diferenca = conjunto1 - conjunto2
            print(diferenca)  # saída: {1}
            ```
            
        - Teste de pertinência.
            
            ```
            conjunto = {1, 2, 3}
            print(2 in conjunto)  # saída: True
            print(4 in conjunto)  # saída: False
            ```
            
    - Dicionários
        
        Criar
        
        ```jsx
        dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}
        ou
        dicionario = dict(chave1='valor1', chave2='valor2')
        ```
        
        Acessar
        
        ```jsx
        dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}
        print(dicionario['chave1'])  # saída: 'valor1'
        ```
        
        Adicionar
        
        ```jsx
        dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}
        dicionario['chave3'] = 'valor3'
        print(dicionario)  # saída: {'chave1': 'valor1', 'chave2': 'valor2', 'chave3': 'valor3'}
        ```
        
        Remover
        
        ```jsx
        dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}
        del dicionario['chave1']
        print(dicionario)  # saída: {'chave2': 'valor2'}
        ```
        
        Ordenar
        
        ```jsx
        dicionario = {'b': 2, 'a': 1, 'c': 3}
        dicionario_ordenado = sorted(dicionario.items(), key=lambda x: x[0])
        print(dicionario_ordenado)  # saída: [('a', 1), ('b', 2), ('c', 3)]
        ```
        
        Verificar
        
        ```jsx
        dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}
        print('chave1' in dicionario)  # saída: True
        print('chave3' in dicionario)  # saída: False
        ```
        
- Python Fluxo Condicional & Repetições
    - Estrutura condicional if - else - elif
        
        a) Crie um programa que solicite ao usuário um número inteiro e verifique se ele é positivo, negativo ou igual a zero. Caso seja positivo, exiba a mensagem "O número é positivo", caso seja negativo, exiba "O número é negativo" e caso seja igual a zero, exiba "O número é igual a zero".
        
        ```python
        number = -1
        if(number > 0):
          print('O número é positivo')
        else:
          print('O número é negativo')
        ```
        
        b) Crie um programa que solicite ao usuário o seu nome e a sua idade e verifique se ele é maior de idade ou não. Caso seja maior de idade, exiba a mensagem "Seja bem-vindo, [nome]!", caso contrário, exiba a mensagem "Você não tem idade suficiente para acessar este site."
        
        ```python
        nome = 'Bryan'
        number = 12
        if(number >= 18):
          print('Seja bem-vindo,', nome +'!')
        else:
          print('Você não tem idade suficiente para acessar este site.')
        ```
        
    - Estrutura condicional try, cacth, finally
        
        a) Crie um programa que solicite ao usuário um número inteiro e tente convertê-lo para float. Caso ocorra um erro de conversão, exiba a mensagem "O valor inserido não é um número inteiro válido", caso contrário, exiba o valor convertido.
        
        ```python
        numero = 2
        try:
          print("O número convertido é:", numero)
        except ValueError:
            print("O valor inserido não é um número inteiro válido")
        ```
        
        b) Crie um programa que solicite ao usuário o nome de um arquivo e tente abrir esse arquivo. Caso ocorra um erro de abertura do arquivo, exiba a mensagem "Não foi possível abrir o arquivo", caso contrário, exiba o conteúdo do arquivo.
        
        ```python
        try:
            arquivo = open("meu_arquivo.txt", "r")
            print("O arquivo foi aberto com sucesso!")
        except IOError:
            print("Não foi possível abrir o arquivo")
        ```
        
    - Estrutura condicional for - in - range
        
        a) Crie um programa que exiba na tela todos os números pares de 0 a 10 utilizando a estrutura de repetição for.
        
        ```python
        for valor in range(0,12,2):
          print(valor)
        ```
        
        b) Crie um programa que solicite ao usuário uma palavra e exiba na tela a quantidade de vogais que essa palavra possui utilizando a estrutura de repetição for e a função in.
        
        ```python
        palavra = 'maranhao'
        letras = list(palavra)
        vogais = 'aeiou'
        array = []
        for l in letras:
          for v in list(vogais):
            if(l == v):
              array.append(l)
              print(array)
        ```
        
- Python Arquivos & Funções
    
    ## Leitura
    ``````
    %%writefile banco.csv
    age,job,marital,education,default,balance,housing,loan
    30,unemployed,married,primary,no,1787,no,no
    33,services,married,secondary,no,4789,yes,yes
    35,management,single,tertiary,no,1350,yes,no
    30,management,married,tertiary,no,1476,yes,yes
    59,blue-collar,married,secondary,no,0,yes,no
    35,management,single,tertiary,no,747,no,no
    36,self-employed,married,tertiary,no,307,yes,no
    39,technician,married,secondary,no,147,yes,no
    41,entrepreneur,married,tertiary,no,221,yes,no
    43,services,married,primary,no,-88,yes,yes
    ``````
    ## Comando para ler todo o conteúdo de um arquivo.
    ``````
    with open(file='./banco.csv', mode='r', encoding='utf8') as db:
    print(db.read())
    ``````
    ## Comando para ler o conteúdo de um arquivo uma linha por vez.
    ``````
    with open(file='./banco.csv', mode='r', encoding='utf8') as linha:
    print(linha.readline())
    ``````
    ## Extraindo os valores da primeira coluna (idade).
    ``````
    array = []
    with open(file='./banco.csv', mode='r', encoding='utf8') as idade:
    idade.readline()
    age = idade.readline()
    while age:
    lista = age.split(sep=',')
    array.append(lista)
    age = idade.readline()
    print(array)
    ``````
    ## Comando para escrever em um arquivo, se o arquivo não existir, ele será criado.
    ``````
    rescrever = None
    with open(file='./banco3.csv', mode='w', encoding='utf8') as rescrever:
    line = 'hello word!'
    rescrever.write(line)
    
    with open(file='./banco3.csv', mode='r', encoding='utf8') as ler:
    lendo = ler.read()
    
    print(lendo)
    ``````
    ## Você trabalha na bolsa de valores e precisa simular o retorno de um investimento para diversos cenários:
    ``````
    def bolsaValores(valor_inicial:float, taxa_juros_anual:float, anos:int) -> str:
    valor_final = valor_inicial
    for ano in range(1, anos+1):
    valor_final = valor_final * (1 + taxa_juros_anual)
    valor_final = round(valor_final, 2)
    print(f'Para um valor inicial de R$ {valor_inicial} e uma taxa de juros anual de {taxa_juros_anual}, em {anos} anos você terá R$ {valor_final}')
    
    bolsaValores(16020, 0.13, 5)
    ``````
# Programação Funcional

##1. Função lambda;

email = 'bryan.soares19@hotmail.com';
extrair_nome_email = lambda email: email.split(sep='@')[0]
nome_email = extrair_nome_email(email)

def retorno(juros: float, investimento: float):
  j = lambda investimento: investimento * (1 + juros)
  i = j(investimento)
  return i

print(retorno(5, 1000))

## 2. Função map

numeros = [1, 2, 3]
quadrado = map(lambda numero: numero ** 2, [21,212,43123,513213])
print(list(quadrado))

not1 = [8, 7, 6]
not2 = [9, 5, 8]
aritimetica = map(lambda n1, n2:(n1 + n2)/2, not1, not2)
print(list(aritimetica))

## 3. Função filter

nomes = ['jose pedro', 'maria','maria','maria','maria', 'mauricio']
numeros_par = filter(lambda nomes: nomes == 'maria', nomes)
print(list(numeros_par))

## 4. Função reduce

from functools import reduce

numeros = [1, 2, 3]
soma = reduce(lambda x, y: x + y, numeros)
print(soma)


*texto em itálico*# Nova seção

# Programação Orientada a Objetos

### 1. Crie uma classe chamada Pessoa com atributos nome e idade. Adicione um método chamado apresentacao que imprime uma mensagem contendo o nome e a idade da pessoa.

class Pessoa:
  def __init__(self, nome, idade) -> None:
    self.nome = nome
    self.idade = idade
  def toSay(self):
    print(f"Meu nome é {self.nome} e tenho {self.idade} anos")


joao = Pessoa('joão',19)
joao.toSay()

### 2. Crie uma classe chamada *ContaBancaria* com atributos privados saldo e numero. Adicione métodos para depositar, sacar e consultar o saldo da conta. Garanta que os métodos de saque e depósito não permitam valores negativos.

class ContaBancaria:
    def __init__(self, saldo, number):
        self.__saldo = saldo
        self.__number = number

    def sacar(self, valor_saque):
       if self.__saldo > 0 and valor_saque <= self.__saldo:
          self.__saldo -= valor_saque
       else:
         print('valor indisponivel')

    def depositar(self, valor_deposito):
        self.__saldo += valor_deposito

    def consulta(self):
        print(f'seu saldo atual é de R$ {self.__saldo}')

c = ContaBancaria(0, 2131332)
c.depositar(100)
c.sacar(20)
c.consulta()

### 3. Crie uma classe base chamada Animal com um método chamado falar. Crie classes derivadas chamadas Cachorro e Gato, que herdam de Animal. Implemente o método falar em ambas as classes derivadas para imprimir "Au au!" e "Miau!", respectivamente.

self.falar(self)
    

class Gata(Animal):

r = Retangulo(10, 20)
r.calcular_area()

### 4. Crie uma classe abstrata chamada FiguraGeometrica com um método abstrato chamado area. Crie classes derivadas chamadas Circulo e Retangulo, que herdam de FiguraGeometrica. Implemente o método area em ambas as classes derivadas para calcular a área do círculo e do retângulo, respectivamente.

class ContaBancaria:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.__saldo = saldo
        self.limite = 1000

    def depositar(self, valor):
        self.__saldo += valor
        print(f"Depósito de R${valor:.2f} realizado. Novo saldo: R${self.__saldo:.2f}")

    def sacar(self, valor):
        if valor > self.__saldo:
            print("Saldo insuficiente.")
        else:
            self.__saldo -= valor
            print(f"Saque de R${valor:.2f} realizado. Novo saldo: R${self.__saldo:.2f}")

c = ContaBancaria('byan', 200)
c._ContaBancaria__saldo = 400
c.sacar(123)
c.sacar(87)
c.sacar(87)


# Módulos & Pacotes

### 1. Importe o módulo math e utilize a função sqrt para calcular a raiz quadrada de 81. Utilize o alias m ao importar o módulo.

import math as m 
m.sqrt(81)

2. Crie um módulo chamado conversor.py com duas funções: celsius_para_fahrenheit(temp_celsius) e fahrenheit_para_celsius(temp_fahrenheit). Importe esse módulo e converta 100 graus Celsius para Fahrenheit e 212 graus Fahrenheit para Celsius.

with open(file='conversor.py', mode='w', encoding='utf8') as conversor:
  conversor.write('def celsius_para_fahrenheit(number): \n  return number*1.8+32')

import conversor as cnv

cnv.celsius_para_fahrenheit(100)

3. Baixe e instale o pacote requests. Importe-o e faça uma requisição GET para 'https://api.github.com'. Verifique se a resposta tem o status code 200.

import requests as req

req.get('https://api.github.com')

4. Crie um pacote chamado validador: email validar_email(email) que retorna True se o email fornecido for válido e False caso contrário. Importe e teste em um arquivo Python separado.

with open(file='mail.py', mode='w', encoding='utf8') as email:
    email.write('def valide_email(email):\n')
    email.write('    if "@" in email and "." in email.split("@")[-1]:\n')
    email.write('        return "TrueA"\n')
    email.write('    else:\n')
    email.write('        return "FalseA"\n')

import mail as e

print(e.validar_email('aluno@gmail.com'))  


5. Utilize o módulo random para gerar uma lista de 10 números aleatórios entre 1 e 100. Em seguida, use o módulo statistics para calcular a média e o desvio padrão da lista.

import random
import statistics as stat

numeros_aleatorios = [random.randint(1, 10) for i in range(1,10]
print(f'Nota dos alunos foram: {numeros_aleatorios}')
print(f'A média das notas:{stat.mean(numeros_aleatorios)}')
print(f'E seu desvio padrão é:{stat.stdev(numeros_aleatorios)}')



6. Crie um módulo chamado fibonacci.py que contenha uma função fibonacci(n) que retorne o n-ésimo número da sequência de Fibonacci. Importe e teste a função em um arquivo Python separado.

with open(file='fibonacci.py', mode='w', encoding='utf8') as fbc:
    fbc.write(
'''def fibonacci(n):
    if n <= 0:
        raise ValueError("O valor de n deve ser positivo.")
    elif n == 1:
        return 0
    elif n == 2:
        return 1
    else:
        a, b = 0, 1
        for _ in range(n - 2):
            a, b = b, a + b
        return b
''')

import fibonacci as fib

print(fib.fibonacci(5))


7. Utilize o módulo os para criar um diretório chamado arquivos. Em seguida, crie um arquivo chamado dados.txt dentro do diretório arquivos e escreva nele a string "Dados importantes". Por fim, leia e imprima o conteúdo do arquivo dados.txt.

import os

if not os.path.exists('arquivos'):
  os.mkdir('arquivos')

with open(os.path.join('arquivos', 'dados.txt'), 'w') as arq:
  arq.write('Dados importantes')

with open(os.path.join('arquivos', 'dados.txt'),'r') as read:
  print(read.read())


8. Crie um módulo chamado ordenacao.py que contenha duas funções de ordenação: bubble_sort(lista) e selection_sort(lista). Importe e teste ambas as funções em um arquivo Python separado, utilizando uma lista de números desordenados.

import os
import sys

sys.path.append('bubble-arc')  
import bubble as b

num_random = [i + 1 for i in range(0, 10, 2)]
print(num_random)
print(b.bubble_sort(num_random))

9. Importe o módulo time e utilize a função sleep para criar um contador regressivo de 10 a 0, com um intervalo de 1 segundo entre cada número.

from time import sleep as dormir

for i in range(0, 10):
  dormir(1)
  print(f'{i+1} segundos')

10. Utilize o módulo json para converter uma string JSON em um dicionário Python. Em seguida, acesse um valor específico do dicionário e imprima-o.

import json

dicionario = {'nome': 'Bryan', 'idade': 23, 'cidade': 'Porto Alegre'}
format_json = json.dumps(dicionario)
print(f'JSON: {format_json}')
estrutura_dicionario = json.loads(format_json)
print(f'Dicionario: {estrutura_dicionario}')
print(estrutura_dicionario['nome'])
- Python Tratamento de Erros
- Python Scripting
