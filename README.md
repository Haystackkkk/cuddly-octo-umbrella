# cuddly-octo-umbrella
Green Circule

Code:
You need to use python pycharm to execute.

----------------------------------------------------------------------------------------




import pygame
pygame.init()

x=400
y=300
velocity=10

windon = pygame.display.set_mode((800,600))
pygame.display.set_caption("Green Circule")

windon_open = True
while windon_open :
    pygame.time.delay(50)
    for event in pygame.event.get() :
        if event.type == pygame.QUIT:
            windon_open = False

        comands = pygame.key.get_pressed()
        if comands [pygame.K_UP]:
             y+= velocity
        if comands [pygame.K_DOWN]:
             y-= velocity
        if comands [pygame.K_RIGHT]:
             x+= velocity
        if comands [pygame.K_LEFT]:
             x-= velocity
    windon.fill((0,0,0))

    pygame.draw.circle(windon, [0, 200, 30], (x, y), 100)
    pygame.display.update()

pygame.quit()

