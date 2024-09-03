# 1. Calcular o valor de uma variável em um loop
def calcular_soma():
    total_soma = 0
    for i in range(1, 101):
        total_soma += i
    return total_soma

# 2. Determinar a inclusão de um número na sequência de Fibonacci
import math

def eh_quadrado_perfeito(x):
    s = int(math.sqrt(x))
    return s * s == x

def eh_fibonacci(n):
    return eh_quadrado_perfeito(5 * n * n + 4) or eh_quadrado_perfeito(5 * n * n - 4)

# 3. Analisar os dados de receita diária
def calcular_media_receita(receitas):
    total_receita = sum(receitas)
    numero_de_dias = len(receitas)
    return total_receita / numero_de_dias if numero_de_dias > 0 else 0

# 4. Calcular a porcentagem da receita estadual
def calcular_percentual(receita_estado, receita_total):
    return (receita_estado / receita_total) * 100 if receita_total > 0 else 0

# 5. Reverter strings sem usar funções integradas
def reverter_string(s):
    string_revertida = ""
    for char in s:
        string_revertida = char + string_revertida
    return string_revertida

if __name__ == "__main__":
    # Teste das soluções
    print("1. Soma dos números de 1 a 100:", calcular_soma())

    num = int(input("2. Digite um número para verificar se é Fibonacci: "))
    if eh_fibonacci(num):
        print(f"{num} é um número de Fibonacci.")
    else:
        print(f"{num} não é um número de Fibonacci.")

    receitas = [float(x) for x in input("3. Digite as receitas diárias separadas por espaço: ").split()]
    media_receita = calcular_media_receita(receitas)
    print(f"A receita média diária é {media_receita:.2f}")

    receita_estado = float(input("4. Digite a receita do estado: "))
    receita_total = float(input("Digite a receita total do país: "))
    percentual = calcular_percentual(receita_estado, receita_total)
    print(f"A porcentagem da receita estadual é {percentual:.2f}%")

    input_string = input("5. Digite uma string para reverter: ")
    string_revertida = reverter_string(input_string)
    print(f"A string revertida é: {string_revertida}")
