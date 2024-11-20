# IoT Log Parser Dashboard

This project is a **Flask-based IoT log parser** that processes log files, extracts meaningful insights, and generates **visualizations** for data analysis.

---

## 📋 Prerequisites
Before setting up the project, ensure the following dependencies are installed:

- **Python 3.x**
- **Flask**
- **pandas**
- **matplotlib**
- **seaborn**

If these are not installed,  you can install them using ```pip```:

```
pip install flask pandas matplotlib seaborn
```

## 🗂 File Structure

```
IoT_Log_Parser_Software_Assessment/
│
├── app.py                # Main Flask application script
├── assignment_prod.log              # Log file to be parsed
├── templates/
│   └── visualization.html # HTML template for displaying visualizations
```

## ⚙️ Setup Instructions
Follow these steps to set up and run the project:
1. Clone or download the repository:

```
git clone https://github.com/your-username/IoT_Log_Parser_Software_Assessment.git
cd IoT-Log-Parser
```

2. Place your log file:  Add your log file to the project directory and ensure the file path matches the parse_log_file() function in app.py.

3. Install dependencies: Use the following command to install all required Python libraries:
```
   pip install flask pandas matplotlib seaborn
```

4. Run the Flask app: Start the application by running:
```
python app.py
```
5. Access the dashboard: Open your browser and navigate to: http://127.0.0.1:5000/  to view the dashboard.

## 🚀 How to Run
Once the app is set up, follow these steps to run the log parser:

1. **Place your log file**:  
   Ensure your log file is placed in the specified location (default: `/yourapp/logs.txt`). You can update the path in the `parse_log_file()` function within the `app.py` file.

2. **Start the Flask application**:  
   Run the following command to start the Flask app:
   ```bash
   python app.py
3. **Open the dashboard**:
   Once the Flask server is running, open your browser and navigate to: http://127.0.0.1:5000/ This will load the log dashboard, displaying the visualizations generated from the log file.


## 📸 Screenshots

Here are some screenshots of the IoT Log Parser dashboard:

### Log Dashboard View

![Screenshot 2024-11-20 170608](https://github.com/user-attachments/assets/511350ef-d97f-4d26-b516-5c3f03b6b00f)

![Screenshot 2024-11-20 170623](https://github.com/user-attachments/assets/4ac6343a-b921-4ddb-9375-bad6c7f91542)

![Screenshot 2024-11-20 170633](https://github.com/user-attachments/assets/8283c532-1f7b-49b1-9a7d-d98e2a8632f1)

### Another View

![Screenshot 2024-11-20 170756](https://github.com/user-attachments/assets/36819ea6-9b3d-4c84-9354-581bdc29c5e6)

![Screenshot 2024-11-20 170716](https://github.com/user-attachments/assets/8b744f9a-290d-47b7-b517-e5ee4472c382)


## ✨ Customization

### 1. **Customizing the Log File Parsing**

You can easily modify the `parse_log_file()` function to process log files with different formats or from various locations. Simply update the following:

- **Log File Path**: Change the path to your log file by adjusting the `log_file_path` variable inside the `parse_log_file()` function.
- **Log Format**: If your log files have a different structure or additional fields, you can adjust the regex patterns used in the function to match your log file format.

#### Example:

```python
def parse_log_file():
    log_file_path = 'path/to/your/logfile.log'  # Update this to the path of your log file
    with open(log_file_path, 'r') as file:
        log_content = file.read()
    # Further customization based on log structure
```

### 2. **Customizing the Plot Generation**

The `create_plot()` function allows you to easily customize the types of plots, their titles, labels, and more. Below are the key customization options:

- **Plot Type**: You can change the plot type (e.g., `bar`, `line`, `pie`, etc.) by adjusting the `plot_func` parameter.
- **Plot Parameters**: Customize various parameters like color, size, title, axis labels, and more by passing them to the `create_plot()` function.

#### Example:
```python
create_plot(
    df['log_count'].plot,   # The plot function (bar plot in this case)
    kind='bar',             # The type of plot (e.g., 'bar', 'line', 'pie')
    color='green',          # Color of the plot
    title="Log Count per Day",  # Title of the plot
    xlabel="Day",           # Label for the x-axis
    ylabel="Count"          # Label for the y-axis
)

```

Feel free to explore the plot types available in libraries like matplotlib and seaborn to further enhance the visualizations!

### 3. **Updating the Log File Path**

To point to a different log file, simply modify the path in the `parse_log_file()` function.

For example:

```python
log_file_path = '/path/to/your/logfile.txt'  # Update with your log file path
```
This flexibility allows you to use this tool with various log formats and log file locations.






  
