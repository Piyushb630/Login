
<img width="568" alt="Screenshot 2024-05-23 at 12 50 30 PM" src="https://github.com/Piyushb630/Login/assets/92310553/db80de6a-ce90-4112-95c9-d9c0f5cc91a5">
<img width="612" alt="Screenshot 2024-05-23 at 12 52 06 PM" src="https://github.com/Piyushb630/Login/assets/92310553/212ee701-9e28-4136-8b0b-0e4c4b9b146e">
<img width="612" alt="Screenshot 2024-05-23 at 12 51 32 PM" src="https://github.com/Piyushb630/Login/assets/92310553/987582c1-b386-4614-b06c-d8ab529c0cba">







# Login

#Here is the code


    import customtkinter
    import webbrowser
    import os
    import subprocess

    customtkinter.set_appearance_mode("dark")
    customtkinter.set_default_color_theme("blue")


    valid_username="Admin"
    valid_password="Admin"

    def open_webpage():
    url = "https://seb.collegial.com"
    webbrowser.open_new(url)


    def open_webpage1():
    url = "https://www.google.co.in?"
    webbrowser.open_new(url)
 
    def open_app(): 
    import subprocess 
    subprocess.Popen(["open", "/Applications/netflix.app"])



    def login():
    entered_username = text.get()
    entered_password = text2.get()
    if entered_username == valid_username and entered_password == valid_password:
        window.destroy()

        window1 = customtkinter.CTk()
        window1.geometry("500x600")
        window1.title("EVERYTHING IN ONE PLACE FOR YOU :)")

        frame = customtkinter.CTkFrame(master =window1)
        frame.pack(pady=20, padx=60, fill ="both", expand=True)

        button = customtkinter.CTkButton(master = frame, text = "SEBcampus", command = open_webpage)
        button.pack(pady=12, padx=10)

        button1 = customtkinter.CTkButton(master = frame, text = "Checksheet", command= open_webpage1)
        button1.pack(pady=12, padx=10)

        button2 = customtkinter.CTkButton(master = frame, text = "Calypso", command = open_webpage1)
        button2.pack(pady=12, padx = 10)

        button3 = customtkinter.CTkButton(master = frame, text ="Swift Citrix", command = open_webpage1 )
        button3.pack(pady=12, padx=10)

        button4 = customtkinter.CTkButton(master = frame, text = "Work Instructions", command = open_webpage1)
        button4.pack(pady=12, padx=10)
        


    else:
        window2= customtkinter.CTk()
        window2.geometry("500x200")

        frame = customtkinter.CTkFrame(master =window2)
        frame.pack(pady=20, padx=60, fill ="both", expand=True)

        label = customtkinter.CTkLabel(master = frame, text= "Invalid username or password")
        label.pack()

        Button3 = customtkinter.CTkButton(master = frame, text = "Oops, wanna Retry?", command = retry)
        Button3.pack(pady=12, padx=10)


    def retry():
   
    window.deiconify() 
    
    
          

    window = customtkinter.CTk()
    window.geometry("500x300")
    window.title("EVERYDAY USE APP")

    frame = customtkinter.CTkFrame(master=window)
    frame.pack(pady=20, padx=60, fill="both", expand=True)

    label = customtkinter.CTkLabel(master = frame, text ="Login System")
    label.pack(pady =12, padx= 10)

    text = customtkinter.CTkEntry(master = frame, placeholder_text="Username")
    text.pack(pady =12, padx= 10)

    text2 =customtkinter.CTkEntry(master =frame, placeholder_text="password", show ="*")
    text2.pack(pady =12, padx= 10)

    button = customtkinter.CTkButton(master =frame, text ="login", command=login)
    button.pack(pady=12, padx =10)
           
    window.mainloop()
