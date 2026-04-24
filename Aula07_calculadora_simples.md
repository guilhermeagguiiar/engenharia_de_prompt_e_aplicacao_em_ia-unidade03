def calcular(a, b, op):
    if op == '+':
        return a + b
    elif op == '-':
        return a - b
    elif op == '*':
        return a * b
    elif op == '/':
        if b == 0:
            return "Erro: divisão por zero"
        return a / b
    else:
        return "Operação inválida"


print("=== Calculadora ===")
while True:
    try:
        a = float(input("\nPrimeiro número: "))
        op = input("Operação (+, -, *, /) ou 'q' para sair: ")
        if op == 'q':
            break
        b = float(input("Segundo número: "))
        resultado = calcular(a, b, op)
        print(f"Resultado: {resultado}")
    except ValueError:
        print("Entrada inválida. Digite um número.")
