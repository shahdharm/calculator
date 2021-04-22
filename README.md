# calculator
# from _ast import lambda
from tkinter import *
root = Tk()

# defining title of the project
root.title("simple calculator")
# image insert
root.iconbitmap('don.ico')
e = Entry(root, width=55, borderwidth=10, fg="red", bg="black")
e.grid(row=0, column=0, columnspan=6, padx=12, pady=18)

def button_click(number):
    current = e.get()
    e.delete(0, END)
    e.insert(0, str(current) + str(number))

def button_add():
    first_number = e.get()
    global f_num
    global math
    math = "addition"
    f_num=int(first_number)
    e.delete(0,  END)

def button_sub():
    first_number = e.get()
    global f_num
    global math
    math = "subtraction"
    f_num = int(first_number)
    e.delete(0, END)

def button_mul():
    first_number = e.get()
    global f_num
    global math
    math = "multiplaction"
    f_num = int(first_number)
    e.delete(0, END)

def button_div():
    first_number = e.get()
    global f_num
    global math
    math = "division"
    f_num = int(first_number)
    e.delete(0, END)


def button_equal ():
    second_number = e.get()
    e.delete(0, END)
    if math == "addition":
        e.insert(0, f_num + int(second_number))
    if math == "subtraction":
        e.insert(0, f_num - int(second_number))
    if math == "multiplaction":
        e.insert(0, f_num * int(second_number))
    if math == "division":
        e.insert(0, f_num / int(second_number))

def button_clear():
    e.delete(0, END)


# defining the buttons

button_1 = Button(root, text="1", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(1))
button_2 = Button(root, text="2", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(2))
button_3 = Button(root, text="3", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(3))
button_4 = Button(root, text="4", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(4))
button_5 = Button(root, text="5", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(5))
button_6 = Button(root, text="6", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(6))
button_7 = Button(root, text="7", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(7))
button_8 = Button(root, text="8", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(8))
button_9 = Button(root, text="9", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(9))
button_0 = Button(root, text="0", padx=40, pady=20, bg="blue", fg="white", command=lambda: button_click(0))
button_add = Button(root, text="+", padx=40, pady=20, bg="green", fg="white", command=button_add)
button_sub = Button(root, text="-", padx=40, pady=20, bg="green", fg="white", command=button_sub)
button_mul = Button(root, text="*", padx=40, pady=20, bg="green", fg="white", command=button_mul)
button_div = Button(root, text="/", padx=40, pady=20, bg="green", fg="white", command=button_div)
button_equal = Button(root, text="=", padx=40, pady=20, bg="black", fg="white", command=button_equal)
button_clear = Button(root, text="clear", padx=30, pady=20, bg="red", fg="white", command=button_clear)


# putting button on the screen
button_1.grid(row=3, column=0)
button_2.grid(row=3, column=1)
button_3.grid(row=3, column=2)

button_4.grid(row=2, column=0)
button_5.grid(row=2, column=1)
button_6.grid(row=2, column=2)

button_7.grid(row=1, column=0)
button_8.grid(row=1, column=1)
button_9.grid(row=1, column=2)

button_0.grid(row=4, column=1)
button_add.grid(row=1, column=4)
button_sub.grid(row=2, column=4)
button_mul.grid(row=3, column=4)
button_div.grid(row=4, column=4)
button_equal.grid(row=4, column=2)
button_clear.grid(row=4, column=0)


root.mainloop()
