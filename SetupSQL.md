import sqlite3
import tkinter as tk
from tkinter import messagebox
 
# Connect to the database
conn = sqlite3.connect("test.db")
cursor = conn.cursor()
 
# Ensure the users table exists
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    age INTEGER,
    email TEXT
)
""")
conn.commit()
 
