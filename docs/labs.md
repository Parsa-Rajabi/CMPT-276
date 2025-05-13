# Labs

We are using GitHub Classroom to deliver the labs for this course. You will first need to create a GitHub account, and then you can accept each Class Activity. Once the lab is ready, the link will become active, and you will be able to accept the lab in your [GitHub.com](https://github.com/) account.

Once you click the link, a repository will automatically be created for you with instructions. You can then work on the labs, make commits, and push them to GitHub as often as you please. The last commit before the deadline will be the one that is graded.

This the tentative schedule for all course labs, which is subject to change without notice. Please check on a regular basis for the most up-to-date schedule.

## Labs
Lab links (including schedule) to be posted here once the labs are ready. You will be able to accept the lab in your GitHub account.

<!-- | Labs  | Due Date |                              Link                              |
| :---: | :------: | :------------------------------------------------------------: |
| Lab 1 |          | [Accept L1 on Github](https://classroom.github.com/a/YiysRgeQ) |
| Lab 2 |          | [Accept L2 on Github](https://classroom.github.com/a/EFazkwSK) |
| Lab 3 |          | [Accept L3 on Github](https://classroom.github.com/a/12jxi3mM) |
| Lab 4 |          | [Accept L4 on Github](https://classroom.github.com/a/diab_lxp) |
| Lab 5 |          | [Accept L5 on Github](https://classroom.github.com/a/7UVNZgBt) | -->


### Canvas

All course content include assignments, labs etc. will need to be submitted on Canvas via the [assignment tab](https://canvas.sfu.ca/courses/90645/assignments). Not submitting on Canvas will be considered as a missed assignment/lab and the following penalties will be applied:

- 1st instance penalty = -5%
- 2nd instance penalty = -15%
- 3rd instance penalty (and onwards) = -25%

Students who not submit on Canvas will be assigned a grade of 0 until they reach out to their TA with the correct submission, within 7 days of the deadline. No missed canvas submission will be accepted after 7 days of the deadline. This is not to be confused with the late submission policy, which is outlined in the course syllabus.

### Late Submissions

Refer to the [course syllabus for the late submission policy](/syllabus.md?id=late-deliverables).

### Github Classroom

Here are some instructions on how to start working on assignments/labs that are available on Github classroom.

- Step 1: Accept assignment/lab with link above, and open a Terminal
- Step 2: Clone the repo on your local computer [View Tutorial / Common errors](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
  - `git clone https://...`
- Step 3: Navigate to that directory 
  - `cd /path/to/where/you/cloned/repo/`
- Step 4: Try to navigate the files and folders (if any) in your repo using the Terminal
- Step 5: Making changes based on instructions 
- Step 6: Commit your changes to the repository 
  - `git add -A or git add .`
  - `git commit -m "Insert your commit message here i.e. Updated file X"`
  - You can commit changes to your repository **as many times as you like before the deadline** (any commits after the deadline will be ignored)
- Step 7: Pushing the changes above
  - `git push`
- Step 8: Copy your repository link and submit the link to [Canvas assignment](https://canvas.sfu.ca/courses/90645/assignments). After the deadline, we will begin marking submitted assignments.
  - The link will look something like this: `https://github.com/CMPT-276-FALL-2024/CMPT-276-assignment-#-[YOUR GITHUB USERNAME]` for example, for A1, it will be `https://github.com/CMPT-276-FALL-2024/CMPT-276-assignment-1-Parsa-Rajabi`

### Working with Git

1. Add file: `git add filename.format`
    - e.g. `git add example.txt` (to add a text file named example)
  - 1b. You can commit all files in your directory by using either:
     - `git add .`
     - `git add -A`
2. Commit changes with a message: `git commit -m "type commit message here"` (make sure the commit message is meaningful)
3. Push changes: `git push`