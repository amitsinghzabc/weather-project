from time import time
import tkinter as tk
from tkinter.constants import VERTICAL
import requests
import matplotlib.pyplot as plt
import tkinter.messagebox as tkMessageBox
from tkinter.ttk import *

def getWeather(canvas):
    city = textField.get()
    api = "http://api.openweathermap.org/data/2.5/forecast?q="+ city +"&appid=1c76db04c204092e1d7e971a8b36cdd5"

    json_data = requests.get(api).json()
    try: 
        condition = json_data['list'][1]['weather'][0]['main']
        temp = int(json_data['list'][1]['main']['temp'] - 273.15)
        min_temp = int(json_data['list'][1]['main']['temp_min'] - 273.15)
        max_temp = int(json_data['list'][1]['main']['temp_max'] - 273.15)
        pressure = json_data['list'][1]['main']['pressure']
        humidity = json_data['list'][1]['main']['humidity']
        wind = json_data['list'][1]['wind']['speed']
        final_info = condition + "\n" + str(temp) + "°C" 
        final_data = "Min Temp: " + str(min_temp) + "°C" + "\n" + "Max Temp: " + str(max_temp) + "°C" +"\n" + "Pressure: " + str(pressure) + "\n" +"Humidity: " + str(humidity) + "\n" +"Wind Speed: " + str(wind)
        basic="Showing Weather report of "+ city +" :"
        
        label1.config(text = basic)
        label2.config(text = final_info)
        label3.config(text = final_data)
    except:
        label1.config(text = "")
        label2.config(text = "")
        label3.config(text = "")
        tkMessageBox.showwarning( "Weather App", "There is an unexpected error. Try:\n1. Checking the city name.\n2. Checking your network connection.")
        

def fdd():
    city = textField.get()
    api = "http://api.openweathermap.org/data/2.5/forecast?q="+ city +"&appid=1c76db04c204092e1d7e971a8b36cdd5"
    json_data = requests.get(api).json()
    
    try:
        condition1 = json_data['list'][1]['weather'][0]['main']
        newWin = tk.Toplevel(canvas)
        newWin.title("5-days Weather reports for "+ city)
        newWin.geometry("1200x800")

        frame= tk.Frame(newWin)
        frame.pack(fill='both', expand= 1)

        newWindow=tk.Canvas(frame)
        newWindow.pack(side='left',fill='both', expand= 1)
    
        frm2= tk.Frame(newWindow)
        newWindow.create_window((360,0), window= frm2, anchor="nw")

        f = ("poppins", 20, "bold")
        f2 =("poppins", 15, "bold")
        label1 = tk.Label(frm2, font=f,justify='left')
        label1.pack()
        label2 = tk.Label(frm2, font=f)
        label2.pack()
        label3 = tk.Label(frm2, font=f2)
        label3.pack()
        label4 = tk.Label(frm2, font=f)
        label4.pack()
        label5 = tk.Label(frm2, font=f2)
        label5.pack()
        label6 = tk.Label(frm2, font=f)
        label6.pack()
        label7 = tk.Label(frm2, font=f2)
        label7.pack()
        label8 = tk.Label(frm2, font=f)
        label8.pack()
        label9 = tk.Label(frm2, font=f2)
        label9.pack()
        label10 = tk.Label(frm2, font=f)
        label10.pack()
        label11 = tk.Label(frm2, font=f2)
        label11.pack()
    
        scrollbar = tk.Scrollbar(frame, orient= VERTICAL, command= newWindow.yview)
        scrollbar.pack( side ='right', fill = 'y')
    
        newWindow.configure(yscrollcommand = scrollbar.set)
        newWindow.bind('<Configure>', lambda e: newWindow.configure(scrollregion = newWindow.bbox("all")))

        
        temp1 = int(json_data['list'][1]['main']['temp'] - 273.15)
        min_temp1 = int(json_data['list'][1]['main']['temp_min'] - 273.15)
        max_temp1 = int(json_data['list'][1]['main']['temp_max'] - 273.15)
        pressure1 = json_data['list'][1]['main']['pressure']
        humidity1 = json_data['list'][1]['main']['humidity']
        wind1 = json_data['list'][1]['wind']['speed']
        final_info1 = condition1 + "\n" + str(temp1) + "°C" 
        final_data1 = "Min Temp: " + str(min_temp1) + "°C" + "\n" + "Max Temp: " + str(max_temp1) + "°C" +"\n" + "Pressure: " + str(pressure1) + "\n" +"Humidity: " + str(humidity1) + "\n" +"Wind Speed: " + str(wind1)
        
        condition2 = json_data['list'][9]['weather'][0]['main']
        temp2 = int(json_data['list'][9]['main']['temp'] - 273.15)
        min_temp2 = int(json_data['list'][9]['main']['temp_min'] -273.15)
        max_temp2 = int(json_data['list'][9]['main']['temp_max'] -273.15)
        pressure2 = json_data['list'][9]['main']['pressure']
        humidity2 = json_data['list'][9]['main']['humidity']
        wind2 = json_data['list'][9]['wind']['speed']
        final_info2 = condition2 + "\n" + str(temp2) + "°C" 
        final_data2 = "Min Temp: " + str(min_temp2) + "°C" + "\n" + "Max Temp: " + str(max_temp2) + "°C" +"\n" + "Pressure: " + str(pressure2) + "\n" +"Humidity: " + str(humidity2) + "\n" +"Wind Speed: " + str(wind2)
        
        condition3 = json_data['list'][17]['weather'][0]['main']
        temp3 = int(json_data['list'][17]['main']['temp'] -273.15)
        min_temp3 = int(json_data['list'][17]['main']['temp_min'] -273.15)
        max_temp3 = int(json_data['list'][17]['main']['temp_max'] -273.15)
        pressure3 = json_data['list'][17]['main']['pressure']
        humidity3 = json_data['list'][17]['main']['humidity']
        wind3 = json_data['list'][17]['wind']['speed']
        final_info3 = condition3 + "\n" + str(temp3) + "°C" 
        final_data3 = "Min Temp: " + str(min_temp3) + "°C" + "\n" + "Max Temp: " + str(max_temp3) + "°C" +"\n" + "Pressure: " + str(pressure3) + "\n" +"Humidity: " + str(humidity3) + "\n" +"Wind Speed: " + str(wind3)
        
        condition4 = json_data['list'][26]['weather'][0]['main']
        temp4 = int(json_data['list'][26]['main']['temp'] -273.15)
        min_temp4 = int(json_data['list'][26]['main']['temp_min'] -273.15)
        max_temp4 = int(json_data['list'][26]['main']['temp_max'] -273.15)
        pressure4 = json_data['list'][26]['main']['pressure']
        humidity4 = json_data['list'][26]['main']['humidity']
        wind4 = json_data['list'][26]['wind']['speed']
        final_info4 = condition4 + "\n" + str(temp4) + "°C" 
        final_data4 = "Min Temp: " + str(min_temp4) + "°C" + "\n" + "Max Temp: " + str(max_temp4) + "°C" +"\n" + "Pressure: " + str(pressure4) + "\n" +"Humidity: " + str(humidity4) + "\n" +"Wind Speed: " + str(wind4)
        
        condition5 = json_data['list'][35]['weather'][0]['main']
        temp5 = int(json_data['list'][35]['main']['temp'] -273.15)
        min_temp5 = int(json_data['list'][35]['main']['temp_min'] -273.15)
        max_temp5 = int(json_data['list'][35]['main']['temp_max'] -273.15)
        pressure5 = json_data['list'][35]['main']['pressure']
        humidity5 = json_data['list'][35]['main']['humidity']
        wind5 = json_data['list'][35]['wind']['speed']
        final_info5 = condition5 + "\n" + str(temp5) + "°C" 
        final_data5 = "Min Temp: " + str(min_temp5) + "°C" + "\n" + "Max Temp: " + str(max_temp5) + "°C" +"\n" + "Pressure: " + str(pressure5) + "\n" +"Humidity: " + str(humidity5) + "\n" +"Wind Speed: " + str(wind5)

        label1.config(text ="5-days Weather reports for "+city+" :")
        label2.config(text ="\nToday\n"+final_info1)
        label3.config(text = final_data1)
        label4.config(text ="\nTommorow\n"+final_info2)
        label5.config(text = final_data2)
        label6.config(text ="\nDay 3\n"+final_info3)
        label7.config(text = final_data3)
        label8.config(text ="\nDay 4\n"+final_info4)
        label9.config(text = final_data4)
        label10.config(text ="\nDay 5\n"+final_info5)
        label11.config(text = final_data5)

    except:
        tkMessageBox.showwarning( "5-days data", "There is an unexpected error. Try:\n1. Checking the city name.\n2. Checking your network connection.")

def grph():
    city = textField.get()
    api = "http://api.openweathermap.org/data/2.5/forecast?q="+ city +"&appid=1c76db04c204092e1d7e971a8b36cdd5"
    json_data = requests.get(api).json()
    try:
        temp1 = int(json_data['list'][0]['main']['temp'] - 273.15)
        time1 = str('6:00 AM')
        temp2 = int(json_data['list'][1]['main']['temp'] - 273.15)
        time2 = str('9:00 AM')
        temp3 = int(json_data['list'][2]['main']['temp'] - 273.15)
        time3 = str('12:00 AM')
        temp4 = int(json_data['list'][3]['main']['temp'] - 273.15)
        time4 = str('3:00 PM')
        temp5 = int(json_data['list'][4]['main']['temp'] - 273.15)
        time5 = str('6:00 PM')
        temp6 = int(json_data['list'][5]['main']['temp'] - 273.15)
        time6 = str('9:00 AM')
        temp7 = int(json_data['list'][6]['main']['temp'] - 273.15)
        time7 = str('12:00 AM')
        temp8 = int(json_data['list'][7]['main']['temp'] - 273.15)
        time8 = str('3:00 AM')
        x=[time1,time2,time3,time4,time5,time6,time7,time8]
        y=[temp1,temp2,temp3,temp4,temp5,temp6,temp7,temp8]
        plt.bar(x,y)
        plt.xlabel('Time')
        plt.ylabel('Temprature in °C')
        plt.title('Weather report graph per 3-hrs\nCity: '+ city)
        plt.show()
    except:
        tkMessageBox.showwarning( "Graph", "There is an unexpected error. Try:\n1. Checking the city name.\n2. Checking your network connection.")

canvas = tk.Tk()
canvas.geometry("1200x800")
canvas.title("Weather App")
f = ("poppins", 15, "bold")
t = ("poppins", 35, "bold")

w = tk.Label(canvas, text="Enter the city name below and press 'Enter' button.", font=("poppins", 35, "bold"))
w.pack(pady = 10)

textField = tk.Entry(canvas, justify='center', width = 20, font = t)
textField.pack(pady = 10)
textField.focus()
textField.bind('<Return>', getWeather)

label1 = tk.Label(canvas, font=t)
label1.pack()
label2 = tk.Label(canvas, font=t)
label2.pack()
label3 = tk.Label(canvas, font=f)
label3.pack()

b = tk.Button(canvas, text ="Get 5-days data", command = fdd, font=f)
b.pack(pady = 10)
b2 = tk.Button(canvas, text ="Get Bar Graph", command = grph, font=f)
b2.pack(pady = 10)
canvas.mainloop()
