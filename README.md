# Week 8 workshop - Getting started with Project 2

In Project 2, you will investigate **New York City taxi data** provided by the NYC Taxi and Limousine Commission (TLC), and available to download [here](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page).

Today, we will help you get started with Project 2.

- First, we will create a new **conda environment** with the Python packages you will need for the project.
- Then, we will download one of the data files and start exploring it with the help of Pandas.
- Finally, you will discuss your ideas with your group and with a tutor about what you'd like to investigate, and start making a plan for working on your project.

---
## Setting up a new conda environment

For this project, you will **create a conda environment**. All group members should do this to set up their own computers.

An **environment** is essentially a set of packages installed together. You can create as many different environments as you like, with different packages installed, and even different versions of the same package. You can switch which environment you are using by *activating* or *deactivating* an environment.

To learn more about conda environments:

- [Conda environments](https://conda.io/projects/conda/en/latest/user-guide/concepts/environments.html)
- [Managing environments - conda documentation](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) -- if you are comfortable using a terminal.
- [Managing environments - Anaconda Navigator](https://docs.anaconda.com/anaconda/navigator/tutorials/manage-environments/#creating-a-new-environment) -- if you prefer using Anaconda Navigator.

So far in the course, we have only used the default environment, called `'base'`, which includes by default all the packages that come pre-installed with Anaconda. Creating a new environment allows us to start fresh, and only include the packages that we need.

One way to do this is with an **environment file**. The [conda documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#create-env-file-manually) gives some examples; for Project 2, you should use the file `environment.yml` provided in your repository (this is the same as the file provided in this repository).

Open the file in VSCode and look at the content.

- The name of the environment will be `pp-proj2`.
- The conda packages that we want to install are listed under `dependencies:`.
- Note that the last package we install is `pip`. This is because some of the packages you might use for Project 2 can't be installed directly with `conda`.

Now, we will use `environment.yml` to create the environment.

- If you use **Anaconda Navigator**:
    - In the "Environments" menu, click "Import" at the bottom.
    - Click on the folder icon to browse your local files, and select the file `environment.yml`.
    - Change the name from "environment" to "pp-proj2" in the text box.
    - Click "Import", and wait for the setup to finish.
    - Once it's done, your new environment `pp-proj2` will appear below `base (root)`.
    - Select `pp-proj2` to activate it, then go back to the "Home" menu, and launch Jupyter as usual. Jupyter will now be using your new environment.
- If you prefer using the **terminal**:
    - On Windows, launch Anaconda Prompt. On MacOS and Linux, launch the Terminal.
    - Run the command `conda env create -f path/to/environment.yml` and wait for the setup to finish.
    - Once it's done, run the command `conda activate pp-proj2` to activate your new environment. You can launch Jupyter after this by running the command `jupyter notebook`.

Remember to activate `pp-proj2` before every time you launch Jupyter, otherwise it will use the `base` environment by default.

#### VSCode

If you work in VSCode, you will be able to select `pp-proj2` after you set it up. To do this, when you open a .py script:

- At the bottom left of VSCode, in the blue bar, you should see something like “Python …” with a version number.
- Click on this, and you will be given more options at the top of the screen.
- Make sure you select `Python 3.x.x ... ('pp-proj2': conda)`.

When you launch a Jupyter notebook, VSCode should ask you directly to select an interpreter -- make sure you choose `Python 3.x.x ... ('pp-proj2': conda)`.

#### Checking that it works

Activate your new `pp-proj2` environment, open a .py script or a Jupyter notebook, and try the command `import fastparquet`. If it works, you're all set! If it doesn't work, ask a tutor for help.

---

## Exploring the data

The [website](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) provides "Data Dictionaries" at the bottom of the page, to explain how the data is structured, as well as a "User guide" document which explains the terminology in more detail. You should read these carefully as you're exploring the data.

Launch the notebook `exploring_data.ipynb`, and study the examples there. In particular, there is a function `get_taxi_data()` provided for you in the `utils.py` module, which you should learn how to use to retrieve the data.

Start retrieving some data, and try a few simple examples with your group. For example:

- Pick a ride and calculate its duration.
- Pick a month, a pickup zone, and calculate the average distance of all taxi rides.
- What was the most popular payment method that month?
- Look at the data distribution for different columns (e.g. fare amounts, distances...) and start thinking about data cleaning strategies.

---

## Making a plan

#### Planning your report

You should now have everything you need to get started on Project 2. Discuss your ideas for questions to investigate with your group members and with a tutor. You can take inspiration from the proposed questions in the Project 2 instructions, or you can come up with your own questions.

#### Organising teamwork

When working in teams, it's important to establish a project plan early on. Here are some important points to agree with your group:

- Is everyone comfortable with using git/GitHub with a shared repo? If not, ask a tutor **now**!
- Discuss your availability over the duration of the project. For example, some group members might be very busy right now with another assignment, and others might be fine now but will be busy in week 11; in that case, make sure you plan accordingly and set out clear expectations.
- When and how often will you meet as a group? (At the very least, you will meet every week during your workshop.)
- How will you communicate outside of your meetings (email, Teams, Discord, group chat...)?
- How will you organise the final submission? You should plan to have all your code ready at least a few days ahead of the deadline, so that you have some time to proofread the final notebook, and review the code together to make any final improvements.
- How will you distribute the workload? You have a few options:
    - Every group member works on a separate sub-task.
    - For groups of 4, split the group in 2 pairs, and each pair works on a separate sub-task.
    - One person takes on a smaller amount of programming work, but also takes the role of project manager to keep everyone on track. (That person would probably be responsible for making the submission.)
    - etc.


#### Your plan

Make sure you come up with a good plan by the start of Week 9 at the latest. In future workshop sessions, you will discuss your progress together and with a tutor, who will also be able to give you some advice and feedback.

*You can write down your ideas and your plan here in this file, to keep a record of it, and consult as you advance your project. Don't forget to commit and push your changes so they appear on GitHub for everyone.*
