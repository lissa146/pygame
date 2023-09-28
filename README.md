# pinao
#event queue (bucket that holds stuff that happens in game and passes to one of the sections below)
event = pygame.event.wait()

#update/timer section---------------------------------------    
if mousePos[0] > 0 and mousePos[0] < 100 and mousePos[1] >500:
    key = 1
elif mousePos[0] > 100 and mousePos[0] < 200 and mousePos[1] >500:
    key = 3
elif mousePos[0] > 200 and mousePos[0] < 300 and mousePos[1] >500:
    key = 2
elif mousePos[0] > 300 and mousePos[0] < 400 and mousePos[1] >500:
    key = 4
elif mousePos[0] > 400 and mousePos[0] < 500 and mousePos[1] >500:
    key = 5
elif mousePos[0] > 500 and mousePos[0] < 600 and mousePos[1] >500:
    key = 6
elif mousePos[0] > 600 and mousePos[0] < 700 and mousePos[1] >500:
    key = 7
elif mousePos[0] > 700 and mousePos[0] < 800 and mousePos[1] >500:
    key = 8
#add more keys here!
else:
    key = 0
    
#input section----------------------------------------------
if event.type == pygame.QUIT: #close game window
    break

if event.type == pygame.MOUSEBUTTONDOWN:
    press = True

if event.type == pygame.MOUSEBUTTONUP:
    press = False

if event.type == pygame.MOUSEMOTION:
    mousePos = event.pos


#render section---------------------------------------------

#the keys 
pygame.draw.rect(screen, (255, 255, 255), (0, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (100, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (200, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (300, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (400, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (500, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (600, 500, 100, 300))
pygame.draw.rect(screen, (255, 255, 255), (700, 500, 100, 300))
#key outlines
pygame.draw.rect(screen, (0, 0, 0), (0, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (100, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (200, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (300, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (400, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (500, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (600, 500, 100, 300), 2)
pygame.draw.rect(screen, (0, 0, 0), (700, 500, 100, 300), 2)
#if a key is pressed, highlight in grey and play the sound:
if press == True:
    if key == 0:
        print("no key")
    elif key == 1:
        pygame.mixer.Sound.play(k1)
        pygame.draw.rect(screen, (150,150,150), (0,500,100,300))
    elif key == 3:
        pygame.mixer.Sound.play(k3)
        pygame.draw.rect(screen, (150,150,150), (100,500,100,300))
    elif key == 2:
        pygame.mixer.Sound.play(k2)
        pygame.draw.rect(screen, (150,150,150), (200,500,100,300))
    elif key == 4:
        pygame.mixer.Sound.play(k2)
        pygame.draw.rect(screen, (150,150,150), (300,500,100,300))
    elif key == 5:
        pygame.mixer.Sound.play(k2)
        pygame.draw.rect(screen, (150,150,150), (400,500,100,300))
    elif key == 6:
        pygame.mixer.Sound.play(k2)
        pygame.draw.rect(screen, (150,150,150), (500,500,100,300))
    elif key == 7:
        pygame.mixer.Sound.play(k2)
        pygame.draw.rect(screen, (150,150,150), (600,500,100,300))
    elif key == 8:
        pygame.mixer.Sound.play(k2)
        pygame.draw.rect(screen, (150,150,150), (700,500,100,300))
pygame.display.flip() #always needed at the end of every game loop!
