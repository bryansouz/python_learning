# Analista de Dados - 47h | 20/04  
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
    - parei em listas(arrays)
- Python Estruturas de Dados
- Python Fluxo Condicional & Repetições
- Python Arquivos & Funções
- Python Programação Funcional
- Python Programação Orientada a Objetos
- Python Módulos & Pacotes
- Python Tratamento de Erros
- Python Scripting
