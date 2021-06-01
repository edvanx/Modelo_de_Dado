# Programador: Edvan Oliveira Santos
# Criado em: 01/06/2021
# Modificado em: 01/06/2021
# O programa é um simulador de um dado.

import turtle as Tut
import random
from PIL import Image

def main():
    jogar = jogar_dado()
    jogar.ConstruirDado(Tut)
    Tut.Screen().exitonclick()
    
class jogar_dado:
    def __init__(self):
        self.valor_minimo = 1
        self.valor_maximo = 6
        
    def GerarValor(self, valor_minimo, valor_maximo):
        #gerando um valor aleatório no intervalo de 1 a 6
        valor = random.randint(valor_minimo, valor_maximo)
        return valor
        
    def GerarDado(self):
        valor = self.GerarValor(self.valor_minimo, self.valor_maximo)
 
        if valor == 1:
            dado = [[1, 1, 1],
                    [1, 0, 1],
                    [1, 1, 1]]
        elif valor == 2:  
            dado = [[0, 1, 1],
                    [1, 1, 1],
                    [1, 1, 0]]
        elif valor == 3:
            dado = [[0, 1, 1],
                    [1, 0, 1],
                    [1, 1, 0]]
        elif valor == 4:
            dado = [[0, 1, 0],
                    [1, 1, 1],
                    [0, 1, 0]]
        elif valor == 5:
            dado = [[0, 1, 0],
                    [1, 0, 1],
                    [0, 1, 0]]
        else:
            dado = [[0, 1, 0],
                    [0, 1, 0],
                    [0, 1, 0]]
        return dado

    def ConstruirDado(self, t):
        dado = self.GerarDado()
        imgx = 500; imgy = 500
        image = Image.new('RGB', (imgx, imgy))
        pixels = image.load()
        mx = 3; my = 3
        color = [(0, 0, 0), (255, 255, 255)] # RGB cores do dado
        # colorindo o dado
        for ky in range(imgy):
            for kx in range(imgx):
                pixels[kx, ky] = color[dado[my * ky // imgy][mx * kx // imgx]]
        nomearq = 'dado' + '.gif'
        image.save( nomearq, 'GIF')
        t.setup( imgx, imgy )
        t.bgpic( nomearq )
        
if __name__ == '__main__':
    main() 
