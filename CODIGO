import tkinter as tk
from tkinter import messagebox, ttk
import matplotlib.pyplot as plt
from matplotlib.backends.backend_tkagg import FigureCanvasTkAgg

def calcularM():
    try:
        txtX1 = firstEntry.get()
        txtY1 = secondEntry.get()
        txtX2 = thirdEntry.get()
        txtY2 = fourthEntry.get()
        if txtX1 and txtY1 and txtX2 and txtY2:
            x1 = float(txtX1)
            y1 = float(txtY1)
            x2 = float(txtX2)
            y2 = float(txtY2)
            if x1 and y1 and x2 and y2 == 0:
                tk.messagebox.showwarning(title="Error", message="Los valores ingresados no son validos para trazar una recta")
            else:
                dx = x2 - x1
                dy = y2 - y1
                i = 0
                xcoor = []
                ycoor = []
                try:
                    m = round(dy / dx, 3)
                    sexthLabel.config(text=m)
                    #Pendiente es igual a 0
                    if m == 0:
                        if dx > 0:
                            descrip_linea_label.config(text="Caso Especial M=0, 1. Izquierda - Derecha")
                            clearTable()
                            while x1 < x2 + 1:
                                xcoor.append(x1)
                                ycoor.append(y1)
                                x1 = x1 + 1
                                # Imprimimos valores en X
                                x_label = tk.Label(table, text=xcoor[i])
                                x_label.grid(row=1 + i, column=0)
                                x_label.configure(font=("Courier", 8, "bold"))
                                # Imprimimos valores en Y
                                d_label = tk.Label(table, text=ycoor[i])
                                d_label.grid(row=1 + i, column=1)
                                d_label.configure(font=("Courier", 8, "bold"))
                                # Completamos la configuración de las etiquetas
                                for widget in table.winfo_children():
                                    widget.grid_configure(padx=0, pady=0)
                                # Aumentamos el contador i
                                i = i + 1
                            plotGraphic(xcoor, ycoor)
                        else:
                            descrip_linea_label.config(text="Caso Especial M=0, 2. Derecha - Izquierda")
                            clearTable()
                            while x1 + 1 > x2:
                                xcoor.append(x1)
                                ycoor.append(y1)
                                x1 = x1 - 1
                                # Imprimimos valores en X
                                x_label = tk.Label(table, text=xcoor[i])
                                x_label.grid(row=1 + i, column=0)
                                x_label.configure(font=("Courier", 8, "bold"))
                                # Imprimimos valores en Y
                                d_label = tk.Label(table, text=ycoor[i])
                                d_label.grid(row=1 + i, column=1)
                                d_label.configure(font=("Courier", 8, "bold"))
                                # Completamos la configuración de las etiquetas
                                for widget in table.winfo_children():
                                    widget.grid_configure(padx=0, pady=0)
                                # Aumentamos el contador i
                                    i = i + 1
                            plotGraphic(xcoor, ycoor)
                    #Pendiente es positiva
                    elif m > 0:
                        #Pendiente es igual a 1
                        if m == 1:
                            if dx and dx > 0:
                                descrip_linea_label.config(text="1Caso Especial M=1, 1. Izquierda Derecha, Abajo Arriba")
                                clearTable()
                                while x2+1 > x1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1+1
                                    y1 = y1+1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                            else:
                                descrip_linea_label.config(text="2 Caso Especial M=1, 1. Derecha-Izquierda, Arriba-Abajo")
                                clearTable()
                                while x1 > x2:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1 - 1
                                    y1 = y1 - 1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                        #Pendiente es mayor a 1
                        elif m > 1:
                            #CASO 3
                            if(dx and dy > 0):
                                descrip_linea_label.config(text="+CASO 3: Izquierda Derecha, Abajo Arriba")
                                clearTable()
                                while y1<y2+1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1+(1/m)
                                    y1 = y1+1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                            #CASO 4
                            else:
                                descrip_linea_label.config(text="+CASO 4: Derecha Izquierda, Arriba a Abajo")
                                clearTable()
                                while y1>y2-1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1-(1/m)
                                    y1 = y1-1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)

                        #Pendiente es menor a 1 pero mayor a 0
                        else:
                            #CASO 1
                            if(dx and dy > 0):
                                descrip_linea_label.config(text="+CASO 1: Izquierda Derecha, Abajo Arriba")
                                clearTable()
                                while x1<x2+1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1+1
                                    y1 = y1+m
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                            #CASO 2
                            else:
                                descrip_linea_label.config(text="+CASO 2: Derecha Izquierda, Arriba a Abajo")
                                clearTable()
                                while x1>x2-1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1-1
                                    y1 = y1-m
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                    #Pendiente es negativa
                    else:
                        #Pendiente es igual a -1
                        if m == -1:
                            if dx<0:
                                descrip_linea_label.config(text="1Caso M=-1. Derecha, Izquierda. Abajo Arriba")
                                clearTable()
                                while x1 > x2-1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1-1
                                    y1 = y1+1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                            else:
                                descrip_linea_label.config(text="2Caso M=-1. Izquierda-Derecha. Arriba-Abajo")
                                clearTable()
                                while x1 < x2+1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1+1
                                    y1 = y1-1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                        #Pendiente es menor a -1
                        elif m<-1:
                            #CASO 3 ¡¡EN REVISIÓM!!
                            if dx<0:
                                descrip_linea_label.config(text="-CASO 3: Derecha, Izquierda. Abajo Arriba")
                                clearTable()
                                while y1<y2+1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1 - (1/abs(m))
                                    y1 = y1 + 1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                            #CASO 4 ¡¡EN REVISIÓM!!
                            else:
                                descrip_linea_label.config(text="-CASO 4: Izquierda - Derecha. Arriba - Abajo")
                                clearTable()
                                while y1>y2-1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1 + (1/abs(m))
                                    y1 = y1 - 1
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                        #Pendiente es mayor a 0 pero mayor a -1
                        else:
                            #CASO 1
                            if dx<0:
                                descrip_linea_label.config(text="-CASO 1: Derecha, Izquierda. Abajo Arriba")
                                clearTable()
                                while x1 > x2-1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1 - 1
                                    y1 = y1 + abs(m)
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                            #CASO 2
                            else:
                                descrip_linea_label.config(text="-CASO 2: Izquierda - Derecha. Abajo Arriba")
                                clearTable()
                                while x1 < x2+1:
                                    xcoor.append(x1)
                                    ycoor.append(y1)
                                    x1 = x1 + 1
                                    y1 = y1 - abs(m)
                                    #Imprimimos valores en X
                                    x_label=tk.Label(table,
                                    text=xcoor[i])
                                    x_label.grid(row=1+i, column=0)
                                    x_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Imprimimos valores en Y
                                    d_label=tk.Label(table,
                                    text=ycoor[i])
                                    d_label.grid(row=1+i, column=1)
                                    d_label.configure(font=("Courier",
                                    8, "bold"))
                                    #Completamos la configuración de las etiquetas
                                    for widget in table.winfo_children():
                                        widget.grid_configure(padx=0,pady=0)
                                    #Aumentamos el contador i
                                    i = i+1
                                plotGraphic(xcoor, ycoor)
                except ZeroDivisionError:
                    eme = dy, "/", dx
                    sexthLabel.config(text=eme)
                    if dy < 0:
                        descrip_linea_label.config(text="Caso error 1: Arriba - Abajo")
                        clearTable()
                        while y1 > y2 - 1:
                            xcoor.append(x1)
                            ycoor.append(y1)
                            y1 = y1 - 1
                            # Imprimimos valores en X
                            x_label = tk.Label(table, text=xcoor[i])
                            x_label.grid(row=1 + i, column=0)
                            x_label.configure(font=("Courier", 8, "bold"))
                            # Imprimimos valores en Y
                            d_label = tk.Label(table, text=ycoor[i])
                            d_label.grid(row=1 + i, column=1)
                            d_label.configure(font=("Courier", 8, "bold"))
                            # Completamos la configuración de las etiquetas
                            for widget in table.winfo_children():
                                widget.grid_configure(padx=0, pady=0)
                            # Aumentamos el contador i
                            i = i + 1
                        plotGraphic(xcoor, ycoor)
                    else:
                        descrip_linea_label.config(text="Caso error 2: Abajo - Arriba")
                        clearTable()
                        while y1 < y2 + 1:
                            xcoor.append(x1)
                            ycoor.append(y1)
                            y1 = y1 + 1
                            # Imprimimos valores en X
                            x_label = tk.Label(table, text=xcoor[i])
                            x_label.grid(row=1 + i, column=0)
                            x_label.configure(font=("Courier", 8, "bold"))
                            # Imprimimos valores en Y
                            d_label = tk.Label(table, text=ycoor[i])
                            d_label.grid(row=1 + i, column=1)
                            d_label.configure(font=("Courier", 8, "bold"))
                            # Completamos la configuración de las etiquetas
                            for widget in table.winfo_children():
                                widget.grid_configure(padx=0, pady=0)
                            # Aumentamos el contador i
                            i = i + 1
                        plotGraphic(xcoor, ycoor)
        else:
            tk.messagebox.showwarning(title="Error", message="Todos los campos son requeridos")
            clearTable()
    except ValueError:
        tk.messagebox.showwarning(title="Error", message="Ingrese solo números")
        clearTable()

def clearTable():
    x = range(30)
    for n in x:
        # Limpiamos valores en X
        x_label.config(text="")
        # Limpiamos valores en Y
        d_label.config(text="")

def plotGraphic(coorx, coory):
    ax.clear()
    ax.grid(True), ax.set_xlabel("Eje en X"), ax.set_ylabel("Eje en Y"), ax.set_title("Gráfica")
    ax.plot(coorx, coory)
    ax.plot(coorx[-1], coory[-1], 'o:c')
    line.draw()

# Creamos la ventana raíz
window = tk.Tk()
window.title("|Método Graficación Linea Recta|")
# window.resizable(False, False)
window.state("zoomed")
window.configure(bg="#6c043c")

# Primera mitad
frame = tk.Frame(window)
frame.configure(bg="#910142")
frame.grid(row=0, column=0, padx=15, pady=15)

# Segunda mitad
second_frame = tk.Frame(window)
second_frame.configure(bg="#910142")
second_frame.grid(row=0, column=1, padx=35)

# Primera sección: Ingresar datos
datos_section = tk.LabelFrame(frame, text="Ingrese los valores correspondientes: ")
datos_section.grid(row=0, column=0, padx=10, pady=10)
datos_section.configure(bg="#910142", font=("Courier", 16, "bold"))

# Primera línea
firstLabel = tk.Label(datos_section, text="Valor de X1")
firstLabel.grid(row=0, column=0)
firstLabel.configure(bg="#910142", font=("Courier", 10))
secondLabel = tk.Label(datos_section, text="Valor de Y1")
secondLabel.grid(row=0, column=1)
secondLabel.configure(bg="#910142", font=("Courier", 10))

# Segunda línea
firstEntry = tk.Entry(datos_section, justify="center")
firstEntry.grid(row=1, column=0)
secondEntry = tk.Entry(datos_section, justify="center")
secondEntry.grid(row=1, column=1)

# Tercera línea
thirdLabel = tk.Label(datos_section, text="Valor de X2")
thirdLabel.grid(row=2, column=0)
thirdLabel.configure(bg="#910142", font=("Courier", 10))
fourthLabel = tk.Label(datos_section, text="Valor de Y2")
fourthLabel.grid(row=2, column=1)
fourthLabel.configure(bg="#910142", font=("Courier", 10))

# Cuarta línea
thirdEntry = tk.Entry(datos_section, justify="center")
thirdEntry.grid(row=3, column=0)
fourthEntry = tk.Entry(datos_section, justify="center")
fourthEntry.grid(row=3, column=1)

# Quinta línea: Pendiente = M
fifthLabel = tk.Label(datos_section, text="Valor de la pendiente (m) --->")
fifthLabel.grid(row=4, column=0)
fifthLabel.configure(bg="#910142", font=("Courier", 10))
sexthLabel = tk.Label(datos_section, text=" ")
sexthLabel.grid(row=4, column=1)

for widget in datos_section.winfo_children():
    widget.grid_configure(padx=10, pady=10)

# Segunda sección
info_section = tk.LabelFrame(frame, text="Descripción del caso y la recta")
info_section.grid(row=1, column=0, padx=10, pady=10, sticky="news")
info_section.configure(font=("Courier", 12, "bold"))

# Etiqueta descripcion del caso
descrip_linea_label = tk.Label(info_section, text="")
descrip_linea_label.grid(row=0, column=0, padx=10, pady=10)
descrip_linea_label.configure(bg="#fef7d5", font=("Courier", 10))

# Botón para calcular M
button = tk.Button(frame, text="Graficar", command=calcularM)
button.grid(row=2, column=0, sticky="ew", padx=20, pady=10)
button.configure(font=("Courier", 12, "bold"), bg="#b0c4de")

# Primera sección: Ingresar datos
table = tk.LabelFrame(frame, text="Datos de la tabla", borderwidth=1, relief="solid")
table.grid(row=0, rowspan=3, column=1, padx=10, pady=10, sticky="news")
table.configure(bg="#fef7d5",font=("Courier", 12, "bold"))

# Etiquetas de la tabla
# Etiqueta X
XLabel = tk.Label(table, text=" X ")
XLabel.grid(row=0, column=0, padx=0, pady=10)
XLabel.configure(bg="#fef7d5",font=("Courier", 12, "bold"), borderwidth=1, relief="solid")
# Etiqueta Y
YLabel = tk.Label(table, text=" Y ")
YLabel.grid(row=0, column=1, padx=0, pady=10)
YLabel.configure(bg="#fef7d5",font=("Courier", 12, "bold"), borderwidth=1, relief="solid")

# Inicializamos la tabla en valores 0
z = range(30)
for n in z:
    # Limpiamos valores en X
    x_label = tk.Label(table, text="")
    x_label.grid(row=1 + n, column=0)
    # Limpiamos valores en Y
    d_label = tk.Label(table, text="")
    d_label.grid(row=1 + n, column=1)

# Pintammos el grafico
graphic = plt.Figure(figsize=(6, 6))
ax = graphic.add_subplot(111)
ax.grid(True), ax.set_xlabel("Eje en X"), ax.set_ylabel("Eje en Y"), ax.set_title("Gráfica")
line = FigureCanvasTkAgg(graphic, second_frame)
line.get_tk_widget().pack(side=tk.LEFT, fill=tk.BOTH, expand=1)

window.mainloop()
