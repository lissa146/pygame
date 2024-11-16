# fractial
import pygame
import math
import cmath


WIDTH = 800
HEIGHT = 800

pygame.init()  # initializes Pygame
pygame.display.set_caption("mandelbot")  # sets the window title
screen = pygame.display.set_mode((WIDTH, HEIGHT))  # create game screen
screen.fill((0, 0, 0))  # paint background black

def Mandelbrot(c):
    z = complex(0,0)
    counter = 2
    while abs(z) < 2 and counter<80:
        z=z**2+c
        counter+=1
    return counter
   



t = -2 #lower bound for real axis
while t<2: #upper bound for real (horizontal) axis
    t+=.01#make this number SMALLER to increase picture resolution
   
    m = -2 #lower bound for inaginary numbers
    while m<2: #upper bound for imaginary (verticle) axis
        m+=.01 #make this number SMALLER to increase picture resolution
       
        c = complex(t,m)
        num = Mandelbrot(c);
        if num < 20:
            screen.set_at((int(t*100+400), int(m*100+400)), (num*8, num*6, num*12))
        elif num < 40:
            screen.set_at((int(t*100+400), int(m*100+400)), (num*3, num/2, num*6))
        elif num == 80:
            screen.set_at((int(t*100+400), int(m*100+400)), (255, 255, 255))
        else:
            screen.set_at((int(t*100+400), int(m*100+400)), (num*3, num/2, num*2))
           
        #print("num is ", num, " at ", t*100+400, m*100+400 )
           
        pygame.display.flip()
       
           

pygame.time.wait(10000)
pygame.quit()
