# Creating Python Module Files in the Google Colab Application

[Google Colab](https://colab.research.google.com/)

## Summary

Experimenting with or developing modules in Colab requires some additional steps beyond entering code into a code cell and then executing the code in your custom module.  The reason for the additional steps is that developing a module requires one to save the python code in a file to a location that Colab's python interpreter can access. 

Assuming you're in a hurry to resolve this so you can continue with a python training class or something, follow these steps:

1. Write the module code in a Colab cell and test as desired.

2. In the Colab Files location usually displayed in the lefthand pane of the Colab browser window, right-click and select `New file`.  Save the file as `module_name.py`.  

3. Double-click the file to open it, displaying the file on the righthand side of the browser window.  Copy the module code from the appropriate cell, place the cursor in the new file area that you just opened, and paste the code into the file.  There should be a * by the file name.  Select the file name to save the changes.  

4. Close the file at any time by selecting the X near the file name. 

Now the file should be available in a location where Colab can access it.  Statements like `import module_name` should now work as expected.  One can confirm the successful import by executing the following commands in a Colab code cell:

`module_name`

or

`dir(module_name)`

which provide some simple information about the module. 

## Note

Remember that if you change the file during testing, one has to use the importlib module and its reload function for the changes to take effect. 
