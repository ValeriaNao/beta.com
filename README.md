# lista_de_nombres.py

# Lista inicial con tres nombres
nombres = ["valeria", "adrina", "henrry marcos"]

def mostrar_nombres():
    print("\nNombres actuales:")
    for i, nombre in enumerate(nombres, start=1):
        print(f"{i}. {nombre}")

def editar_nombre():
    mostrar_nombres()
    try:
        indice = int(input("\n¿Qué nombre deseas editar? (1-3): ")) - 1
        if 0 <= indice < len(nombres):
            nuevo_nombre = input("Escribe el nuevo nombre: ")
            nombres[indice] = nuevo_nombre
            print("Nombre actualizado con éxito.")
        else:
            print("Índice fuera de rango.")
    except ValueError:
        print("Por favor ingresa un número válido.")

def main():
    while True:
        editar_nombre()
        mostrar_nombres()
        continuar = input("\n¿Deseas editar otro nombre? (s/n): ").lower()
        if continuar != 's':
            break

if __name__ == "__main__":
    main()
