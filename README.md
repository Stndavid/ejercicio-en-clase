EXAMEN HERNECIAS STR
class Familia:

    def __init__(self,padre,madre,hijos=[]):
        self.padre=padre
        self.madre=madre
        self.hijos=hijos

    def __str__(self):
        cadena=self.padre+","+self.madre
        for hi in self.hijos:
            cadena=cadena+","+hi
        return cadena




familia1=Familia("Pablo","Ana",["Pepe","Julio"])
familia2=Familia("Jorge","Carla")
familia3=Familia("Luis","Maria",["marcos"])

print(familia1)
print(familia2)
print(familia3)
CLASE Y OBJETOS CON METOD

class Vehiculo():

    def __init__(self, color, ruedas):
        self.color = color
        self.ruedas = ruedas

    def __str__(self):
        return "Color {}, {} ruedas".format( self.color, self.ruedas )

class Coche(Vehiculo):

    def __init__(self, color, ruedas, velocidad, cilindrada):
        self.color = color
        self.ruedas = ruedas
        self.velocidad = velocidad
        self.cilindrada = cilindrada

    def __str__(self):
        return "color {}, {} km/h, {} ruedas, {} cc".format( self.color, self.velocidad, self.ruedas, self.cilindrada )


coche = Coche("azul", 150, 4, 1200)
print(coche)
 
 
 
 HERNECIA DENTRO DE UNA HERENCIAS
 class Persona:

    def __init__(self):
        self.nombre=input("Ingrese el nombre:")
        self.edad=int(input("Ingrese la edad:"))

    def imprimir(self):
        print("Nombre:",self.nombre)
        print("Edad:",self.edad)


class Empleado(Persona):

    def __init__(self):
        super().__init__()
        self.sueldo=float(input("Ingrese el sueldo:"))

    def imprimir(self):
        super().imprimir()
        print("Sueldo:",self.sueldo)

    def paga_impuestos(self):
        if self.sueldo>1500:
            print("El empleado debe pagar impuestos")
        else:
            print("No paga impuestos")


# bloque principal

persona1=Persona()
persona1.imprimir()
print("____________________________")
empleado1=Empleado()
empleado1.imprimir()
empleado1.paga_impuestos()
