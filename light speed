# light-speed
import pygame
import random
import math

pygame.init()
gamescreen = pygame.display.set_mode((900, 900))
pygame.display.set_caption("single paricale")
clock = pygame.time.Clock()
mousePos = (500,500)


    

#parical setup

xpos = []
ypos = []
xVel = []
yVel = []
speed = 2
# create paricals
for i in range(100):
    xpos.append(450)
    ypos.append(450)
    
    velX = random.uniform(-1, 1)
    velY = random.uniform(-1, 1)
    
    magnitude = math.sqrt(velX**2 + velY**2)
    
    if magnitude != 0:
        normalizedVelX = speed * velX / magnitude
        normalizedVelY = speed * velY / magnitude
    else:
        noemalizedVelX = 0
        normalizedVelY = 0
        
    xVel.append(normalizedVelX)
    yVel.append(normalizedVelY)
    

#gameloop
while True:
    clock.tick(60)
    
    for i in range(1):
        if len(xpos) < 10:
            
            velX = random.uniform(-1, 1)
            velY = random.uniform(-1, 1)
            
            magnitude = math.sqrt(velX**2 + velY**2)
            
            
            if magnitude != 0:
                normalizedVelX = 2 * velX / magnitude
                normalizedVelY = 2 * velY / magnitude
            else:
                normalizedVelX = 0
                normalizedVelY = 0
                
                
            xpos.append(450)
            ypos.append(450)
            xVel.append(normalixedVelX)
            yVel.append(normalixedVelY)
    
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            break
  
        if event.type == pygame.MOUSEMOTION:
            mousePos = event.pos
            
    print(mousePos)   
    #phyics
    for i in range(100):
    # update position
        xpos[i] += xVel[i]
        ypos[i] += yVel[i]
    
    #bondary checking
        if xpos[i] < 0 or xpos[i] > 900 or ypos[i] < 0 or ypos [i] > 900:
           xpos[i]=450
           ypos[i]=450
        
        
        
    velX = random.uniform(-1, 1)
    velY = random.uniform(-1, 1)
    
    magnitude = math.sqrt(velX**2 + velY**2)
    
    
    
    if magnitude != 0:
        xVel[i] = speed * velX / magnitude
        yVel[i] = speed * velY / magnitude
    else:
        xVel[i] = 0
        yVel[i] = 0
        
    #render setion
    
    gamescreen.fill((0, 0, 0))
    for i in range(100):
        pygame.draw.circle(gamescreen, (255, 255, 255), (xpos[i], ypos[i]), 5)
    pygame.display.flip()
    
    
    
    
pygame.quit()
