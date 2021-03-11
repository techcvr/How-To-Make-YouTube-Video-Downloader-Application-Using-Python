# How-To-Make-YouTube-Video-Downloader-Application-Using-Python

<p>This is just a&nbsp;<strong>two-line</strong>&nbsp;program actually but to explain it in a better way we have used the comments.</p>

<p>So, first, let’s see the two-line code to download any youtube video.</p>

```Python
from pytube import YouTube
YouTube("link").streams.first().download()
```

You can download the pytube module using "pip install pytube" but if this gives you the error then you should try "pip install pytube3" inside your terminal.

```Python
from pytube import YouTube
link = input("Enter the link ")
print("Downloding...")
YouTube(link).streams.first().download()
print("Video downloaded successfully")
```

<h3>Output</h3>

<p>Enter the link - <a href="https://www.youtube.com/watch?v=-oOGRsUPGqw" target="_blank" rel="noreferrer noopener">https://www.youtube.com/watch?v=-oOGRsUPGqw</a><br>Downloding…<br>Video downloaded successfully</p>


# GUI Version
Library installation part is same so no need to discuss again. Lets dive into the code part.

```Python
# importing tkinter
from tkinter import *

# importing YouTube module
from pytube import YouTube

# initializing tkinter
root = Tk()

# setting the geometry of the GUI
root.geometry("400x350")

# setting the title of the GUI
root.title("Youtube video downloader application")

# defining download function
def download():
    # using try and except to execute program without errors
    try:
        myVar.set("Downloading...")
        root.update()
        YouTube(link.get()).streams.first().download()
        link.set("Video downloaded successfully")
    except Exception as e:
        myVar.set("Mistake")
        root.update()
        link.set("Enter correct link")

# created the Label widget to welcome user
Label(root, text="Welcome to youtube\nDownloader Application", font="Consolas 15 bold").pack()

# declaring StringVar type variable
myVar = StringVar()

# setting the default text to myVar
myVar.set("Enter the link below")

# created the Entry widget to ask user to enter the url
Entry(root, textvariable=myVar, width=40).pack(pady=10)

# declaring StringVar type variable
link = StringVar()

# created the Entry widget to get the link
Entry(root, textvariable=link, width=40).pack(pady=10)

# created and called the download function to download video
Button(root, text="Download video", command=download).pack()

# running the mainloop
root.mainloop()
```


<p><strong>Reference </strong>- <a href="https://copyassignment.com/youtube-downloader-application-using-python/" target="_blank" rel="noreferrer noopener">copyassignment.com</a></p>

<p><strong>Note : </strong>This article is for personal record only, whenever i found something useful i share it to my site and the users who use it so i can get the code whenever i want. i dont have to remembers the multiple site for searching same code in future.</p>

