# **SBA: Version Control** *Desiree Rose*

## Reflection: 
>*In this assessment, I was able to practice the skills that I learned in Module 1: Version Control. This exercise simulated working on a large project where there were multiple peolple working on different sections of the project. I learned how to track changes in my codebase, collaborate with others using remote repositories, and managing branches for feature development. I was also able to practice using the CLI in bash, which really helped work on my muscle memory in the bash command line interface.*
>*I did find that the SBA instructions did not give me all of the steps needed to complete this assignment, so I had to use what I learned througout module 1 to add a few steps that were needed to successfully complete the excersize, so here are the actual steps that I took:*

# Part 1: Set Up the Repository

### 1. Create a New GitHub Repository:

- Log in to your GitHub  account and create a new repository.
- Name the repository as follows: version-control-simulation-desireeRose.
- Do not initialize the repository with a README or any other files (this will be done locally).
- Copy the repository URL for future use.

### 2. Clone the Repository:

- Clone the repository to your local machine:

```bash
    $ git clone https://github.com/your-username/version-control-simulation-desireeRose.git
```

# Part 2: Create and Manage Branches

### 1. Create a New Branch for a Feature:

- In your local repository, create a new branch called feature/header to simulate working on the header section of a webpage:

```bash
    $ git checkout -b feature/header
```

### 2. Make Changes in the Feature Branch:

- Create a simple index.html file, and add a basic HTML structure with a header.
- Stage and commit the changes:

```bash
    $ git add index.html
    $ git commit -m "Added header section to index.html"
```

### 3. Switch Back to Main:

>*I had an issue here because git couldn't find my main branch, so I had to create one.*

- Switch back to the main branch:

```bash
    $ git checkout main
```

>*Instead I used:*

```bash
    $ git checkout -b main
```

# Part 3: Simulate a Merge Conflict

### 1. Create a New Branch for Another Feature:

- Create another branch called feature/footer to simulate working on a different feature:

```bash
    $ git checkout -b feature/footer
```

### 2. Make Changes in the New Branch:

- In index.html, add a footer element at the bottom of the file.
- Stage and commit the changes:

```bash
    $ git add index.html
    $ git commit -m "Added footer section to index.html"
```

### 3. Switch Back to feature/header:

- Now, switch back to the feature/header branch and modify the index.html file by changing something in the footer section to simulate a conflict.

### 4. Merge feature/footer into main:

- Merge the feature/footer branch into main:

```bash
    $ git checkout main
    $ git merge feature/footer
```

### 5. Attempt to Merge feature/header:

- Now, try merging the feature/header branch into main:

```bash
    $ git merge feature/header
```

### 6. Resolve the Conflict:

- A merge conflict will occur. Open the conflicting file, resolve the conflict, and commit the resolved changes.
- Use git status to ensure all conflicts are resolved, then:

```bash
    $ git add index.html
    $ git commit
```
>*In order to fix the conflict, I opened up the file and edited it, then ran add then commit.*
