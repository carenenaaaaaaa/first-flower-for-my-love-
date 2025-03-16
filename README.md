# first-flower-for-my-love-```
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.animation as animation

Fungsi untuk menggambar bunga
def draw_flower(frame):
    ax.clear()
    theta = np.linspace(0, 2*np.pi, 100)
    r = np.exp(np.sin(theta*frame/10))
    x = r * np.cos(theta)
    y = r * np.sin(theta)
    ax.plot(x, y, color='pink')
    ax.set_xlim(-2, 2)
    ax.set_ylim(-2, 2)
    ax.set_aspect('equal')

Membuat figura dan axis
fig, ax = plt.subplots()

Membuat animasi
ani = animation.FuncAnimation(fig, draw_flower, frames=range(100), interval=50)

plt.show()
```
