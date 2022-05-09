
from tkinter import *

gui = Tk()
var1 = DoubleVar()
var2 = DoubleVar()
var3 = DoubleVar()

label = Label(gui, text = 'Temperature Converter', font=('Verdana', 30, 'italic'))
label.pack(side=TOP, pady=10)

label1= Label(gui, text='in Celcius       = ', font=('Verdana', 10))
label1.place(x=50,y=100)

label2= Label(gui, text='in Fahrenheit  = ', font=('Verdana', 10))
label2.place(x=50,y=130)

entry1 = Entry(gui, textvariable=var1)
entry1.place(x=200,y=100)

label3= Label(gui)
label3.place(x=195,y=130)

labeladd1= Label(gui, text='in Kelvin         = ', font=('Verdana', 10))
labeladd1.place(x=50,y=160)

labeladd1= Label(gui)
labeladd1.place(x=195,y=160)

def click1():
    label3.config(text='' +str(var1.get() * 1.8 + 32)+ ' °F')
    labeladd1.config(text=''+str(var1.get() + 273.15)+ ' °K')


button1= Button(gui, text='Convert', command= click1)
button1.place(x=350,y=95)

#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#

label4= Label(gui, text = 'in Fahrenheit  = ', font=('Verdana', 10))
label4.place(x=450,y=100)

label5 = Label(gui, text= 'in Celcius       =', font=('Verdana', 10))
label5.place(x=450, y=130)

label6 = Label(gui)
label6.place(x=595,y=130)

entry2= Entry(gui, textvariable=var2)
entry2.place(x=600,y=100)

labeladd1_1= Label(gui, text='in Kelvin         = ', font=('Verdana', 10))
labeladd1_1.place(x=450,y=160)

labeladd1_1= Label(gui)
labeladd1_1.place(x=595,y=160)

def click2():
    label6.config(text=''+ str((var2.get()-32)/1.8) + ' °C')
    labeladd1_1.config(text='' + str((var2.get()-32) * 5/9 + 273.15) + ' °K')

button2= Button(gui, text= 'Convert',font= ('Verdana', 10), command=click2)
button2.place(x=750,y=95)

#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#^#

label7= Label(gui, text = 'in Kelvin        = ', font=('Verdana', 10))
label7.place(x=850,y=100)

entry3= Entry(gui, textvariable=var3)
entry3.place(x=1000,y=100)

label8 = Label(gui, text= 'in Fahrenheit  =', font=('Verdana', 10))
label8.place(x=850, y=130)

label9 = Label(gui, text= 'in Celcius       =', font=('Verdana', 10))
label9.place(x=850, y=160)

label10= Label(gui)
label10.place(x=995, y=130)

label11= Label(gui)
label11.place(x=995, y=160)

def click3():
    label10.config(text='' + str((var3.get() - 273.15) * 9/5 + 32) +'F')
    label11.config(text='' + str(var3.get() - 273.15) + 'C')

button3= Button(gui, text= 'Convert',font= ('Verdana', 10), command=click3)
button3.place(x=1150,y=90)

gui.geometry('1280x300')
gui.title("Temperature Converter")
gui.mainloop()
