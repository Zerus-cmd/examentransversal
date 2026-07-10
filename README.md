recorridos = {
    "R001" : ["Santiago", "Valparaiso", 120, "normal", "día", True],
    "R002" : ["Santiago", "Concepcion", 500, "cama", "noche", True],
    "R003" : ["La Serena", "Coquimbo", 15, "normal", "día", False],
    "R004" : ["Temuco", "Valdivia", 165, "semi-cama", "día", True],
    "R005" : ["Iquique", "Arica", 310, "cama", "noche", False],
    "R006" : ["Santiago", "Rancagua", 90, "normal", "dia", True],
    
}

venta = {
    "R001" : [7990, 20],
    "R002" : [25990, 0],
    "R003" : [1990, 35],
    "R004" : [12990, 8],
    "R005" : [18990, 3],
    "R006" : [4990, 12],

}

asientosdisponibles = 0

def buscar_codigo(codigo):
    buscar = input("").strip().lower()
    for i in range(len(recorridos)):
        if (recorridos[i][venta].lower() == buscar):
            print(f"La ciudad {recorridos} existe")
            return i
        
        print("lol")
        return -1


def asientos_origen(origen):
    origen = input("Ingrese la ciudad que planea ir: ")
    return origen


def busqueda_precio(p_min, p_max):
    try:
        p_min = int(input("Ingrese el precio minimo que desea utilizar: "))
        p_max = int(input("Ingrese la cantidad de pesos maximo que desea utilizar"))
        if p_min and p_max >= 0:
            if p_min <= p_max:
                return
        else:
            raise ValueError
    except ValueError:
        print("Ingrese un valor numerico")


def distancia_km():
    if distancia_km > 0:
        return distancia_km



def menu():
    print("=============MENU PRINCIPAL==============")
    print("1) Asientos por ciudad de origen")
    print("2) Búsqueda de recorridos por rango de precio")
    print("3) Actualizar precio de recorrido")
    print("4) Agregar recorrido")
    print("5) Eliminar recorrido")
    print("6) Salir")
    print("=========================================")

def leer_opc():
    try: 
        if (opc >= 1 and opc <= 6):
            return opc
        else:
            raise ValueError
    except ValueError:
        print ("Ingrese una opcion valida")


        
while True:
    try:

        menu()

        opc = int(input("Ingrese una opcion: "))

        leer_opc()

        if opc == 1:
            ciudad = input("Ingrese la ciudad que desea a viajar: ")

        elif opc == 2:
            busqueda_precio()

        elif opc == 3:
            buscar_codigo()

        elif opc == 4:
            pass    
        elif opc == 5:
            pass    
        elif opc == 6:
            break
        else:
            raise ValueError
    except ValueError:
        print("errooooooooooooooooor")
