# Variables & Expressions

The ability to use variables within Studio greatly enhances flexibility in configuring interactivity for projects, enabling the creation of complex solutions and systems.



{% hint style="info" %}
This feature is currently in Beta as we actively refine the experience with variables and expressions. Despite ongoing improvements, it is already highly functional and enhances project capabilities significantly.
{% endhint %}



## What are Variables?

Vectary enables to create and manage variables that can be utilized across various Studio settings. These variables represent data elements such as numbers, text, or formulas, which can be created directly within Studio or imported from external sources like Google Sheets. A variable can store a specific value or use expressions to dynamically determine its value based on other parameters.



{% hint style="success" %}
Variables are also available for use in [Slider](../floating-ui/slider.md) and [Input](../floating-ui/input.md)
{% endhint %}



All variables are centralized for easy access and management:

{% embed url="https://screen.studio/share/VKn4z6rw" %}

{% hint style="info" %}
To delete or rename a variable, right-click on its name
{% endhint %}



## Expressions



Expressions provide a dynamic method for calculating parameter values using functions, binary operators, and variables.

This approach facilitates the creation of procedural effects and enables the implementation of complex solutions.

Most input fields in the UI support expressions (a detailed list can be found [here](list-of-inputs.md)), allowing for real-time modification of various settings, parameters, and text.



## Learn more

<table data-card-size="large" data-view="cards" data-full-width="false"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><strong>Syntax</strong></td><td><a href="syntax.md">syntax.md</a></td><td><a href="../../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td></tr><tr><td><strong>Functions</strong></td><td><a href="functions.md">functions.md</a></td><td><a href="../../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td></tr><tr><td><strong>List of inputs</strong></td><td><a href="list-of-inputs.md">list-of-inputs.md</a></td><td><a href="../../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td></tr><tr><td><strong>Data import (.csv)</strong></td><td><a href="data-import-.csv.md">data-import-.csv.md</a></td><td><a href="../../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td></tr></tbody></table>



## Example



Let's consider a simple example using **Variables** and **Expressions**.

**Task:** create a configuration that allows parametric changes to the length and width of the tabletop.<br>

{% stepper %}
{% step %}
Create a simple table using primitives

<figure><img src="../../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Create variables: **Width** and **Length**

Assign a value of 100 to each as the base size.

<figure><img src="../../../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Assign variables

Assign the created variables to the dimensions along the X and Y axes (replace the value with the variable name)

<div align="left"><figure><img src="../../../.gitbook/assets/image (195).png" alt="" width="323"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
Expression setup

To ensure the position of the table legs changes synchronously with the table dimensions, an **expression** using the **variable** must be assigned for the position value of each leg:

<table><thead><tr><th width="116.578125">Object</th><th width="137.34765625">X</th><th width="143.63671875">Y</th></tr></thead><tbody><tr><td>Leg 1</td><td><code>-width/2+5</code></td><td><code>-length/2+5</code></td></tr><tr><td>Leg 2</td><td><code>-width/2+5</code></td><td><code>length/2-5</code></td></tr><tr><td>Leg 3</td><td><code>width/2+5</code></td><td><code>length/2+5</code></td></tr><tr><td>Leg 4</td><td><code>width/2-5</code></td><td><code>-length/2+5</code></td></tr></tbody></table>

<figure><img src="../../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Add the **Floating UI**

Add the **Floating UI** to the scene and create a **Text** element along with a **Slider** element. The Text element will dynamically display the table size, while the **Slider** will be used to adjust the size.

<figure><img src="../../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Setup **Text** element

Setup the **Text** element using an expression so that the table size is dynamically displayed based on the size selected by the end user.\
\
Use the following expression: "Width `${width}` "

<div align="left"><figure><img src="../../../.gitbook/assets/image (198).png" alt="" width="238"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
Setup the **Slider**

Setup the **Slider** element to allow the end user to adjust the dimensions of the table

Specify the variable **Width**, set the **Range** and **Step**:

<figure><img src="../../../.gitbook/assets/image (199).png" alt="" width="244"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Repeat steps 6 and 7 for the length

**Done!** The Preview mode can now be activated to check the result:

{% embed url="https://screen.studio/share/rZf6zWna" %}
{% endstep %}
{% endstepper %}



