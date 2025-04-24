# calculadora.py

def somar(x, y):
    return x + y

def subtrair(x, y):
    return x - y

def multiplicar(x, y):
    return x * y

def dividir(x, y):
    if y == 0:
        return "Erro: divisão por zero"
    return x / y

def main():
    print("=== Calculadora em Python ===")
    print("Operações disponíveis:")
    print("1. Somar")
    print("2. Subtrair")
    print("3. Multiplicar")
    print("4. Dividir")

    escolha = input("Escolha a operação (1/2/3/4): ")

    try:
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
    except ValueError:
        print("Erro: entrada inválida. Digite números.")
        return

    if escolha == '1':
        print(f"Resultado: {somar(num1, num2)}")
    elif escolha == '2':
        print(f"Resultado: {subtrair(num1, num2)}")
    elif escolha == '3':
        print(f"Resultado: {multiplicar(num1, num2)}")
    elif escolha == '4':
        print(f"Resultado: {dividir(num1, num2)}")
    else:
        print("Opção inválida.")

if __name__ == "__main__":
    main()