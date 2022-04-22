# Python - CLI Print Tool
Improve the readability and appearance of your print statements.

---

## How to get started
If you would rather take a look at the code instead of the documentation, open directly the `example.py` file.

### Step 1 - Import the class
Import the `CLIPrintTool` class from `cli_print_tool.py`
```python
from cli_print_tool import CLIPrintTool
```
(Optional) Import the `TextAlignment` class from `cli_print_tool.py` to change the text alignment (by default left-aligned).
```python
from cli_print_tool import CLIPrintTool, TextAlignment
```

### Step 2 - Create a class object
Create a `CLIPrintTool` object.
```python
CLIPrintTool()
```
(Optional) Specify the maximum line length for your content (by default 100 characters).
```python
CLIPrintTool(120)  # custom max length of 120 characters
```

### Step 3 - Use the public object methods
Use the [public methods](#list-of-public-methods) from `CLIPrintTool` to print your formatted text content.
```python
CLIPrintTool().textbox("Hello World!")
```

---

## List of public methods
1. [Text](#text)
2. [Textbox](#textbox)
3. [Heading](#heading)
4. [List](#list)

---

## Text
Takes two parameters and prints long text wrapped to respect the maximum line length.

### Parameters
<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Type</th>
            <th>Required</th>
            <th>Default Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>text</td>
            <td>String</td>
            <td>Yes</td>
            <td>None</td>
        </tr>
        <tr>
            <td>alignment</td>
            <td>TextAlignment</td>
            <td>No</td>
            <td>TextAlignment.left</td>
        </tr>
    </tbody>
</table>

### Examples
#### Example 1
Prints long text wrapped to respect the maximum line length and left-aligned.
```python
long_text = "This is a very very very very very long sentence. And here is another one, but don't worry about that \
CLIPrintTool will automatically wrap the text to respect the maximum line length (by default 100 characters)."

CLIPrintTool().text(long_text)
```
![Screenshot of the console output from the example above.](./img/text-example-1.png)

#### Example 2
Prints long text wrapped to respect the maximum line length and centered.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
long_text = "This is a very very very very very long sentence. And here is another one, but don't worry about that \
CLIPrintTool will automatically wrap the text to respect the maximum line length (by default 100 characters)."

CLIPrintTool().text(long_text, TextAlignment.center)
```
![Screenshot of the console output from the example above.](./img/text-example-2.png)

#### Example 3
Prints long text wrapped to respect the maximum line length and right-aligned.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
long_text = "This is a very very very very very long sentence. And here is another one, but don't worry about that \
CLIPrintTool will automatically wrap the text to respect the maximum line length (by default 100 characters)."

CLIPrintTool().text(long_text, TextAlignment.right)
```
![Screenshot of the console output from the example above.](./img/text-example-3.png)

---

## Textbox
Takes two parameters and prints text inside a box.

### Parameters
<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Type</th>
            <th>Required</th>
            <th>Default Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>text</td>
            <td>String</td>
            <td>Yes</td>
            <td>None</td>
        </tr>
        <tr>
            <td>alignment</td>
            <td>TextAlignment</td>
            <td>No</td>
            <td>TextAlignment.left</td>
        </tr>
    </tbody>
</table>

### Examples
#### Example 1
Prints text inside a box and left-aligned.
```python
CLIPrintTool().textbox("The quick, brown fox jumps over a lazy dog.")
```
![Screenshot of the console output from the example above.](./img/textbox-example-1.png)

#### Example 2
Prints text inside a box and centered.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().textbox("The quick, brown fox jumps over a lazy dog.", TextAlignment.center)
```
![Screenshot of the console output from the example above.](./img/textbox-example-2.png)

#### Example 3
Prints text inside a box and right-aligned.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().textbox("The quick, brown fox jumps over a lazy dog.", TextAlignment.right)
```
![Screenshot of the console output from the example above.](./img/textbox-example-3.png)

---

## Heading
Takes three parameters and prints two texts vertically separated by a line (divider).

### Parameters
<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Type</th>
            <th>Required</th>
            <th>Default Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>title</td>
            <td>String</td>
            <td>Yes</td>
            <td>None</td>
        </tr>
        <tr>
            <td>subtitle</td>
            <td>String</td>
            <td>Yes</td>
            <td>None</td>
        </tr>
        <tr>
            <td>alignment</td>
            <td>TextAlignment</td>
            <td>No</td>
            <td>TextAlignment.left</td>
        </tr>
    </tbody>
</table>

### Examples
#### Example 1
Prints two texts vertically separated by a line (divider) and left-aligned.
```python
CLIPrintTool().heading("This is a Title", "This is a Subtitle")
```
![Screenshot of the console output from the example above.](./img/heading-example-1.png)

#### Example 2
Prints two texts vertically separated by a line (divider) and centered.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().heading("This is a Title", "This is a Subtitle", TextAlignment.center)
```
![Screenshot of the console output from the example above.](./img/heading-example-2.png)

#### Example 3
Prints two texts vertically separated by a line (divider) and right-aligned.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().heading("This is a Title", "This is a Subtitle", TextAlignment.right)
```
![Screenshot of the console output from the example above.](./img/heading-example-3.png)

---

## List
Takes three parameters and prints a list of elements vertically with a title (optional).

### Parameters
<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Type</th>
            <th>Required</th>
            <th>Default Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>elements</td>
            <td>List of String</td>
            <td>Yes</td>
            <td>None</td>
        </tr>
        <tr>
            <td>title</td>
            <td>String</td>
            <td>No</td>
            <td>""</td>
        </tr>
        <tr>
            <td>alignment</td>
            <td>TextAlignment</td>
            <td>No</td>
            <td>TextAlignment.left</td>
        </tr>
    </tbody>
</table>

### Examples
#### Example 1
Prints a list of elements vertically without title and left-aligned.
```python
CLIPrintTool().list(["System Information", "Crash Reports", "Exit"])
```
![Screenshot of the console output from the example above.](./img/list-example-1.png)

#### Example 2
Prints a list of elements vertically without title and centered.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().list(["System Information", "Crash Reports", "Exit"], "", TextAlignment.center)
```
![Screenshot of the console output from the example above.](./img/list-example-2.png)

#### Example 3
Prints a list of elements vertically without title and right-aligned.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().list(["System Information", "Crash Reports", "Exit"], "", TextAlignment.right)
```
![Screenshot of the console output from the example above.](./img/list-example-3.png)

#### Example 4
Prints a list of elements vertically with title and left-aligned.
```python
CLIPrintTool().list(["System Information", "Crash Reports", "Exit"], "MAIN MENU")
```
![Screenshot of the console output from the example above.](./img/list-example-4.png)

#### Example 5
Prints a list of elements vertically with title and centered.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().list(["System Information", "Crash Reports", "Exit"], "MAIN MENU", TextAlignment.center)
```
![Screenshot of the console output from the example above.](./img/list-example-5.png)

#### Example 6
Prints a list of elements vertically with title and right-aligned.

**Note:** The `TextAlignment` class needs to be imported from `cli_print_tool.py` to change the text alignment.
```python
CLIPrintTool().list(["System Information", "Crash Reports", "Exit"], "MAIN MENU", TextAlignment.right)
```
![Screenshot of the console output from the example above.](./img/list-example-6.png)