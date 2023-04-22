
Dave's ITK spell checking code
==============================

These scripts run spell checking on the comments in the ITK codebase.
The main reason for this work has been to improve the quality of the ITK
documentation, which is extracted from those comments.

In particular, the spell checking script checks the C++ header files (.h and
.hxx) of all the classes in Modules sub-directory of ITK, except the
ThirdParty directory.  Also we spell check all code files in the ITK/Examples
sub-directory, since users may view them.  In the examples we check the
.cxx and .py files.

To run the spell checker:

    1. Create a python virtual environment using the 'requirements.txt' file.

    2. Run the 'setup' script to download ITK's codebase, the 'codespell.py'
       script, and SimpleITK's 'additional_dictionary.txt'

    3. Run the 'spell' script that actually performs the spell checking.  The
       voluminous output of the spell checker is written to 'modules.log' and
       'examples.log'.

The main spell checking script, 'codespell.py' comes from the following repo:
    https://github.com/SimpleITK/SimpleITKSpellChecking
    
The file 'itk_dict.txt' contains the dictionary of acceptable words found in
ITK.
