import Tkinter as tk
import time
root=tk.Tk()
root.title("Traffic Simulation")
canvas = tk.Canvas(root, width=1000, height=400, bg="#FFFFFF")
canvas.pack()
# make roads
road_data = [
  (140,150,200,150,200,150,200,50),
  (250,150,250,50,250,150,374,150,374,150,374,50),
  (424,150,424,50,424,150,542,150,542,150,542,50),
  (592,150,592,50,592,150,674,150,674,150,674,50),
  (724,150,724,50,724,150,850,150),
  (140,200,200,200,200,200,200,300),
  (250,200,250,300,250,200,344,200,344,200,344,300),
  (394,200,394,300,394,200,542,200,542,200,542,300),
  (592,200,592,300,592,200,674,200,674,200,674,300),
  (724,200,724,300,724,200,850,200),
  ]
for t in road_data:
  canvas.create_line(t, width=5)
# color roads
road_color_data = [
  (140,152,850,198),
  (202,50,248,300),
  (376,50,422,152),
  (346,198,392,300),
  (544,52,590,300),
  (676,52,722,300),
  ]
for t in road_color_data:
  canvas.create_rectangle(t, fill="#999999", outline='#999999')
# lines on road
road_lines_data = [
  (140,175,850,175),
  (225,50,225,150,248,150),
  (202,200,248,200),
  (225,200,225,300),
  (399,50,399,150,422,150),
  (346,200,392,200),
  (369,200,369,300),
  (567,50,567,150,590,150),
  (699,50,699,150,722,150),
  (544,200,590,200),
  (567,200,567,300),
  (676,200,722,200),
  (699,200,699,300),
  (200,152,200,175),
  (374,152,374,175),
  (542,152,542,175),
  (674,152,674,175),
  (724,198,724,175),
  (592,198,592,175),
  (394,198,394,175),
  (250,198,250,175),
  ]
for t in road_lines_data:
  canvas.create_line(t, width=5, fill="White")
# create car
class Car(object):
  def __init__(self, a,b,c,d, outline='blue', fill='blue'):
    self.rect = canvas.create_rectangle(a,b,c,d, outline=outline, fill=fill)
    self.speed = (0, 0)
  def move(self):
    canvas.move(self.rect, self.speed[0], self.speed[1])
  def set_speed(self, x, y):
    self.speed = x, y
car1 = Car(20, 155, 40, 170, outline='blue', fill='blue')
car1.set_speed(5, 0)
car2 = Car(20, 180, 40, 195, outline='red', fill = 'red')
car2.set_speed(3, 0)
# move car
for x in range(200):
  time.sleep(0.025)
  car1.move()
  car2.move()
  canvas.update()
root.mainloop()