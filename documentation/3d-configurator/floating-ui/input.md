# Input



### Overview



The **Input** element adds an editable field to Floating UI that allows end users to enter **text**, **numeric**, or **color** values. The value entered into the Input field updates the [<mark style="color:blue;">variable</mark>](../variables-and-expressions/) specified in the Input settings.

By binding the Input element to a variable, it becomes possible to build interactive user interfaces where scene properties can be modified directly through user-defined values.<br>

<div align="left"><figure><img src="../../../.gitbook/assets/input.gif" alt="" width="316"><figcaption></figcaption></figure></div>



#### How the Input element works



* Input element is configured to target a specific variable
* Any value entered by the end user updates that variable in real time
* All Studio properties that reference the same variable respond immediately to the change



This approach enables flexible configurators where scene behavior and appearance are driven by user input.



### Settings&#x20;



The primary configuration of the Input element consists of selecting an existing variable (variable is type-agnostic) and defining the mode in which the Input operates.

Available Input modes:<br>

* **`Text`** - allows entering a text value
* **`Number`** - allows entering a numeric value
* **`Color`** - allows entering a color value in **HEX** or **RGB** format

All remaining settings of the Input element are purely visual and affect only its appearance in the Floating UI.

<div align="left"><figure><img src="../../../.gitbook/assets/image (544).png" alt="" width="375"><figcaption></figcaption></figure></div>

\
**Number-specific settings**<br>

When **`Number`** mode is selected, additional configuration options become available:<br>

* **Use range** - enables restricting input values to a defined range
* **Range** - defines the minimum and maximum allowed values
* **Step** - sets the increment for value changes (manual input values are automatically rounded according to the defined step)





### Text input example



This example demonstrates how to control a 3D text object using a text Input.

{% embed url="https://screen.studio/share/dKiYFE5D" %}



**Steps:**<br>

* Create a **3D Text** object
* Create a variable in the Variables Manager
* In the 3D text content field, insert the variable using the following syntax:\
  `${variable}`\
  This syntax replaces the displayed text with the value of the variable\
  The variable can also be embedded within text, for example:\
  `Text ${variable} Text`
* Add Floating UI and create an **Input** element
* In the Input settings, select **Text** mode and assign the created variable



**Result: i**n Preview mode, entering text into the Input field updates the text displayed by the 3D Text object.



***



### Number input example



{% embed url="https://screen.studio/share/uhmAY2SI" %}



This example demonstrates how to control a numeric property, such as object scale.

\
**Steps:**<br>

* Create a 3D object, such as a **Box**
* Create a variable in the Variables Manager
* Assign the variable to a numeric property, for example the **Scale X** value of the object
* Add Floating UI and create an **Input** element
* In the Input settings, enable **Number** mode and select the created variable



**Result:** in Preview mode, entering a numeric value into the Input field updates the object scale according to the entered value.



***



### Color input example



For interactive material color control, Floating UI provides a dedicated [<mark style="color:blue;">**Color**</mark>](color.md) element with a color palette.\
The **Input** element can be used alongside the Color element or as an alternative method for color adjustment.

The mechanism follows the same principle as Text and Number modes:



* A variable is selected in the Input settings
* The end user enters a color value in the Input field
* Supported formats, such as **RGB** or **HEX**, are defined in the Input settings



When the same variable is used by both the Color element and the Input element, color changes can be made either visually through the palette or precisely through numeric color values.





