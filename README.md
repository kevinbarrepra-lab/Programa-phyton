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
prin("Ingrese los datos de al menos 5 sesiones de clientes")
n = int(input("¿Cuántas sesiones desea registrar? (mínimo 5): "))
