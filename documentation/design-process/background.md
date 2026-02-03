# Background



The background setting determines how the scene’s backdrop is displayed.



<figure><img src="../../.gitbook/assets/image (282).png" alt="" width="375"><figcaption></figcaption></figure>

* **Transparent** — removes the background, making the scene fully transparent



* **Environment** — uses the HDRI environment ([environment.md](environment.md "mention")) as the background, blending the lighting and reflections with the scene.\
  \
  \- **Ground projection** — modifies the HDRI projection to create a realistic ground surface, ensuring objects appear naturally integrated into the environment. This prevents the floating effect typically seen with spherical HDRI projection and enhances realism by aligning the background and reflections with the scene.\
  \
  \- **Size** — adjusts the projection size to match the scale of the scene\
  \
  \- **Blur** — applies an extreme blur effect, making the HDRI background indistinguishable except for its colors. If background blur is disabled, additional blur adjustments can be made in the environment settings.\
  \
  **- Environment settings** — [#settings](environment.md#settings "mention")



* **Solid** — applies a single, uniform color as the background



* **Linear** — creates a smooth gradient between two colors, providing a soft transition effect



* **Radial** — generates a circular gradient effect, transitioning from one color at the center to another at the edges



* **Texture** — uses an imported image as the background, allowing for custom designs or photographic backdrops.





