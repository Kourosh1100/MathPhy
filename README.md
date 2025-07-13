# MathPhy
from tkinter import *
from tkinter import ttk
from tkinter import messagebox as m
from math import pi
import math as ma
import time
from fractions import Fraction as f


num2 = 2

his = []

root = Tk()
root.title("Math & Phyzics")
root.geometry("700x500")
root.resizable(False,False)
root.option_add("*tearoff" , False)

label = Label(root, font=("G2 Rubber Stamp LET", 13, 'bold'), bg="#f2e750", fg="#363529", bd=5) 
label.place(x = 0 , y = 0)
label2 = Label(root, font=("G2 Rubber Stamp LET", 13, 'bold'), bg="#f2e750", fg="#363529", bd=5) 
label2.place(x = 583 , y = 0)

def digital_clock():
    time_live = time.strftime("%H:%M:%S")
    tm = time.strftime("%Y/%m/%d")
    label.config(text=time_live)
    label2.config(text=tm) 
    label.after(200, digital_clock)
      
digital_clock()


def dogh():
    global fisa
    
    
def hist():
    global his
    pot = (txt1.get())
    
    his.append(pot)
    print(his)

def btnClick(n):
        global main
        global txt1
        
        main = main + str(n)
        txt1.set(main)
def btnClearDisplay():
        global txt1
        global main
        global his
        main = ""
        txt1.set("")

def btnEqualsInput():
        global main
        global txt1
        sumup = str(eval(main))
        txt1.set(sumup)
        main=""
        global his
        pot = (txt1.get())
        his.append(pot)


main=""
txt1 = IntVar()
# txtDisplay = Entry(root, font=('Times New Romans', 15 , 'bold'), textvariable=txt1, bd=4, insertwidth=4, bg='powder blue', justify='right').place(x = 100 , y = 300)
btn7 = Button(root, padx=6, pady=6, bd=4,relief = "flat", fg='white', font=('arial', 20, 'bold'), text='7' , command = lambda:btnClick(7) , bg = "black").place(x = 260, y = 400)
btn8 = Button(root, padx=6, pady=6, bd=4, relief = "flat",fg='white', font=('arial', 20, 'bold'), text='8' , command = lambda:btnClick(8) , bg = "black").place(x = 320, y = 400)
btn9 = Button(root, padx=6, pady=6, bd=4,relief = "flat", fg='white', font=('arial', 20, 'bold'),text='9' ,command = lambda:btnClick(9) , bg = "black").place(x = 380, y = 400)
addition = Button(root, padx=6, pady=6, relief = "flat",bd=4, fg='white', font=('arial', 20, 'bold'), text='+' , command = lambda:btnClick('+') , bg = "black").place(x = 500, y = 250)                                 
btndat = Button(root, padx=9, pady=6, relief = "flat",bd=4, fg='white', font=('arial', 20, 'bold'), text='.' , command = lambda:btnClick(".") , bg = "black").place(x = 200, y = 325)
btnp = Button(root, padx=6, pady=7,relief = "flat", bd=4, fg='white', font=('arial', 19, 'bold'), text='Л' , command = lambda:btnClick(pi) , bg = "black").place(x = 200, y = 400)
btn4 = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'), text='4' , command = lambda:btnClick(4) , bg = "black").place(x = 260, y = 325)       
btn5 = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'), text='5' , command = lambda:btnClick(5) , bg = "black").place(x = 320, y = 325)  
btn6 = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold') , text='6' , command = lambda:btnClick(6) , bg = "black").place(x = 380, y = 325)
negative = Button(root , padx=9, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold') , text='-' , command = lambda:btnClick('-') , bg = "black").place(x = 500, y = 325)
btn1 = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'),text='1' , command = lambda:btnClick(1) , bg = "black").place(x = 260, y = 250)
btn2 = Button(root, padx=6, pady=6, relief = "flat",bd=4, fg='white', font=('arial', 20, 'bold'),text='2' , command = lambda:btnClick(2) , bg = "black").place(x = 320, y = 250)
btn3 = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'),text='3' , command = lambda:btnClick(3) , bg = "black").place(x = 380, y = 250)
multiply = Button(root, padx=6, pady=6, relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'),text='×' , command = lambda:btnClick('*') , bg = "black").place(x = 440, y = 250)         
btn0 = Button(root, padx=6 , pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'), text='0' , command = lambda:btnClick(0) , bg = "black").place(x = 200 , y = 250)
btnClear = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'), text='c' , command = btnClearDisplay , bg = "black").place(x = 500, y = 400)
btnEquals = Button(root, padx=6, pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'), text='=' , command=btnEqualsInput , bg = "black").place(x = 440, y = 400)
division = Button(root, padx=6 , pady=6,relief = "flat", bd=4, fg='white', font=('arial', 20, 'bold'), text='÷' , command = lambda:btnClick('/') , bg = "black").place(x = 440, y = 325)
poru = Button(root, padx=6 , pady=6, relief = "flat",bd=4, fg='white', font=('arial', 20, 'bold'), text='^' , command = lambda:btnClick('**') , bg = "black").place(x = 560, y = 250)
poruu = Button(root, padx=6 , pady=6, relief = "flat",bd=4, fg='white', font=('arial', 20, 'bold'), text='√' , command = lambda:btnClick(f"**(1/2)") , bg = "black").place(x = 560, y = 325)
poruu = Button(root , padx= 4 ,pady=20,relief = "flat", bd=4, fg='white', font=('arial', 10, 'bold'), text='(' , command = lambda:btnClick("(") , bg = "black").place(x = 560, y = 400)
poruu = Button(root , padx= 4 ,pady=20, relief = "flat",bd=4, fg='white', font=('arial', 10, 'bold'), text=')' , command = lambda:btnClick(")") , bg = "black").place(x = 588, y = 400)
fogo = Label(root ,pady =20 ,relief = "flat",  text = "@Kourosh._.smile ™" , font =("B Homa" , 9) , bg = 'red' , fg='white',)
fogo.place(x = 20 , y =  428)


# def matn():
    
#     cwd = os.getcwd()
#     file = open("new.txt" , "w")
#     file.write("")
#     file.close()
#     m.showinfo("News!" , f"Check your files on {cwd}")
def bd1():
    try:
        if (v1.get() == True) and (v2.get() == False) and (v3.get() == False):
           n = txt1.get()
           fr = 2 ** n
           his.append(fr)
           lbd1 = Label(root ,
                        text = f"مجموعه {fr} عضو دارد" ,
                        fg = "red",
                        font = ("B Homa" , 12))
           lbd1.place(x = 480 , y = 180)
       
        elif (v1.get() == False) and (v2.get() == True) and (v3.get() == False):

            ns1 = txt1.get()
            ns2 = txt2.get()
            yt = (pow(ns1 , 2)) + (pow(ns2 , 2))
            gh = ma.sqrt(yt)
            his.append(gh)
            Label(root ,
                  text = f"{gh}وتر:" ,
                  fg = "red",
                  font = ("B Homa" , 13)).place(x = 500 , y = 180)
        
        elif(v1.get() == False) and (v2.get() == False) and (v3.get() == True):
           l = txt1.get()
           t = txt2.get()
           s = l/t
           his.append(s)
           Label(root ,
                  text = f"{s:,} m/s" ,
                  fg = "red",
                  font = ("B Homa" , 13)).place(x = 500 , y = 180)
           
        elif fisa.get() == True:
            ns1 = txt1.get()
            ns2 = txt2.get()
            yt = (pow(ns1 , 2)) + (pow(ns2 , 2))
            gh = ma.sqrt(yt)
            his.append(gh)
            Label(root ,
                  text = f"{gh}وتر:" ,
                  fg = "red",
                  font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif a.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s^2" ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif F.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} N" ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif W.get() == True:
            l = txt1.get()
            s = l*9.8
            his.append(s)
            Label(root ,
                   text = f"{s:,} N" ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mazi.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"A = {s:,} " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif gash.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} N.m " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif kar.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} J " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif pas.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} pa " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif sayal.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t*9.8
            his.append(s)
            Label(root ,
                   text = f"{s:,} pa " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm1.get() == True:
            l = txt1.get()
            s = ((((l**3)*4)/3)*pi)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm2.get() == True:
            l = txt1.get()
            s = 4*(l**2)*pi
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^2 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm3.get() == True:
            l = txt1.get()
            s = ((((l**3)*2)/3)*pi)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
            
            
        elif hajm4.get() == True:
            l = txt1.get()
            s = 2*(l**2)*pi
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
                    
        elif hajm5.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l**2)/3*pi*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif a2.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s^2 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif vd.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif speed.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm6.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l/3)*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mrb2.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l+t)**2
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mrb3.get() == True:
            l = txt1.get()
            t = txt2.get()
            q = txt3.get()
            s = (l+t+q)**2
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mzj.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l**2)-(t**2)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mst.get() == True:
            l = txt1.get()
            t = txt2.get()
            q = txt3.get()
            s = (l+t)*(l+q)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm7.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm8.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l**2)*pi*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        else:
            m.showerror("Error!" , "اشتباهي در پردازش رخ داده است!")
    
        
    except TclError: 
            pass
    except TypeError:
        m.showerror("Error!" , "ورودي عدد وارد کنيد!")
        

def inf():
    if fisa.get() == True:
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":ضلع اول")
        lb2 = Label(root ,
            text = ":ضلع دوم" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif a.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":F نيرو ")
        lb2 = Label(root ,
            text = ":M جرم" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif F.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":a شتاب ")
        lb2 = Label(root ,
            text = ":M جرم" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif W.get() == True :
        lb1.config(text = ":M جرم ")
        
    elif mazi.get() == True:
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":d1 يا f2")
        lb2 = Label(root ,
            text = ":d2 يا f1" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
        
    elif gash.get() == True or kar.get() == True:
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":d جابجايي يا طول بازو")
        lb2 = Label(root ,
            text = ": F نيرو" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif pas.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":F نيرو ")
        lb2 = Label(root ,
            text = ":A مساحت سطح تماس" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif sayal.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":ῥ چگالي ")
        lb2 = Label(root ,
            text = ":h ارتفاع مايع" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif a2.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":تغييرات سرعت")
        lb2 = Label(root ,
            text = ":S زمان" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif hajm5.get() == True or hajm8.get() == True:
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":r شعاع")
        lb2 = Label(root ,
            text = ":h ارتفاع" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif vd.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":d جابجايي")
        lb2 = Label(root ,
            text = ":S زمان" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif speed.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":L مسافت")
        lb2 = Label(root ,
            text = ":S زمان" ,
            font = ("B Homa" , 14),
            )
        lb2.place(x = 530 , y = 143)
    elif hajm6.get() == True or hajm7.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":S مساحت قاعده")
        lb2 = Label(root ,
            text = ":h ارتفاع" ,
            font = ("B Homa" , 14),)
        lb2.place(x = 530 , y = 143)
    elif mrb2.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":a")
        lb2 = Label(root ,
            text = ":b" ,
            font = ("B Homa" , 14),)
        lb2.place(x = 530 , y = 143)
    elif mrb3.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent3 = Entry(root ,
                     width = 10 ,
                     bg = "brown" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt3 )
        ent3.place(x = 50 , y = 200)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        txt3.set("")
        ent2.bind("<Down>" , lambda event : ent3.focus()  )
        ent3.bind("<Up>" , lambda event : ent2.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        ent3.bind("<Return>" , ali  )
        lb1.config(text = ":a")
        lb2 = Label(root ,
            text = ":b" ,
            font = ("B Homa" , 14),)
        lb2.place(x = 530 , y = 143)
        lb3 = Label(root ,
            text = ":c" ,
            font = ("B Homa" , 14),)
        lb3.place(x = 160 , y = 200)
    elif mzj.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        lb1.config(text = ":a")
        lb2 = Label(root ,
            text = ":b" ,
            font = ("B Homa" , 14),)
        lb2.place(x = 530 , y = 143)
    elif mst.get() == True :
        ent2 = Entry(root ,
                     width = 30 ,
                     bg = "yellow" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt2 )
        ent2.place(x = 200 , y = 150)
        ent3 = Entry(root ,
                     width = 10 ,
                     bg = "brown" ,
                     relief = "flat",
                     font = ("Times New Roman" , 14) ,
                     bd = 5 , textvariable = txt3 )
        ent3.place(x = 50 , y = 200)
        ent2.bind("<Up>" , lambda event : ent.focus()  )
        txt3.set("")
        ent2.bind("<Down>" , lambda event : ent3.focus()  )
        ent3.bind("<Up>" , lambda event : ent2.focus()  )
        ent.bind("<Down>" , lambda event : ent2.focus() )
        ent2.bind("<Return>" , ali  )
        ent3.bind("<Return>" , ali  )
        lb1.config(text = ":a")
        lb2 = Label(root ,
            text = ":b" ,
            font = ("B Homa" , 14),)
        lb2.place(x = 530 , y = 143)
        lb3 = Label(root ,
            text = ":c" ,
            font = ("B Homa" , 14),)
        lb3.place(x = 160 , y = 200)
    elif hajm1.get() == True or hajm2.get() == True or hajm3.get() == True or hajm4.get() == True or hajm6.get() == True:
        lb1.config(text = ":r شعاع ")
    
        

    else:
        m.showerror("Error!" , "Error in choosing!")
        
    
def ali(event):
    try:
        if (v1.get() == True) and (v2.get() == False) and (v3.get() == False):
           n = txt1.get()
           fr = 2 ** n
           his.append(fr)
           lbd1 = Label(root ,
                        text = f"مجموعه {fr} عضو دارد" ,
                        fg = "red",
                        font = ("B Homa" , 12))
           lbd1.place(x = 480 , y = 180)
       
        elif (v1.get() == False) and (v2.get() == True) and (v3.get() == False):

            ns1 = txt1.get()
            ns2 = txt2.get()
            yt = (pow(ns1 , 2)) + (pow(ns2 , 2))
            gh = ma.sqrt(yt)
            his.append(gh)
            Label(root ,
                  text = f"{gh}وتر:" ,
                  fg = "red",
                  font = ("B Homa" , 13)).place(x = 500 , y = 180)
        
        elif(v1.get() == False) and (v2.get() == False) and (v3.get() == True):
           l = txt1.get()
           t = txt2.get()
           s = l/t
           his.append(s)
           Label(root ,
                  text = f"{s:,} m/s" ,
                  fg = "red",
                  font = ("B Homa" , 13)).place(x = 500 , y = 180)
           
        elif fisa.get() == True:
            ns1 = txt1.get()
            ns2 = txt2.get()
            yt = (pow(ns1 , 2)) + (pow(ns2 , 2))
            gh = ma.sqrt(yt)
            his.append(gh)
            Label(root ,
                  text = f"{gh}وتر:" ,
                  fg = "red",
                  font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif a.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s^2" ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif F.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} N" ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif W.get() == True:
            l = txt1.get()
            s = l*9.8
            his.append(s)
            Label(root ,
                   text = f"{s:,} N" ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mazi.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"A = {s:,} " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif gash.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} N.m " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif kar.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} J " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif pas.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} pa " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif sayal.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t*9.8
            his.append(s)
            Label(root ,
                   text = f"{s:,} pa " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm1.get() == True:
            l = txt1.get()
            s = ((((l**3)*4)/3)*pi)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm2.get() == True:
            l = txt1.get()
            s = 4*(l**2)*pi
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^2 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm3.get() == True:
            l = txt1.get()
            s = ((((l**3)*2)/3)*pi)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
            
            
        elif hajm4.get() == True:
            l = txt1.get()
            s = 2*(l**2)*pi
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
                    
        elif hajm5.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l**2)/3*pi*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif a2.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s^2 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif vd.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif speed.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l/t
            his.append(s)
            Label(root ,
                   text = f"{s:,} m/s " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm6.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l/3)*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm^3 " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mrb2.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l+t)**2
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mrb3.get() == True:
            l = txt1.get()
            t = txt2.get()
            q = txt3.get()
            s = (l+t+q)**2
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mzj.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l**2)-(t**2)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif mst.get() == True:
            l = txt1.get()
            t = txt2.get()
            q = txt3.get()
            s = (l+t)*(l+q)
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm7.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = l*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        elif hajm8.get() == True:
            l = txt1.get()
            t = txt2.get()
            s = (l**2)*pi*t
            his.append(s)
            Label(root ,
                   text = f"{s:,} cm " ,
                   fg = "red",
                   font = ("B Homa" , 13)).place(x = 500 , y = 180)
        
    except TclError: 
            pass
    except TypeError:
        m.showerror("Error!" , "ورودي عدد وارد کنيد!")
    
    

    
# img = PhotoImage(master = root , file = "D:\Kourosh\Programing\qmowee.png")
# iml = Label(root , image = img )
# iml.place(x = 20 , y = 100)

info = Button(root ,
              text = "!" ,
              font = ("Baskerville Old Face" , 15) ,
              bg = "blue" ,
              fg = "white" ,
              command = inf,
              relief = "flat",
              activebackground = "red")
info.place(x = 580 , y = 40)


v1 = BooleanVar()
v2 = BooleanVar()
v3 = BooleanVar()
v10 = IntVar()
txt3 = IntVar()
txt1 = IntVar()
txt2 = IntVar()


ent = Entry(root ,
            bg = "pink" ,
            fg = "blue" ,
            bd = 5 ,
            width = 30 ,
            relief = "flat",
            font = ("Times New Roman" , 14),
            textvariable = txt1)
ent.place(x = 200 , y = 100)
ent.bind("<Return>" , bd1)
ent.bind("<Backspace>" , )
ent.focus()
txt1.set("")



txt2.set("")
lb1 = Label(root ,
            text = ":عدد اول" ,
            font = ("B Homa" , 14),
            )
lb1.place(x = 530 , y = 85)

# lb2 = Label(root ,
#             text = ":تعداد زير مجموعه" ,
#             font = ("B Homa" , 8),
#             )
# lb2.place(x = 530 , y = 115)


# cb1 = Checkbutton(root ,
#                  text = "تعداد عضو هاي مجموعه",
#                  bg = "brown",
#                  fg = "orange" ,
#                  relief = "groove" ,
#                  font = ("B Titr" , 10) ,
#                  variable = v1)
# cb1.place(x = 200 , y = 50)


cb2 = Menubutton(root ,
                 text = "فيزيک",
                 bg = "lightblue",
                 fg = "black",
                 activebackground = "gray",
                 relief = "flat" ,
                 font = ("B Titr" , 10) ,
                 padx = 50)
cb2.place(x = 200 , y = 30)
cb2.menu = Menu(cb2 , tearoff = False)
cb2["menu"] = cb2.menu



cb3 = Menubutton(root,
                 text = "رياضي",
                 bg = "red",
                 fg = "black",
                 activebackground = "gray",
                 relief = "flat" ,
                 font = ("B Titr" , 10) ,
                 padx =50
                 )
cb3.place(x = 350 , y = 30 )
cb3.menu = Menu(cb3 , tearoff = False)
cb3["menu"] = cb3.menu



b1 = Button(root ,
            text = "Submit" ,
            bg = "lime" ,
            font = ("Baskerville Old Face" , 15) ,
            padx = 50 ,
            bd = 3 ,
            relief = "flat",
            command = bd1)
b1.place(x = 260 , y = 200)

root_menu = Menu(root)
root.config(menu = root_menu)
hel = Menu(root_menu)
mn2 = Menu(root_menu)
mn3 = Menu(root_menu)
more = Menu(root_menu)
makers = Menu(root_menu)
graph = Menu(root_menu)
forml = Menu(root_menu)


fisa = BooleanVar()
a = BooleanVar()
F = BooleanVar()
W = BooleanVar()
mazi = BooleanVar()
gash = BooleanVar()
kar = BooleanVar()
pas = BooleanVar()
sayal = BooleanVar()
a2 = BooleanVar()
vd = BooleanVar()
speed = BooleanVar()

cb2.menu.add_checkbutton(label = "a = F/m", variable = a , )
cb2.menu.add_checkbutton(label = "F = m.a", variable = F , )
cb2.menu.add_checkbutton(label = "W = mg",variable = W , )
cb2.menu.add_separator()
cb2.menu.add_checkbutton(label = "A = F2/F1", variable = mazi , )
cb2.menu.add_checkbutton(label = "ح = d*f",variable = gash , )
cb2.menu.add_checkbutton(label = "w = d*f",variable = kar ,)
cb2.menu.add_separator()
cb2.menu.add_checkbutton(label = "a = ∆V/∆T",variable = a2)
cb2.menu.add_checkbutton(label = "V = d/∆T",variable = vd)
cb2.menu.add_checkbutton(label = "s = L/∆T",variable = speed)
cb2.menu.add_separator()
cb2.menu.add_checkbutton(label = "P = F/A", variable = pas)
cb2.menu.add_checkbutton(label = "P = ῥgh",variable = sayal)

hajm1 = BooleanVar()
hajm2 = BooleanVar()
hajm3 = BooleanVar()
hajm4 = BooleanVar()
hajm5 = BooleanVar()
hajm6 = BooleanVar()
hajm7 = BooleanVar()
hajm8 = BooleanVar()
mrb2 = BooleanVar()
mrb3 = BooleanVar()
mzj = BooleanVar()
mst = BooleanVar()

cb3.menu.add_checkbutton(label = "(a+b)^2 = a^2 + 2ab + b^2", variable = mrb2)
cb3.menu.add_checkbutton(label = "(a+b+c)^2 = a^2+b^2+c^2+2ab+2ac+2bc",variable = mrb3)
cb3.menu.add_checkbutton(label = "(a+b)(a-b) = a^2 - b^2",variable = mzj)
cb3.menu.add_checkbutton(label = "(a+b)(a+c) = a^2 + a(b+c) + bc",variable = mst)
cb3.menu.add_separator()
cb3.menu.add_checkbutton(label = "V Koreh = 4/3Лr^3", variable = hajm1)
cb3.menu.add_checkbutton(label = "S Koreh = 4Лr^2", variable = hajm2)
cb3.menu.add_checkbutton(label = "V NimKoreh = 2/3Лr^3", variable = hajm3)
cb3.menu.add_checkbutton(label = "S NimKoreh =  2Лr^2",variable = hajm4)
cb3.menu.add_checkbutton(label = "V Makhrout = 1/3Лr^2h", variable = hajm5)
cb3.menu.add_checkbutton(label = "V Heram = 1/3sh", variable = hajm6)
cb3.menu.add_checkbutton(label = "V Manshour = sh",variable = hajm7)
cb3.menu.add_checkbutton(label = "V Ostovaneh = Лr^2h ",variable = hajm8)
cb3.menu.add_separator()
cb3.menu.add_checkbutton(label = "a^2+B^2 = فيثاغورس", variable = fisa)
cb3.menu.add_checkbutton(label = "2^n = زيرمجموعه ها" , )

# forml.add_cascade(menu = cb2 , label = "فيزيک")
# forml.add_cascade(menu = cb3 , label = "رياضي")

# cb3.add_cascade(menu = tehad , label = "ااتحاد ها")
# cb3.c(menu = haj , label = "حجم")
# cb3.add_cascade(menu = bagh , label = "ادامه")
# cb2.add_cascade(menu = speed , label = "سرعت و شتاب")
# cb2.add_cascade(menu = niro , label = "نيرو")
# cb2.add_cascade(menu = feshar , label = "فشار")
# cb2.add_cascade(menu = gasht , label = "گشتاور")


# 
# 
# 


# # gasht.add_checkbutton(label = "d1*f1 = d2*f2",variable = tad , command = bd1)

root_menu.add_cascade(menu = mn2 , label = "About Us")
root_menu.add_command(label = "History" , command = lambda:m.showinfo("History" , f"{his}"))
mn2.add_cascade(menu = makers , label = "Makers")
makers.add_command(label = "Kourosh Naseri")
# root_menu.add_cascade(menu = forml , label = "Formols")

root_menu.add_cascade(menu = mn3 , label = "Them")
mn3.add_command(label = "White" , command = lambda:root.config(bg = "white"))
mn3.add_command(label = "Light Blue" , command = lambda:root.config(bg = "lightblue"))
mn3.add_command(label = "Red" , command = lambda:root.config(bg = "red"))
mn3.add_command(label = "Black" , command = lambda:root.config(bg = "black"))
mn3.add_command(label = "Yellow" , command = lambda:root.config(bg = "yellow"))
mn3.add_command(label = "Green" , command = lambda:root.config(bg = "green"))
mn2.add_cascade(label = "Graphics" , menu = graph)
graph.add_command(label = "Kourosh Naseri")
mn2.add_cascade(menu = more , label = "More")
more.add_command(label = "Settings" ,)

root_menu.add_command(label = "Reset" , command = lambda : root.destroy())
root_menu.add_cascade(label = "Help" ,menu = hel )
hel.add_command(label = "^ = توان")
hel.add_command(label = "C = پاکسازي")
hel.add_command(label = "** = توان")
hel.add_command(label = "/ = تقسيم")
hel.add_command(label = "! = گسترش مراحل")

root.mainloop()
