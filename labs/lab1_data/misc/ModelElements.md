###More about model elements
***
**Tools**: Although you might use only built-in system tools in your models, several other types of tools can be added to any model. For example, you can add a Python script tool or DLL that performs customized functionality.
You can also add models to existing models. A model can be run as a single tool and added to another model if it logically fits in the other model's workflow. If you have several complex processes that you want to simplify to make it easier to decipher your model, you can divide those processes into sub-processes and then add those "sub-models" to other models.
An iterator is a model tool that allows you to loop through something like a geodatabase and perform some type of geoprocessing operation on each feature class.
Finally, some tools can be used only within a model. These tools are known as model-only tools.
***
**Connectors**: The basic data connector will always be used within any model, but the other connectors might be used only in certain circumstances. For example, you can connect a model element to another as an environment setting, such as a current workspace.
Additionally, a precondition connector connects one process to another to show that the former process must be completed before the latter. The second process requires information in its input; the first process creates that information. You can communicate this to the model using a precondition.
Finally, a feedback connector can be used to feed the output of the model back into the first process and modify it again a certain number of times.