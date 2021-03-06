# Definindo e chamando funções

>[**função**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:função)
>Uma sequência nomeada de declarações que executa alguma operação útil. As funções podem receber argumentos ou não e podem ou não produzir algum resultado.

### Sintaxe da definição de uma função
```python
def nome_da_função(nome_parâmetro, outro_nome_parâmetro): # esta função tem dois parâmetros
     corpo_com_instruções_que_a_função_executa
     
def outra_função(): # esta função não tem nenhum parâmetro
     corpo_da_outra_função
```

### Sintaxe da invocação, ou chamada, de uma função

```python
nome_da_função(valor, outro_valor) # esta função precisa de dois argumentos

outra_função() # esta função não requer argumentos
```

Os parâmetros, quando existem, recebem os valores dos argumentos usados quando a função é chamada.

### Exemplo da função `olho()`

```python
def setup():
    size(400, 400)
    background(0)
    olho(300, 100, random(50, 100)) # x, y, tamanho sorteado
    olho(100, 200, random(10, 150)) 
    olho(200, 300, random(10, 150))

def olho(x, y, tamanho) :
    """Olho precisa de 3 parâmetros"""
    noStroke()
    fill(255)
    ellipse(x, y, tamanho, tamanho/2)
    fill(0)
    circle(x, y, tamanho*.40)
```

### Funções que devolvem resultados

A função `olho()` desenha um olho mas não devolve nenhum valor, na verdade ela devolve o valor especial `None` (uma espécie de "nada"). Mas é comum termos funções que devolvem algum valor como resultado. Aqui alguns exemplos:

```python
def cor_sorteada():
    """Sorteia uma cor RGB"""
    r = random(256)
    g = random(256)
    b = random(256)
    cor = color(r, g, b)
    return cor # instrução que devolve a cor e retorna o fluxo de execução
```

Uso:
```python
fill(cor_sorteada())   # pede um preenchimento com uma cor sorteada!
rect(10, 10, 100, 50)
```

Da mesma maneira todo o tipo de manipulação de valores pode ser "encapsulada" em uma função.

```python
def media(a, b):
     return (a + b) / 2.
```

#### Glossário

[**encapsulamento**](https://penseallen.github.io/PensePython2e/04-caso-interface.html#termo:encapsulamento) O processo de transformar uma sequência de instruções em uma definição de função.

[**definição de função**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:definição%20de%20função) Uma instrução que cria uma função nova, especificando seu nome, parâmetros e as instruções que contém.

[**cabeçalho**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:cabeçalho) A primeira linha de uma definição de função.

[**corpo**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:corpo) A sequência de instruções dentro de uma definição de função.

[**parâmetro**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:parâmetro) Um nome usado dentro de uma função para se referir ao valor passado como argumento.

[**chamada de função**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:chamada%20de%20função) Uma instrução que executa uma função. É composta pelo nome da função seguido de uma lista de argumentos entre parênteses, ou caso a função possa ser chamada sem argumentos, só os parênteses (`nome()`).

[**argumento**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:argumento) Um valor apresentado a uma função quando a função é chamada. Este valor é atribuído ao parâmetro correspondente na função.

[**valor de retorno**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:valor%20de%20retorno) O resultado de uma função. Se uma chamada de função for usada como uma expressão, o valor de retorno é o valor da expressão.

[**função com resultado**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:função%20com%20resultado) Uma função que devolve um valor.

[**`None`**](https://penseallen.github.io/PensePython2e/03-funcoes.html#termo:None) Um valor especial apresentado por funções nulas (circularmente definidas como funções que devolvem o valor `None`, em lugar de outro valor de resultado).

---
Este material é baseado no material do curso https://arteprog.space/programacao-criativa/

---
Texto e imagens / text and images: CC BY-NC-SA 4.0; Código / code: GNU GPL v3.0 exceto onde explicitamente indicado por questões de compatibilidade.
