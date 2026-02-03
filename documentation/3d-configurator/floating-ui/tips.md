# Tips

## How to make a r**esponsive** UI



Adaptive UI is implemented by creating multiple versions of the interface (e.g., desktop, mobile) and using interactions to determine which one should be displayed based on screen size.<br>

{% stepper %}
{% step %}
#### Desktop and mobile UIs

Create two separate UI versions: one for desktop and one for mobile.
{% endstep %}

{% step %}
#### Interactions

Set up interactions that detect screen size and control the visibility of the appropriate UI:\
\
\- **trigger**: `On update`\
\- **condition**: `Breakpoint`\
\- **action 1**: Show the relevant UI\
\- **action 2**: Hide the other UI<br>
{% endstep %}
{% endstepper %}

{% embed url="https://youtu.be/psm6GT3sWBg?si=FIHH1ZishXP0py2v" %}



## How to link Floating UI with a Hotspot or any other object



Floating UI can be positioned not only relative to the canvas, but also relative to any object - such as hotspots, 3D objects, or even the pointer. This behavior is controlled in the **Visibility** action settings. When selecting a Floating UI, use the **Relative to** option to define the reference point.

To adjust the corner and offset from that point, use the **Offset** and **Position** settings within the Floating UI configuration (Design mode).

<figure><img src="../../../.gitbook/assets/image (74).png" alt="" width="563"><figcaption></figcaption></figure>

{% embed url="https://youtu.be/7EjESmzHzok" %}



## How to switch Floating UI using Variants



Floating UI can be used within Variants by placing it into a group.

<div align="left"><figure><img src="../../../.gitbook/assets/image (75).png" alt="" width="363"><figcaption></figcaption></figure></div>





