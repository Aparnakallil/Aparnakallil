from tkinter import *
# Creating a GUI Window
window = Tk()
def from_kg():
    gram = float(r2_value.get())*1000
    pound = float(r2_value.get())*2.20462
    ounce = float(r2_value.get())*35.274
    h1.delete("1.0",END)
    h1.insert(END, gram)
    h2.delete("1.0", END)
    h2.insert(END, pound)
    h3.delete("1.0", END)
    h3.insert(END, ounce)

r1 = Label(window, text="Input the weight in KG")
r2_value = StringVar()
r2 = Entry(window, textvariable=r2_value)
r3 = Label(window, text="Gram")
r4 = Label(window, text="Pound")
r5 = Label(window, text="Ounce")

h1 = Text(window, height=5, width=30)
h2 = Text(window, height=5, width=30)
h3 = Text(window, height=5, width=30)

n1 = Button(window, text="Convert", command=from_kg)

r1.grid(row=0, column=0)
r2.grid(row=0, column=1)
r3.grid(row=1, column=0)
r4.grid(row=1, column=1)
r5.grid(row=1, column=2)
h1.grid(row=2, column=0)
h2.grid(row=2, column=1)
h3.grid(row=2, column=2)
n1.grid(row=0, column=2)

window.mainloop()
