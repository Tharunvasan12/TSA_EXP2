## Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
## Name:Tharunish vasan T
## Register number:212224240174
## Dataset:Airpassengers.csv
## Software used:Jupiter Lab
## Date:31/10/2026
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:
```
A - LINEAR TREND ESTIMATION
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from tkinter import Tk, filedialog
root = Tk()
root.withdraw()
root.attributes('-topmost', True)
file_path = filedialog.askopenfilename(
    title="Select AirPassengers CSV File",
    filetypes=[("CSV Files", "*.csv")]
)
root.destroy()
df = pd.read_csv(file_path)
x = np.arange(len(df))
y = df['#Passengers'].values
coeff = np.polyfit(x, y, 1)
trend = np.polyval(coeff, x)
print("Linear Trend Values:")
print(trend)
plt.scatter(x, y, label="Original Data")
plt.plot(x, trend, color='red', label="Linear Trend")
plt.xlabel("Months")
plt.ylabel("Number of Passengers")
plt.title("Linear Trend Estimation")
plt.legend()
plt.show()



B- POLYNOMIAL TREND ESTIMATION
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from tkinter import Tk, filedialog
root = Tk()
root.withdraw()
root.attributes('-topmost', True)
file_path = filedialog.askopenfilename(
    title="Select AirPassengers CSV File",
    filetypes=[("CSV Files", "*.csv")]
)
root.destroy()
df = pd.read_csv(file_path)
x = np.arange(len(df))
y = df['#Passengers'].values
coeff = np.polyfit(x, y, 2)
trend = np.polyval(coeff, x)
print("Polynomial Trend Values:")
print(trend)
plt.scatter(x, y, label="Original Data")
plt.plot(x, trend, color='red', label="Polynomial Trend")
plt.xlabel("Months")
plt.ylabel("Number of Passengers")
plt.title("Polynomial Trend Estimation")
plt.legend()
plt.show()
```
### OUTPUT
A - LINEAR TREND 


<img width="630" height="407" alt="image_8" src="https://github.com/user-attachments/assets/839b30f9-167e-4377-ae1a-2afd6b20af0d" />

B- POLYNOMIAL TREND ESTIMATION


<img width="771" height="402" alt="image_9" src="https://github.com/user-attachments/assets/c73ba8c7-8f1d-4025-bff0-bcf263d09cd0" />

### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
