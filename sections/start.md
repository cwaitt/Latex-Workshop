# Getting Started
Once you log into Overleaf, you will see a page that looks something like this:

![Starting](/images/Getting-Started.png)

If this is your first time in Overleaf, you shouldn't have any documents here. However, as you can see, Overleaf gives you the ability to easily create new projects, as well as an organizational scheme so you can store and save older documents.

Lets start by creating a new project by selecting the green `New Project` button above. This should create a drop down menu like this:

![Blank](/images/Blank-project.png)

As you can see, you can start a project from scratch (Blank Project), or a generic Template Document, or from a preexisting project. LaTeX as has some premade templates for spefic documents such as articles, letters, CVs, etc. For now, lets start a brand new project by selecting `Blank Project` and name it `My First LaTeX Project` or some other pithy title.

# Overleaf Structure
Overleaf organizes every project into three windows.

![Overleaf](/images/Overleaf-config.png)

1. (Far left) Window that displays and organizes various LaTeX files, images, and folder. `main.tex` is usually the name of your primary LaTeX file that Overlead reads and begins its compilation into pdf from.
2. (Center) The most import window of all three. This contains content of `main.tex` which is the source code written in LaTeX that is latter compiled into a pdf. This window is where you will be spending 99% of your time. 
3. (Far Right) This window compiles your LaTeX code into a pdf, which can be viewd on the right. The resulting document can then be downloaded for your own personal use.

Before we begin editing or writing anything LaTeX, lets break down the structure of the LaTeX code.

## LaTeX Document Structure

![Doc_Struct](/images/Doc-Struct.png)

Firstly, Overleaf color codes LaTeX specific commands as either blue or green, and plain text as black. You will also notice that the LaTeX commands start with a`\command{something}` or `\command[option]{something}`. These are protected symbols that LaTeX use to tell the difference between text and commands. We wont get into specifics here, but you should be aware that there are certain symbols you need to use with caution. 

Every LaTeX document as two sections: a Preamble and a Body.

[The Preamble and Body >>>](preamble-body.md)

[<<< Back](account.md)

[<<< Home](../README.md)
