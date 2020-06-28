# tkinter

tkinter is a Python library for dealing with GUI Dekstop Application.

## Installation

default package comes with python


## Executable file building in Python

pip install pyinstaller

pyinstaller --onefile --window  script.py

## Usage

```python
import tkinter

window = Tk()

l1 = Label(window,text="Title")
l1.grid(row=0,column=0)

l1 = Label(window,text="Author")
l1.grid(row=0,column=2)

l1 = Label(window,text="Year")
l1.grid(row=1,column=0)

l1 = Label(window,text="ISBN")
l1.grid(row=1,column=2)

title_text = StringVar()
e1=Entry(window,textvariable = title_text)
e1.grid(row=0, column=1)

author_text = StringVar()
e2=Entry(window,textvariable = author_text)
e2.grid(row=0, column=3)

year_text = StringVar()
e3=Entry(window,textvariable = year_text)
e3.grid(row=1, column=1)

isbn_text = StringVar()
e4=Entry(window,textvariable = isbn_text)
e4.grid(row=1, column=3)

# Listbox

list1= Listbox(window, height = 6, width =35)
list1.grid(row=2,column=0,rowspan=6,columnspan=2)

# scrollbarr
sb1= Scrollbar(window)
sb1.grid(row=2, column=2,rowspan=6)

# list box configure
list1.configure(yscrollcommand=sb1.set)
sb1.configure(command= list1.yview)

# list box bind
list1.bind('<<ListboxSelect>>', get_selected_row)


b1= Button(window, text="View All", width=12,command = view_command)
b1.grid(row=2, column=3)

b2= Button(window, text="Search Entry", width=12, command=search_command)
b2.grid(row=3, column=3)

b3= Button(window, text="Add Entry", width=12, command =add_command)
b3.grid(row=4, column=3)

b4= Button(window, text="Update", width=12,command= update_command)
b4.grid(row=5, column=3)

b5= Button(window, text="Delete", width=12, command= delete_command)
b5.grid(row=6, column=3)

b6= Button(window, text="Close", width=12)
b6.grid(row=7, column=3)




window.mainloop()
```

## Output

![python desktop app](https://user-images.githubusercontent.com/16940235/85951829-9208df80-b987-11ea-8b0e-e949b019bec5.PNG)




## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/Shohanurcsevu/Python-Dektop-App/blob/master/LICENCE)