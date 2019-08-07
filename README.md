# robotframework
Ferramenta de testes robotframework

Robot Framework
•	Introduction
•	Installation
•	Example
•	Usage
•	Documentation
•	Support and contact
•	License

Introduction
Robot Framework is a generic open source automation framework for acceptance testing, acceptance test driven development (ATDD), and robotic process automation (RPA). It has simple plain text syntax and it can be extended easily with libraries implemented using Python or Java.
Robot Framework is operating system and application independent. The core framework is implemented using Python, supports both Python 2 and Python 3, and runs also on Jython (JVM), IronPython (.NET) and PyPy. The framework has a rich ecosystem around it consisting of various generic libraries and tools that are developed as separate projects. For more information about Robot Framework and the ecosystem, see http://robotframework.org.
Robot Framework project is hosted on GitHub where you can find source code, an issue tracker, and some further documentation. See CONTRIBUTING.rst if you are interested to contribute. Downloads are hosted on PyPI, except for the standalone JAR distribution that is on Maven central.
Robot Framework development is sponsored by Robot Framework Foundation.
   
Installation
If you already have Python with pip installed, you can simply run:
pip install robotframework
Alternatively you can get Robot Framework source code by downloading the source distribution from PyPI and extracting it, or by cloning the project repository from GitHub. After that you can install the framework with:
python setup.py install
For more detailed installation instructions, including installing Python, Jython, IronPython and PyPy or installing from git, see INSTALL.rst.
Example
Below is a simple example test case for testing login to some system. You can find more examples with links to related demo projects from http://robotframework.org.
*** Settings ***
Documentation     A test suite with a single test for valid login.
...
...               This test has a workflow that is created using keywords in
...               the imported resource file.
Resource          resource.robot

*** Test Cases ***
Valid Login
    Open Browser To Login Page
    Input Username    demo
    Input Password    mode
    Submit Credentials
    Welcome Page Should Be Open
    [Teardown]    Close Browser
Usage
Starting from Robot Framework 3.0, tests are executed from the command line using the robot script or by executing the robot module directly like python -m robot or jython -m robot.
The basic usage is giving a path to a test (or task) file or directory as an argument with possible command line options before the path:
robot tests.robot
robot --variable HOST:example.com --outputdir results path/to/tests/
Additionally there is rebot tool for combining results and otherwise post-processing outputs:
rebot --name Example output1.xml output2.xml
Run robot --help and rebot --help for more information about the command line usage. For a complete reference manual see Robot Framework User Guide.
Documentation
•	Robot Framework User Guide
•	Standard libraries
•	Built-in tools
•	API documentation
•	General documentation and demos
Support and contact
•	robotframework-users mailing list
•	Slack community
•	#robotframework IRC channel on freenode
•	@robotframework on Twitter
•	Other forums
License
Robot Framework is open source software provided under the Apache License 2.0. Robot Framework documentation and other similar content use the Creative Commons Attribution 3.0 Unported license. Most libraries and tools in the ecosystem are also open source, but they may use different licenses.

