import tkinter as tk
import random
import webbrowser

def generate_random_number():
    number = random.randint(1, 100)
    label.config(text=f"на те: {number}")

def open_website():
    webbrowser.open("https://learn.algoritmika.org/login")

window = tk.Tk()
window.title("рандомайзер")
window.geometry("300x250")

# Генерация случайных значений для RGB фона
red = random.randint(0, 255)
green = random.randint(0, 255)
blue = random.randint(0, 255)
rgb_color = f'#{red:02x}{green:02x}{blue:02x}'

window.configure(bg=rgb_color)  # Установка RGB фона окна

button_random = tk.Button(window, text="Жмай", command=generate_random_number)
button_random.pack(pady=10)

label = tk.Label(window, text="Нажмите кнопку для генерации числа")
label.pack()

link_label = tk.Label(window, text="Перейти на сайт", fg="blue", cursor="hand2")
link_label.pack(pady=5)
link_label.bind("<Button-1>", lambda e: open_website())

window.mainloop()
это был рандомайзер ес че
