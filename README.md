# Funcion para clasificar compromiso
def clasificar_sesion(duracion, clics):
    if duracion > 180 and clics > 8:
        return "Alto"
    elif duracion < 60 or clics < 3:
        return "Bajo"
    else:
        return "Medio"
# Programa principal
# lista vacia para almacenar las sesiones
sesiones = []
print("Ingrese los datos de al menos 5 sesiones de clientes")
n = int(input("¿Cuántas sesiones desea registrar? (mínimo 5): "))
if n < 5:
    print("Debe ingresar al menos 5 sesiones.")
else:
    for i in range(n):
        print(f"\n--- Sesión {i+1} ---")
        id_cliente = int(input("Ingrese ID del cliente: "))
        duracion = int(input("Ingrese duración en segundos: "))
        clics = int(input("Ingrese número de clics: "))
        sesiones.append([id_cliente, duracion, clics])
 # Generar informe
    print("\nInforme de Clasificación de Sesiones")
    print("-----------------------------------")
    for sesion in sesiones:
        id_cliente, duracion, clics = sesion
        clasificacion = clasificar_sesion(duracion, clics)
        print(f"Cliente {id_cliente}: {clasificacion}")
