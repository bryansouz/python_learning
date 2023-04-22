# Analista de Dados - 47h | 20/04  
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
        - união
            
            ```
            conjunto1 = {1, 2, 3}
            conjunto2 = {2, 3, 4}
            uniao = conjunto1 | conjunto2
            print(uniao)  # saída: {1, 2, 3, 4}
            ```
            
        - interseção
            
            ```
            conjunto1 = {1, 2, 3}
            conjunto2 = {2, 3, 4}
            intersecao = conjunto1 & conjunto2
            print(intersecao)  # saída: {2, 3}
            ```
            
        - diferença
            
            ```
            conjunto1 = {1, 2, 3}
            conjunto2 = {2, 3, 4}
            diferenca = conjunto1 - conjunto2
            print(diferenca)  # saída: {1}
            ```
            
        - teste de pertinência.
            
            ```
            conjunto = {1, 2, 3}
            print(2 in conjunto)  # saída: True
            print(4 in conjunto)  # saída: False
            ```
            
    - Dicionários
        
        ```jsx
        dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}
        print(dicionario['chave1'])  # saída: 'valor1'
        ```
        
- Python Fluxo Condicional & Repetições
- Python Arquivos & Funções
- Python Programação Funcional
- Python Programação Orientada a Objetos
- Python Módulos & Pacotes
- Python Tratamento de Erros
- Python Scripting
