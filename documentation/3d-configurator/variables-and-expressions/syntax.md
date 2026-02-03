# Syntax



The syntax for expressions is inspired by JavaScript. While it resembles JavaScript in many ways, it is not a full implementation of the language. Instead, it is a minimalistic subset specifically tailored for defining expressions in this context.

This approach ensures simplicity and ease of use while maintaining the flexibility needed for powerful expressions. Users familiar with JavaScript will find the syntax intuitive, but it's important to note that certain JavaScript features may not be available.



## Data types



<table data-full-width="false"><thead><tr><th width="150.7421875">Type</th><th width="153.875">Input</th><th width="210.20703125">Description</th><th>Example</th></tr></thead><tbody><tr><td>variables</td><td><mark style="color:purple;">variable name</mark></td><td></td><td></td></tr><tr><td>string</td><td><code>"hello”</code> or <code>'hello’</code></td><td></td><td></td></tr><tr><td>number</td><td><code>89</code><br><br><code>6.45</code></td><td>integer<br>float<br></td><td></td></tr><tr><td>boolean</td><td><mark style="color:green;">true</mark><br><br><mark style="color:green;">false</mark></td><td></td><td></td></tr><tr><td>template string</td><td><code>text </code><mark style="color:orange;"><code>${}</code></mark><code> text</code></td><td>Everything is interpreted as a string, except what is inside <mark style="color:orange;"><code>${}</code></mark> it is an embedded expression</td><td>Use this to utilize variables and expressions for a Text element (Floating UI) or 3D text.</td></tr><tr><td>datasets</td><td><code>IDENTIFIER[SELECTOR]</code></td><td>Datasets are referenced using the syntax: <code>IDENTIFIER[SELECTOR]</code></td><td><mark style="color:blue;"><code>Data</code></mark><code>[</code><mark style="color:green;"><code>"A1"</code></mark><code>]</code><br><br>Multidimensional selection is supported for rows and columns:<br><mark style="color:blue;"><code>Data</code></mark><code>[</code><mark style="color:green;"><code>0</code></mark><code>][</code><mark style="color:green;"><code>1</code></mark><code>]</code></td></tr><tr><td>unary expressions</td><td>minus <code>-</code><br>negation<br><code>!</code></td><td></td><td></td></tr></tbody></table>





## Supported data structures



Our expression language supports the following data structures:

**Arrays**

* Arrays can contain elements of mixed types, for example: `[1, 2, "A", "B", true]`
* Colors and vectors are represented as arrays:
  * `[1, 0, 0]` represents the color RGB(255, 0, 0)
  * `[5, 10, 3]` represents a 3D vector, Vector3(5, 10, 3)
* Objects or classes are not used; only arrays are employed to maintain simplicity

**Array Indexing**

* Elements within an array can be accessed using zero-based indexing:
  * Example: `[1, 2, 3, 4, 5, 6][0]` evaluates to `1`
  * Syntax: `[array content][index]`





## Binary operators



<table><thead><tr><th width="212.203125">Name</th><th width="90.0234375">Symbol</th><th width="158.65625">Example</th></tr></thead><tbody><tr><td>add</td><td><mark style="color:green;"><code>+</code></mark></td><td></td></tr><tr><td>subtract</td><td><mark style="color:green;"><code>-</code></mark></td><td></td></tr><tr><td>multiply</td><td><mark style="color:green;"><code>*</code></mark></td><td></td></tr><tr><td>divide</td><td><mark style="color:green;"><code>/</code></mark></td><td></td></tr><tr><td>equals</td><td><mark style="color:green;"><code>==</code></mark></td><td><code>5</code><mark style="color:green;"><code>==</code></mark><code>6</code> (false)</td></tr><tr><td>not equals</td><td><mark style="color:green;"><code>!=</code></mark></td><td><code>5</code><mark style="color:green;"><code>!=</code></mark><code>6</code> (true)</td></tr><tr><td>less than</td><td><mark style="color:green;"><code>&#x3C;</code></mark></td><td></td></tr><tr><td>more than</td><td><mark style="color:green;"><code>></code></mark></td><td></td></tr><tr><td>less than or equal to</td><td><mark style="color:green;"><code>&#x3C;=</code></mark></td><td></td></tr><tr><td>more than or equal to</td><td><mark style="color:green;"><code>=></code></mark></td><td></td></tr><tr><td>AND</td><td><mark style="color:green;"><code>&#x26;&#x26;</code></mark></td><td></td></tr><tr><td>OR</td><td><mark style="color:green;"><code>||</code></mark></td><td></td></tr><tr><td>nullish coalescing</td><td><mark style="color:green;"><code>??</code></mark></td><td></td></tr><tr><td>negation</td><td><mark style="color:green;"><code>!</code></mark></td><td></td></tr><tr><td>mod</td><td><mark style="color:green;"><code>%</code></mark></td><td></td></tr><tr><td>range</td><td><mark style="color:green;"><code>:</code></mark></td><td></td></tr></tbody></table>





### Tips



* **Spaces are ignored** — spaces are ignored in expressions unless they are inside a string or template string.
* **Variable name as text** — typing quotation marks before and after a variable name treats it as regular text rather than referencing the variable.
* **Variable name in the expression** — referencing a variable name in an expression calculates its value like any other number if the variable is of type number.\
  \
  if the value of the variable is 10, than typing position + 100 will output result of 110<br>
*   Colors in UI<br>

    <table data-header-hidden><thead><tr><th width="215.9453125"></th><th width="146.49609375"></th></tr></thead><tbody><tr><td>Regular text or number</td><td><code>Black</code></td></tr><tr><td>Variables</td><td><mark style="color:purple;"><code>Purple</code></mark></td></tr><tr><td>Functions, true/false</td><td><mark style="color:blue;"><code>Blue</code></mark></td></tr><tr><td>Operators</td><td><mark style="color:blue;"><code>Teal</code></mark></td></tr><tr><td>Invalid/incorrect value</td><td><mark style="color:red;"><code>Red</code></mark></td></tr><tr><td>Expression</td><td><mark style="color:yellow;"><code>Yellow</code></mark></td></tr><tr><td>String</td><td><mark style="color:green;"><code>Green</code></mark></td></tr></tbody></table>

