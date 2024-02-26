import tkinter as tk
import requests

def drag(event):
    x, y = event.x_root, event.y_root
    root.geometry(f"+{x - x_offset}+{y - y_offset}")

def start_drag(event):
    global x_offset, y_offset
    x_offset, y_offset = event.x, event.y

def close_window():
    root.destroy()

def minimize_window():
    root.iconify()

def drag_label(event):
    x, y = event.x_root, event.y_root
    root.geometry(f"+{x - x_offset}+{y - y_offset}")

root = tk.Tk()
root.title("Modern DDoS Attack")
root.configure(bg='black')
root.overrideredirect(True)
root.attributes('-topmost', True) # Make the window topmost

title_bar = tk.Frame(root, bg='#3b3b3b', relief='raised', bd=2)
title_bar.pack(fill='x')

title_bar.bind("<B1-Motion>", drag)
title_bar.bind("<Button-1>", start_drag)

close_button = tk.Button(title_bar, text="X", command=close_window, bg='#3b3b3b', fg='red', relief='flat', activebackground='red', activeforeground='white')
close_button.pack(side='right')

minimize_button = tk.Button(title_bar, text="-", command=minimize_window, bg='#3b3b3b', fg='yellow', relief='flat', activebackground='#3b3b3b', activeforeground='white')
minimize_button.pack(side='right')

panel_label = tk.Label(title_bar, text="DDOS Panel By Lucifer", bg='#3b3b3b', fg='yellow', font=("Arial", 12))
panel_label.pack(padx=5, pady=5)

panel_label.bind("<B1-Motion>", drag_label)
panel_label.bind("<Button-1>", start_drag)

frame = tk.Frame(root, bg='black')
frame.pack(padx=20, pady=20)

host_label = tk.Label(frame, text="Host:", bg='black', fg='yellow')
host_label.grid(row=0, column=0, padx=5, pady=5, sticky="e")
host_entry = tk.Entry(frame, bg='black', fg='yellow')
host_entry.grid(row=0, column=1, padx=5, pady=5)

port_label = tk.Label(frame, text="Port:", bg='black', fg='yellow')
port_label.grid(row=1, column=0, padx=5, pady=5, sticky="e")
port_entry = tk.Entry(frame, bg='black', fg='yellow')
port_entry.grid(row=1, column=1, padx=5, pady=5)

time_label = tk.Label(frame, text="Time (seconds):", bg='black', fg='yellow')
time_label.grid(row=2, column=0, padx=5, pady=5, sticky="e")
time_entry = tk.Entry(frame, bg='black', fg='yellow')
time_entry.grid(row=2, column=1, padx=5, pady=5)

method_label = tk.Label(frame, text="Method:", bg='black', fg='yellow')
method_label.grid(row=3, column=0, padx=5, pady=5, sticky="e")
method_entry = tk.Entry(frame, bg='black', fg='yellow')
method_entry.grid(row=3, column=1, padx=5, pady=5)

launch_button = tk.Button(frame, text="Launch Attack", bg='black', fg='yellow')
launch_button.grid(row=4, column=0, columnspan=2, padx=5, pady=5)

status_label = tk.Label(frame, text="", fg="green", bg='black')
status_label.grid(row=5, column=0, columnspan=2, padx=5, pady=5)

root.mainloop()
