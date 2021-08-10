from tkinter import *
from tkinter import ttk
import datetime
from datetime import date
from tkinter import messagebox


app = Tk()
app.geometry("360x280+300+150")
app.resizable(False, False)
app.configure(background='green')
app.title("Age Detector by: Xiu Wawa")
label = ttk.Label(app, text='                  Age Detector')
label.grid(column=1, row=0, padx=4, pady=4, sticky='snew')
name = ttk.Label(app, text="Name:")
name.grid(column=0, row=1, padx=4, pady=4, sticky='snew')
year = ttk.Label(app, text="Year")
year.grid(column=0, row=2, padx=4, pady=4, sticky='snew')
month = ttk.Label(app, text="Month")
month.grid(column=0, row=3, padx=4, pady=4, sticky='snew')
date = ttk.Label(app, text="Day")
date.grid(column=0, row=4, padx=4, pady=4, sticky='snew')

nameEntry = ttk.Entry(app, width=20)
nameEntry.grid(column=1, row=1, padx=4, pady=4, sticky='snew')
yearEntry = ttk.Entry(app, width=20)
yearEntry.grid(column=1, row=2, padx=4, pady=4, sticky='snew')
monthEntry = ttk.Entry(app, width=20)
monthEntry.grid(column=1, row=3, padx=4, pady=4, sticky='snew')
dateEntry = ttk.Entry(app, width=20)
dateEntry.grid(column=1, row=4, padx=4, pady=4, sticky='snew')

agecal = ttk.Button(app, text="Calculate Age")
agecal.grid(column=1, row=5, padx=4, pady=4, sticky='snew')

app.rowconfigure(0, weight=1)
app.rowconfigure(1, weight=1)
app.rowconfigure(2, weight=1)
app.rowconfigure(3, weight=1)
app.rowconfigure(4, weight=1)
app.rowconfigure(5, weight=1)
app.columnconfigure(0, weight=1)
app.columnconfigure(1, weight=1)

# function
def agecalculator():
    name = nameEntry.get()
    currentdate = datetime.date(datetime.datetime.now().year, datetime.datetime.now().month, datetime.datetime.now().day)
    ymd = datetime.date(int(yearEntry.get()), int(monthEntry.get()), int(dateEntry.get()))
    age =(currentdate - ymd).days/365
    messagebox.showinfo(title="Age", message=f"{name} you are {round(age)} years old!!")
agecal.config(command=agecalculator)

# style
style = ttk.Style()
style.theme_use('clam')
style.configure('TButton', background='pink', forground='blue')
style.map('TButton', background=[('pressed', 'green')])
style.configure('TLabel', font=('Arial', 12))


app.mainloop()
