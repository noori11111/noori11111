opencv-python
numpy
pytesseract
sympy
flask
from flask import Flask, render_template, request
import cv2
import numpy as np
import pytesseract
import sympy as sp

app = Flask(__noori__)

@app.route('/')
def home():
    return render_template('index.html')

@app.route('/solve', methods=['POST'])
def solve():
    # كود معالجة الصورة وحل المسألة سيضاف لاحقاً
    pass

if __name__ == '__main__':
    app.run(debug=True)
<!DOCTYPE html>
<html dir="rtl">
<head>
    <title>حل مسائل تحويلات Z</title>
</head>
<body>
    <h1>مرحباً بك في تطبيق حل مسائل تحويلات Z</h1>
    <form action="/solve" method="post" enctype="multipart/form-data">
        <input type="file" name="image" accept="image/*" capture="camera">
        <button type="submit">حل المسألة</button>
    </form>
</body>
</html>

