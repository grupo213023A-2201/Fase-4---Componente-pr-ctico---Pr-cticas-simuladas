# Fase-4---Componente-pr-ctico---Pr-cticas-simuladas
Tare 4 programación 
import tkinter as tk
from tkinter import messagebox
from abc import ABC, abstractmethod
import datetime

# =========================
# LOGS
# =========================
def registrar_log(mensaje):
    with open("logs.txt", "a") as archivo:
        archivo.write(f"{datetime.datetime.now()} - {mensaje}\n")

# =========================
# EXCEPCIONES
# =========================
class ErrorSistema(Exception):
    pass

class ErrorValidacion(ErrorSistema):
    pass

class ErrorReserva(ErrorSistema):
    pass

# =========================
# CLASE ABSTRACTA
# =========================
class Entidad(ABC):
    def __init__(self, id):
        self._id = id

    @abstractmethod
    def mostrar(self):
        pass

# =========================
# CLIENTE
# =========================
