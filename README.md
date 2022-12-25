# pyqt-widget-example
## PyQt GroupableTreeWidget
This repository contains a PyQt5 implementation of a GroupableTreeWidget class that displays data in a tree structure with the ability to group data by a specific column.

### Example usage
Here is an example of how to use the GroupableTreeWidget class:

```python
import sys
from PyQt5 import QtWidgets

# Define example data
COLUMN_NAME_LIST = ["ID", "Name", "Age", "City"]
ID_TO_DATA_DICT = {
    1: {
        "Name": "Alice", 
        "Age": "30", 
        "City": "New York"},
    2: {
        "Name": "Bob", 
        "Age": "25", 
        "City": "Chicago"},
    3: {
        "Name": "Charlie", 
        "Age": "35", 
        "City": "Los Angeles"},
}

# Create the application and tree widget
app = QtWidgets.QApplication(sys.argv)
tree_widget = GroupableTreeWidget(column_name_list=COLUMN_NAME_LIST, 
                         id_to_data_dict=ID_TO_DATA_DICT)

# Show the tree widget
tree_widget.show()

# Run the application
sys.exit(app.exec_())
```
### Features
The GroupableTreeWidget class has the following features:

Ability to set the column names and data to be displayed in the tree widget.
Context menu for the header that allows the user to group the data by a specific column.
Option to expand or collapse all groups.
___

## PyQt ScalableView
The ScalableView class is a PyQt5 widget that extends the QGraphicsView class and provides the ability to scale the contents of the view using the mouse wheel. The ScalableView class takes a parent widget and a widget to be displayed in the view as arguments in its constructor.

### Example usage
Here is an example of how to use the ScalableView class:

```python
import sys
from PyQt5 import QtWidgets

# Create the application and tree widget
app = QtWidgets.QApplication(sys.argv)
tree_widget = GroupableTreeWidget(column_name_list=COLUMN_NAME_LIST, 
                         id_to_data_dict=ID_TO_DATA_DICT)

# Create the scalable view widget and set the tree widget as the widget to be displayed in the view
scalable_view = ScalableView(widget=tree_widget)

# Show the scalable view widget
scalable_view.show()

# Run the application
sys.exit(app.exec_())
```
### Features
The ScalableView class has the following features:

The ability to scale the contents of the view using the mouse wheel while pressing the Ctrl key.
Minimum and maximum zoom levels that can be set to limit the amount of scaling.
The ability to reset the zoom level to the default value (1.0 or no zoom) by pressing "F".
___

## Requirements
The GroupableTreeWidget class requires PyQt5 to be installed. You can install PyQt5 using pip:

```
pip install PyQt5
```
