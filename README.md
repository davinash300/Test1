import tkinter as tk
import time

def update_time():
    current_time = time.strftime('%H:%M:%S')  # Get current time in HH:MM:SS format
    label.config(text=current_time)  # Update label text with current time
    label.after(1000, update_time)  # Call this function again after 1 second

# Create the main window
root = tk.Tk()
root.title("Digital Clock")

# Create and place a label to display the time
label = tk.Label(root, font=('Arial', 48), background='black', foreground='white')
label.pack(anchor='center')

# Start the clock
update_time()

# Run the application
root.mainloop()
