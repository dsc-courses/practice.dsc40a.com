# practice.dsc40a.com

Repository containing practice problems for DSC 40A (past exams and discussion). Hosted at practice.dsc40a.com. 

### Note to futor tutors: If you encountered new issues and resolved it, please help contribute to the "Troubleshooting tips" section below. Thank you! 
-- Your fellow tutor from 2025

# Index 
- 1. Requirements and setup
- 2. Understanding the repo
- 3. Adding problem sets
- 4. Troubleshooting tips

# 1. Requirements and setup
Before using the repo, make sure you have the following packages installed:

```
- BeautifulSoup4
- pandoc
- lxml
```
Note: If you have taken dsc80, you can run this in dsc80's environment. 

# 2. Understanding the repo
## 2.1 Walk through videos from creator of this site 
### (1). [Here is a walkthrough video](https://www.loom.com/share/cdbc8dcc026c43d6ac48cc2df3f57ea8?sid=202e8678-b073-46ff-91d0-afe775bb2541) of how to edit the site.
### (2). [Here's another walkthrough video](https://www.loom.com/share/4fb2816102034b14b4b0cd6476091ec3?sid=6529b884-e4c0-4460-8baa-1051c55a4a5f) of how to use the latex-to-practice-site script!   

## 2.2 Folder info   
1. Important folders: assume you are inside the root directory, `practice.dsc40a.com/`. The only three important folders you will read/write to will be:   
  - `assets`: Where you put your images from the exams. 
  - `docs`: Where you can preview the site's `.HTML` page files.
  - `pages`: Contains metadata/ general information about each exam in `.yml` format. You will add a new file to exam or topic for generating new exam files.
  - `problems`: The generated markdown files from your exams. In case the generating python file fails to compile your latex exam, this is where you will mannually write up the questions and answers. 

# 3. Adding problem sets 
## 3.1 Style guide for writing up problems:

- **Answer:** should be bolded followed by unbolded answer(s), comma separated if it fits on one line, or each answer on a new line if it doesn't fit on one line
- Use () for choose one, [] for select all. Add a space before the text of each answer choice.
- For subsubparts, use numbers followed by period to introduce each question

In translating from Latex to Markdown, there are a few easy find/replace things that help with a lot of things:

```
\begin{verbatim} --> ```py
\end{verbatim} --> ```
" --> '
\_ --> _
\texttt{ --> `
\textbf{ --> **
\textit{ --> *
\bubble --> ( )
\correctbubble --> ( )
\squarebubble --> [ ]
\correctsquarebubble --> [ ]
\begin{subprobset} -->
\end{subprobset} -->
\begin{subprob} --> # BEGIN SUBPROB
\end{subprob} --> # END SUBPROB
\begin{responsebox} --> # BEGIN SOLUTION
\end{responsebox} --> # END SOLUTION
\begin{soln} --> # BEGIN SOLUTION
\end{soln} --> # END SOLUTION
\bigskip -->
\noindent --> 
```
- Note: ( ) and [ ] need a space between the brackets. There should not be blank lines between options.

To explain up-front:
- All exams are individual (collaboration on exams is never allowed).
- What ( ) and [ ] mean. In their absence, students needed to write out code by hand.
- In-person means on-paper.
- Think of select-all questions as a sequence of true-false questions. Partial credit for these questions was assigned accordingly.
- When taking an exam for practice, we recommend having a copy of the DSC 10 reference sheet open in another tab, as well as a second copy of the exam, so you can access the data descriptions.


## 3.2 In case generating test file fails: here's what to do. 
1. As usual, create exam file in `pages` and add your current exam questions to the `exams` and `topics` folder. 
2. Now, if you encounter issue with generating exams because of format issue, go to `problems` -> create new folder for exam -> create MD files for each question. You can use `problems/template.md` template to generate question files and solution.  
**NOTE: Please remember to check for correctness; LLM is not to be relied upon, and we want to be responsible to our fellow students. :)** 
3. Compile and test it locally: `python run.py [insert yaml file name for the exam you created/changed] `. For example, 
`python run.py pages/exams/ss1-25-midterm.yml`
**NOTE: Unless youve messed up tremendously and feel like you have to recompile everything, do not run ``python run.py` without arguments; this will take some 5-10 minutes regenerating every MD file for every exam and topic! 

## 3.3 Sample walk through 
When you are adding a new exam, this is typically what youll do. 
1. If you are not familar with git and worry about messing up, create a separate branch so your will not risk exploding the practice site accidentally. 💥 Only merge your changes to main when you make sure everything works. 
2. In the page folder, create exam file in `pages/exams`. By topic, update the topic file in `pages/topics`. 
3. Follow the steps in the video, run `utils/latex-to-md.py`. If running `utils/latex-to-md.py` fails, create MD file mannually for all the exam questions. 
4. In case latex to md fails, you will possibly also have to add the new file to `docs/index.html`. Add a new entry like this: 
```html
<tr>
<th scope="row">
[Fall 2025] <!-- 1. Quarter information -->
</th>
<td>
Gal Mishne
</td>
<td>
[<a href='fa25-midterm/index.html'>Final </a>] <!-- 2. Your exam files that will be generated by run.py. -->
[<a href='fa25-midterm/index.html'>Midterm </a>] 
</td>
</tr>
```
5. Locally test the files by compiling and run `run.py` with the approprieate argument, go into `docs/your-exam/`, and open the `HTML` file to check correctness.  Also check `docs/index.html` to see your exam is being displayed. 

# 4.Troubleshooting tips 
#### 1.yaml `ModuleNotFoundError` 
```
python run.py
Traceback (most recent call last):
  File "..../practice.dsc40a.com/run.py", line 1, in <module>
    import yaml
ModuleNotFoundError: No module named 'yaml'
```
**Example Behavior:**
```
(base) practice.dsc40a.com % python run.py
Traceback (most recent call last):
  File "practice.dsc40a.com/run.py", line 1, in <module>
    import yaml
ModuleNotFoundError: No module named 'yaml'
(base) practice.dsc40a.com % pip3 install PyYAML

[notice] A new release of pip is available: 24.2 -> 25.3
[notice] To update, run: python3.12 -m pip install --upgrade pip
error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try brew install
    xyz, where xyz is the package you are trying to
    install.
    
    If you wish to install a Python library that isn't in Homebrew,
    use a virtual environment:
    
    python3 -m venv path/to/venv
    source path/to/venv/bin/activate
    python3 -m pip install xyz
    
    If you wish to install a Python application that isn't in Homebrew,
    it may be easiest to use 'pipx install xyz', which will manage a
    virtual environment for you. You can install pipx with
    
    brew install pipx
    
    You may restore the old behavior of pip by passing
    the '--break-system-packages' flag to pip, or by adding
    'break-system-packages = true' to your pip.conf file. The latter
    will permanently disable this error.
    
    If you disable this error, we STRONGLY recommend that you additionally
    pass the '--user' flag to pip, or set 'user = true' in your pip.conf
    file. Failure to do this can result in a broken Homebrew installation.
    
    Read more about this behavior here: <https://peps.python.org/pep-0668/>

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
```
**Solution:** 
- If you have already installed the above packages but still encounter this issue, and have taken DSC 80, use DSC 80 environment either in terminal or in VS code. 
- Otherwise, there will be some rocky troubleshooting with your python environment. Wish you the best of luck (from struggling former tutor).

#### 2.Pathname issue 
```
File "practice.dsc40a.com/run.py", line 549, in <module>
    write_all_pages()
  File "practice.dsc40a.com/run.py", line 508, in write_all_pages
    write_page(path, called_from_write_all_pages=True)
  File "practice.dsc40a.com/run.py", line 421, in write_page
    page, title = process_page(path, is_discussion=is_discussion)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "practice.dsc40a.com/run.py", line 389, in process_page
    out += stitch(params['problems'], params['show_solution'])
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "practice.dsc40a.com/run.py", line 121, in stitch
    r = open(path, 'r', encoding='UTF-8').read()
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'problems/ss2-24-final\\ss2-24-final-q01.md'
```

**Cause**: Windows and mac have different ways of doing pathnames. 

**Solution**: In run.py, you can see the following line:

```python
def stitch(files, show_solution, toc=False):
    ...
    for i, path in enumerate(paths):
            
            # Comment the line below out if you are using windows.
            path = path.replace('\\', '/')
            # Coment the line above out if you are using windows. 

            path = os.path.normpath(path)
    ...
```

Follow the instruction of the comments. If you have issue with pathname, the cause is likely somewhere in this function.