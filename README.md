def adicionar(x, y):
    return x + y

def subtrair(x, y):
    return x - y

def multiplicar(x, y):
    return x * y

def dividir(x, y):
    if y == 0:
        return "Erro: Divisão por zero não é permitida."
    return x / y

def main():
    print("Calculadora Simples")
    print("Selecione a operação desejada:")
    print("1. Adição")
    print("2. Subtração")
    print("3. Multiplicação")
    print("4. Divisão")
    
    while True:
        escolha = input("Digite o número da operação (1/2/3/4): ")
        
        if escolha in ['1', '2', '3', '4']:
            try:
                x = float(input("Digite o primeiro número: "))
                y = float(input("Digite o segundo número: "))
            except ValueError:
                print("Entrada inválida. Digite números válidos.")
                continue
            
            if escolha == '1':
                print(f"Resultado: {adicionar(x, y)}")
            elif escolha == '2':
                print(f"Resultado: {subtrair(x, y)}")
            elif escolha == '3':
                print(f"Resultado: {multiplicar(x, y)}")
            elif escolha == '4':
                print(f"Resultado: {dividir(x, y)}")
        else:
            print("Escolha inválida. Tente novamente.")
        
        mais_calculos = input("Deseja realizar outra operação? (s/n): ").strip().lower()
        if mais_calculos != 's':
            break

if __name__ == "__main__":
    main()
