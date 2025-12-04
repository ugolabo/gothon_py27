# gothon with Python 2.7

This interactive story (7-min read), built in Python 2.7, serves as a proof of concept for a separate project: web.py with Python 3.11 (available in repo: **webpy_py311**). Conceived after an in-depth review of a prior edition of "<a href="https://learnpythonthehardway.org/" target="_blank">Learn Python the Hard Way</a>" (Exercise 43 with additional bells and whistles), this initial project has a dual purpose. First, it is used to test various deployment solutions -- such as virtual environments, standalone packages and containers -- that ensure a project runs reliably with specific versions of the Python interpreter and modules. Second, these tested solutions serve as documented methods for reproducing or reimplementing the project on different operating systems.

<center>
First...

| gothon (English) | gothon (français) |
|:---:|:---:|
| <img src="img/gothon_e.gif" alt=""/>  | <img src="img/gothon_f.gif" alt=""/>  |

Then...

| web.py (English/français) |
|:---:|
|   |

<img src="img/webpy_py311.gif" width=50% alt=""/>
</center>

## Project Setup and Structure

To run this interactive story locally, please ensure your environment meets the following requirements:

- Clone the Repository: Begin by cloning the project files to your machine.
- Environment: The application is designed for Python 2.7.
Dependencies: Only standard modules that come with the Python interpreter. No independant modules needed.

### Directory Layout

The project utilizes a clear structure to separate the engine and story logic.

```text
────gothon
    ├───bin
    └───gothonmap
```

Function: The core application engine ('bin/engine.py') retrieves the narrative data from 'gothonmap/map.py', dynamically renders it.

## Running the Application

To launch the web application, follow these simple steps:

- Navigate: Ensure your terminal is at the root directory of the project (gothon/).
Execute: Run the main application file using your Python executable: python bin/engine.py
    - Note: Depending on your OS setup, you may need to use `py -2 bin/app.py` or `python2 bin/app.py`.
- Access: The interactive story will begin in your terminal. Enter your choices at the command prompt to proceed.

### Troubleshooting: PYTHONPATH Errors

If the Python script fails to launch or reports that it cannot find modules (like `gothonmap`), you likely have a `PYTHONPATH` issue. The interpreter needs to be told where to look for the project's internal libraries.

Execute the appropriate command below in your terminal before you run python `bin/engine.py` again:

- For Linux/macOS: `export PYTHONPATH=$PYTHONPATH:.`
- For Windows (PowerShell): `$env:PYTHONPATH = "$env:PYTHONPATH;."`

Have fun!

For detailed information on the Project's Origins and Modernization efforts, as well as the underlying Concept of Interactive Stories, please refer to the main repository: **webpy_py311**.
