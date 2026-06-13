# python_calculator
#a  calculator built with python
from tkinter import *
root=Tk()
root.title('caculatur')

def btn_click(number):
    global operator
    operator=operator+str(number)
    text_input.set(operator)


def btn_clear():
    global operator
    operator=' '
    text_input.set(operator)
def btn_answer():
    global operator
    sumup=str(eval(operator))
    text_input.set(sumup)
    operator=' '

def btn_backspace():
    global operator
    operator= operator[:-1]
    text_input.set(operator)


operator=' '
text_input=StringVar()
cut=Entry(root,font=('arial',20,'bold'),textvariable=text_input,bd=30,fg='blue').grid(columnspan=500)










#number button 123...1
btn_1=Button(root,padx=16,pady=16,bd=9,fg='blue',bg='red',font=('arial',20,'bold'),text='1',command=lambda:btn_click(1))
btn_2=Button(root,padx=16,pady=16,bd=9,fg='blue',bg='red',font=('arial',20,'bold'),text='2',command=lambda:btn_click(2))
btn_3=Button(root,padx=16,pady=16,bd=9,fg='blue',bg='red',font=('arial',20,'bold'),text='3',command=lambda:btn_click(3))
btn_4=Button(root,padx=16,pady=16,bd=9,fg='yellow',bg='white',font=('arial',20,'bold'),text='4',command=lambda:btn_click(4))
btn_5=Button(root,padx=16,pady=16,bd=9,fg='yellow',bg='white',font=('arial',20,'bold'),text='5',command=lambda:btn_click(5))
btn_6=Button(root,padx=16,pady=16,bd=9,fg='yellow',bg='white',font=('arial',20,'bold'),text='6',command=lambda:btn_click(6))
btn_7=Button(root,padx=16,pady=16,bd=9,fg='orange',bg='pink',font=('arial',20,'bold'),text='7',command=lambda:btn_click(7))
btn_8=Button(root,padx=16,pady=16,bd=9,fg='orange',bg='pink',font=('arial',20,'bold'),text='8',command=lambda:btn_click(8))
btn_9=Button(root,padx=16,pady=16,bd=9,fg='orange',bg='pink',font=('arial',20,'bold'),text='9',command=lambda:btn_click(9))
btn_0=Button(root,padx=16,pady=16,bd=9,fg='black',bg='green',font=('arial',20,'bold'),text='0',command=lambda:btn_click(0))


#operator button+-....
btn_add=Button(root,padx=16,pady=16,bd=9,fg='orange',bg='pink',font=('arial',20,'bold'),text='+',command=lambda:btn_click('+'))
btn_k=Button(root,padx=16,pady=16,bd=9,fg='white',bg='black',font=('arial',20,'bold'),text='.',command=lambda:btn_click('.'))
btn_minse=Button(root,padx=16,pady=16,bd=9,fg='yellow',bg='white',font=('arial',20,'bold'),text='-',command=lambda:btn_click('-'))
btn_multi=Button(root,padx=16,pady=16,bd=9,fg='blue',bg='red',font=('arial',20,'bold'),text='*',command=lambda:btn_click('*'))
btn_divis=Button(root,padx=16,pady=16,bd=9,fg='black',bg='green',font=('arial',20,'bold'),text='/',command=lambda:btn_click('/'))
btn_equal=Button(root,padx=16,pady=16,bd=9,fg='black',bg='green',font=('arial',20,'bold'),text='=',command=btn_answer)
btn_c=Button(root,padx=16,pady=16,bd=9,fg='black',bg='green',font=('arial',20,'bold'),text='c',command=btn_clear)
btn_backspace=Button(root,padx=16,pady=16,bd=9,fg='white',bg='black',font=('arial',20,'bold'),text='⬅ ',command=btn_backspace)
#addrass part
btn_0.grid(row=1,column=0)
btn_c.grid(row=1,column=1,sticky="nsew")
btn_equal.grid(row=1,column=2)
btn_divis.grid(row=1,column=3,sticky="nsew")

btn_1.grid(row=2,column=0)
btn_2.grid(row=2,column=1,sticky="nsew")
btn_3.grid(row=2,column=2)
btn_multi.grid(row=2,column=3,sticky="nsew")

btn_4.grid(row=3,column=0)
btn_5.grid(row=3,column=1,sticky="nsew")
btn_6.grid(row=3,column=2)
btn_minse.grid(row=3,column=3)


btn_7.grid(row=4,column=0)
btn_8.grid(row=4,column=1,sticky="nsew")
btn_9.grid(row=4,column=2)
btn_add.grid(row=4,column=3)

btn_k.grid(row=6,column=0,sticky="nsew")
btn_backspace.grid(row=6,column=1)















root.mainloop()
