import random
from tkinter import *
from tkinter import ttk

def generator():
    a = int(v.get())
    
    if c1.get() == 1:
        l = 'ABCDEFGHIGKLMNOPQRSTUVYXWZ'
    if c2.get() == 1:
        l = '0123456789'
    if c3.get() == 1:
        l = '<>=-_!@#$%'
    if c1.get() == 1 and c2.get() == 1:
        l = 'ABCDEFGHIGKLMNOPQRSTUVYXWZ0123456789'
    if c1.get() == 1 and c3.get() == 1:
        l = 'ABCDEFGHIGKLMNOPQRSTUVYXWZ<>=-_!@#$%'
    if c2.get() == 1 and c3.get() == 1:
        l = '0123456789<>=-_!@#$%'
    if c1.get() == 1 and c2.get() == 1 and c3.get() == 1:
        l = 'ABCDEFGHIGKLMNOPQRSTUVYXWZ0123456789<>=-_!@#$%'
    
    pas = ''
    for i in range(a):
        pas += random.choice(list(l))
               
    A.delete(0, END)
    A.insert(END, pas)

window = Tk()

window.title('Генератор паролей')

window.geometry('300x200')

window.resizable(width=False, height=False)

btn = Button(window, text='Generation', command=generator, bg='grey')
btn.place(relx = 0.5,y = 150,anchor=CENTER)

c3 = IntVar()
c3_checkbutton = ttk.Checkbutton(window, text='Символы', variable=c3)
c3_checkbutton.place(relx = 0.58,y = 10)

c1 = IntVar()
c1_checkbutton = ttk.Checkbutton(window, text='A-Z', variable=c1)
c1_checkbutton.place(relx = 0.2,y = 10)

c2 = IntVar()
c2_checkbutton = ttk.Checkbutton(window, text='Цифры', variable=c2)
c2_checkbutton.place(relx = 0.35,y = 10)

A = Entry(window)
A.place(relx = 0.25,y = 100)

v = IntVar(value=8)
c4 = Scale(window, from_=8, to=30, length=200, orient=HORIZONTAL, variable=v)
c4.place(relx = 0.5,y = 50, anchor=CENTER)

label = ttk.Label()
label.place(anchor=NW)

window.mainloop()

