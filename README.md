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
    
    ## Comando para ler todo o conteúdo de um arquivo.
    
    with open(file='./banco.csv', mode='r', encoding='utf8') as db:
    print(db.read())
    
    ## Comando para ler o conteúdo de um arquivo uma linha por vez.
    
    with open(file='./banco.csv', mode='r', encoding='utf8') as linha:
    print(linha.readline())
    
    ## Extraindo os valores da primeira coluna (idade).
    
    array = []
    with open(file='./banco.csv', mode='r', encoding='utf8') as idade:
    idade.readline()
    age = idade.readline()
    while age:
    lista = age.split(sep=',')
    array.append(lista)
    age = idade.readline()
    print(array)
    
    ## Comando para escrever em um arquivo, se o arquivo não existir, ele será criado.
    
    rescrever = None
    with open(file='./banco3.csv', mode='w', encoding='utf8') as rescrever:
    line = 'hello word!'
    rescrever.write(line)
    
    with open(file='./banco3.csv', mode='r', encoding='utf8') as ler:
    lendo = ler.read()
    
    print(lendo)
    
    ## Você trabalha na bolsa de valores e precisa simular o retorno de um investimento para diversos cenários:
    
    def bolsaValores(valor_inicial:float, taxa_juros_anual:float, anos:int) -> str:
    valor_final = valor_inicial
    for ano in range(1, anos+1):
    valor_final = valor_final * (1 + taxa_juros_anual)
    valor_final = round(valor_final, 2)
    print(f'Para um valor inicial de R$ {valor_inicial} e uma taxa de juros anual de {taxa_juros_anual}, em {anos} anos você terá R$ {valor_final}')
    
    bolsaValores(16020, 0.13, 5)
    
- Python Programação Funcional
- Python Programação Orientada a Objetos
- Python Módulos & Pacotes
- Python Tratamento de Erros
- Python Scripting
