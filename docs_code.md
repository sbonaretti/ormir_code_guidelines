# Code documentation

The standard way to document Python code is through **docstrings** (short for *documentation strings*). A docstring is a string enclosed in triple quotes (`""" ... """`) that is placed at the beginning of a function, class, method, or module. Docstrings describe what the code does, its parameters, and return values and may also include examples, references, and additional notes.

There are several conventions for writing Python docstrings. In the ORMIR community, we recommend using either the [NumPy style](#numpy-style) or the [Google style](#google-style), as both are widely adopted in the scientific Python ecosystem and are compatible with Sphinx and Read the Docs. The choice between the NumPy and Google styles is largely a matter of project preference. At the end of the page, you will also find some tips for  [generating docstrings quickly](#docstrings-fast) using large language models.

---
(numpy-style)=
## Numpy style

The **NumPy style** is the standard in many scientific Python libraries, including NumPy, SciPy, scikit-learn, and pandas. It organizes documentation into clearly defined sections.

Here is an example of a function documented using the NumPy style:


```
def my_function(input1, input2):
    """A one-line summary of what this function does.

    Parameters
    ----------
    input1 : type
        Description of input1
    input2 : type
        Description of input2

    Returns
    -------
    output : int
        Description of the returned value.
    """

    # function body

    return output
```
A docstring contains at least three sections:

- **Short summary**:  a one-line explanation of what the function does
- **Parameters**: the name, data type, and description of each input, including default values
- **Returns**: the name, data type, and description of each output, including any special cases

For a complete reference, see the [NumPy docstring guide](https://numpydoc.readthedocs.io/en/latest/format.html).


---

(google-style)=
## Google style

The **Google style** provides the same information as the NumPy style but uses a more compact and concise format. It uses indentation instead of underlined section headers, making the docstrings shorter.

The same function written in the Google style looks like this:
```
def my_function(input1, input2):
    """Short description of the function.

    Args:
        input1 (type): Description of input1.
        input2 (type): Description of input2.

    Returns:
        int: Description of the returned value.
    """

    # Function body
    return output
```
For a complete reference, see the [Google docstring guide](https://google.github.io/styleguide/pyguide.html).

---

(docstrings-fast)=
## How do I create docstrings fast?

Writing docstrings manually can be time-consuming. Large language models (LLMs) such as Claude or ChatGPT can help you generate a first draft of your docstrings.

For example, you can ask:

> Write NumPy-style docstrings for the following function:  
> [paste your function]

or

> Write Google-style docstrings for the following function:  
> [paste your function]

**Important**: Always **review the generated documentation carefully**! LLMs can produce incorrect or incomplete descriptions, so make sure the docstrings accurately reflect what your code does.


