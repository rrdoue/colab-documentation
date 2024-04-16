# Module Programming and Testing Using the Google Colab Application

[Google Colab](https://colab.research.google.com/)

## Summary

Experimenting with or developing modules in Colab requires some additional steps beyond entering code into a code cell and then executing the code in your custom module.  The reason for the additional steps is that developing a module requires one to save the python code in a file to a location that Colab's python interpreter can access.  

Assuming you're in a hurry to resolve this so you can continue with a python training class or something, in summary, do the following:

1. Write the code in Colab and test as desired.

2. Copy and paste the module code into a file using any text editor and save the file as `module_name.py`.  Note some text editors may complain about saving the file as a *.py file — they usually use a default `txt` suffix. 

3. Upload the file to the Colab Files location usually displayed in the left-hand pane of the Colab browser window.  Colab calls this location "/content".

Now the file should be available in a location where Colab can access it.  Statements like `import module_name` should now work as expected.  One can confirm the successful import by executing the following commands in a Colab code cell:

`module_name`

or

`dir(module_name)`

which provide some simple information about the module. 

## Workarounds

One user has noticed that uploading a revision of an existing file to Colab's Files location is unreliable.  This affects the Constraints comments below, because the module file is not updated with your changes.  In the event that this occurs, one way to recover from the problem is to select the following in the Colab Header Menu:

1. Runtime > Disconnect and delete runtime, acknowledging the warning by choosing `Yes`.

2. After allowing a few minutes for the new runtime to initialize, upload the file and you should see it in the left-hand pane of files. 

## Constraints

When using Colab, one has to upload the revised module file each time changes are needed.  Then, upload the revised file, import the importlib module, and reload the file using the importlib.reload(module_name) command. 
