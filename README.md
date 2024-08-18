# -import math
from turtle import *

def hearta(t):
    return 15 * math.sin(t)**3

def heartb(t):
    return 12 * math.cos(t) - 5 * math.cos(2 * t) - 2 * math.cos(3 * t) - math.cos(4 * t)

speed(0)  # 0 adalah kecepatan maksimum
bgcolor("black")
penup()
goto(0, 0)
pendown()
color("red")

for i in range(0, 628, 1):  # 628 kira-kira 2π*100, cukup untuk satu putaran
    t = i / 100  # Mengubah rentang i ke dalam rentang t untuk trigonometri
    x = hearta(t) * 20
    y = heartb(t) * 20
    goto(x, y)

hideturtle()
done()
