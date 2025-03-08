# Definir la matriz 3D (ciudades, días, semanas)
temperaturas = [
    [  # Ciudad 1
        [[15, 18, 20], [20, 22, 21], [21, 20, 19], [19, 18, 17], [17, 16, 15], [15, 14, 13], [13, 12, 11]],  # Semana 1
        [[16, 19, 21], [21, 23, 22], [22, 21, 20], [20, 19, 18], [18, 17, 16], [16, 15, 14], [14, 13, 12]]   # Semana 2
    ],
    [  # Ciudad 2
        [[25, 28, 30], [30, 32, 31], [31, 30, 29], [29, 28, 27], [27, 26, 25], [25, 24, 23], [23, 22, 21]],  # Semana 1
        [[26, 29, 31], [31, 33, 32], [32, 31, 30], [30, 29, 28], [28, 27, 26], [26, 25, 24], [24, 23, 22]]   # Semana 2
    ]
]

ciudades = ["Ciudad 1", "Ciudad 2"]
semanas = ["Semana 1", "Semana 2"]

# Calcular el promedio de temperaturas por ciudad y semana
for ciudad_idx, ciudad in enumerate(temperaturas):
    for semana_idx, semana in enumerate(ciudad):
        suma_temperaturas = 0
        conteo_dias = 0
        for dia in semana:
            suma_temperaturas += sum(dia)
            conteo_dias += len(dia)
        promedio = suma_temperaturas / conteo_dias
        print(f"El promedio de temperatura para la {ciudades[ciudad_idx]} durante {semanas[semana_idx]} es: {promedio:.2f}°C")
