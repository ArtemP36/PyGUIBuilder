# PyGUIBuilder - README

## Overview

Welcome to the **PyGUIBuilder**, designed to help you create GUI applications with ease. Whether you are building a simple tool or a complex application, our library provides everything you need.

## Table of Contents

1. [Installation](#installation)
2. [Getting Started](#getting-started)
3. [Features](#features)
4. [Usage](#usage)
   - [Creating a Window](#creating-a-window)
   - [Adding Widgets](#adding-widgets)
   - [Other Functions](#other-functions)
5. [Examples](#examples)
6. [License](#license)
7. [Thanks](#thanks)

## Installation

To install the PyGUIBuilder, use pip:

```bash
pip install PyGUIBuilder
```

## Getting Started

Creating your first GUI application is simple. Here’s a quick example to get you started:

```python
import PyGUIBuilder

# Create the main application window
app = PyGUIBuilder.createWindow("My First App", "icon.ico", 400, 400)

# Create a label widget
label = PyGUIBuilder.createLabel(app, "Hello, World!", 1, 0)

# Run the application
PyGUIBuilder.run()
```

## Features

- **Works on Windows**
- **Ease of use:** The library provides a simple and intuitive interface for creating GUI elements
- **Modern Widgets:** Buttons, labels, text entries.
- **Flexible Layouts:** place widgets by rows and columns for flexible UI design.
- **Event Handling:** Simple and intuitive event handling system.

## Usage

### Creating a Window

To create a main application window, use the CreateWindow function:

```python
import PyGUIBuilder

window = PyGUIBuilder.createWindow("My App", "icon.ico", 400, 400)
```

### Adding Widgets

Widgets are the building blocks of a GUI application. You can add various widgets to your window.

Here's an example of adding a label:
```python
label = PyGUIBuilder.createLabel(window, "Hello, World!", 1, 0)
```
Here's an example of adding a entrybox:
```python
entry = PyGUIBuilder.createEntry(window, "text", 3, 0)
```
Here's an example of adding a button:
```python
def callback():
   print("Button clicked!")

button = PyGUIBuilder.createButton(window, "Click Me!", callback, 2, 0)
```
Here's an example of adding a combobox:
```python
langs = ["1", "2", "3", "4"]
combobox = PyGUIBuilder.createComboBox(window, langs, 1, 0)
```
Here's an example of messagebox:
```python
PyGUIBuilder.showMessageBox("showinfo", "Information", "This is an info message.")
PyGUIBuilder.showMessageBox("showwarning", "Warning", "This is a warning message.")
PyGUIBuilder.showMessageBox("showerror", "Error", "This is an error message.")
PyGUIBuilder.showMessageBox("askquestion", "Question", "Are you sure?")
PyGUIBuilder.showMessageBox("askokcancel", "OK Cancel", "Do you want to continue?")
PyGUIBuilder.showMessageBox("askyesno", "Yes No", "Do you agree?")
PyGUIBuilder.showMessageBox("askretrycancel", "Retry Cancel", "Do you want to retry?")
```
Here's an example of adding a CheckBox:
```python
PyGUIBuilder.createCheckbox(window, "text", 1, 0)
```
### Other Functions:
Clearing text in an entry box:
```python
PyGUIBuilder.clearText(entry)
```
Setting text in an entry box:
```python
PyGUIBuilder.setText(entry, "text")
```
Getting text from an entry box:
```python
PyGUIBuilder.getText(entry)
```
Destroying an element:
```python
PyGUIBuilder.destroyElement(label)
```
Getting selection on Combobox:
```python
print(PyGUIBuilder.getComboBoxSelection(combobox))
```
Getting Checkbox state:
```python
PyGUIBuilder.getCheckbox()
```
Running the application:
```python
PyGUIBuilder.run()
```
## Examples

### Simple Form

```python
import PyGUIBuilder

def on_submit():
    print(f"Name: {PyGUIBuilder.getText(entry_name)}, Age: {PyGUIBuilder.getText(entry_age)}")

app = PyGUIBuilder.createWindow("Simple Form", "icon.ico", 400, 400)

label_name = PyGUIBuilder.createLabel(app, "Name:", 1, 0)

entry_name = PyGUIBuilder.createEntry(app, "", 1, 1)

label_age = PyGUIBuilder.createLabel(app, "Age:", 2, 0)

entry_age = PyGUIBuilder.createEntry(app, "", 2, 1)

submit_button = PyGUIBuilder.createButton(app, "Submit", on_submit, 3, 0)

PyGUIBuilder.run()
```

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Thanks
Thank you for using the PyGUIBuilder! We hope it helps you build amazing applications. If you have any questions or need further assistance, feel free to reach out to our community forums or contact panovartem690@gmail.com.

---
Please keep in mind that there may be bugs and flaws. 
