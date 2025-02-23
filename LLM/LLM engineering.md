###### running LLM model on the machine - ollama (c++ version of the model runs directly on command line)
to run the llm we just write 

	`ollama run <name of the llm>`  eg . llama3.2

![[Pasted image 20250223154502.png]]

list of models in the ollama page.
#### choosing a model that caters to your needs is a crucial step 
###### select a model and try out different stuff with it.
## setting up the python development environment
Anaconda is a **distribution of Python and R** specifically designed for data science, machine learning, and scientific computing. It comes with a collection of pre-installed libraries and tools, making it easier to set up and manage your environment
1. **Conda**: A package and environment manager that helps you install, update, and manage dependencies.
    
2. **Anaconda Navigator**: A graphical user interface (GUI) to manage packages and environments.
    
3. **Pre-installed Libraries**: Includes popular data science libraries like NumPy, Pandas, Matplotlib, Scikit-learn, and Jupyter Notebook.

- Anaconda includes **Jupyter Notebook**, a popular tool for interactive coding and data analysis.
    
- Jupyter Notebook is widely used in data science and machine learning for prototyping and sharing code

setting up the environment and stuff in the anaconda prompt so that it decides which package and what version compatible with my device is good for the project in the root project dir.

setup the environment with 
`conda env create -f environment.yml`
###### after installing that environment
![[Pasted image 20250223181308.png]]

and go into that environment with 
`conda activate llms`




