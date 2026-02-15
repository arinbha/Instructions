# Technical Background

## Navigating Enterprise Codebase
When you work on an enterprise codebase for the first time,
often times there are many different files and dependencies, and it
can be overwhelming to understand how the entire system works. However,
there are many tools at your disposal to get up-to-speed.

In most companies, there will typically be a ``README`` or some other
documentation guide explaining the structure and goals of the codebase.
As an intern, one of your first jobs should be to sit down and read the entire
documentation guide at least several times *cover to cover* and take detailed
notes and questions about things you don't understand. Not only does this show
that you are taking the job seriously, you will also gain insight into how corporate
software works and learn how to structure your own codebases in the future.

Another great practice when navigating a new codebase is to experiment with
it yourself. As part of your onboarding setup, you should have created a 
local testing environment to simulate how consumers and/or internal users
interact with your code.

<span style="background-color: yellow;">
**Pro Tip:**
</span>
As you experiment with the codebase to see how the different parts interact,
write a document for yourself with short summaries explaining *in your own words* what the 
functions within the file are doing and how it contributes to the overall design. 

## Git
Most companies will have some sort of version control system for their
codebase. Version control systems track and manage changes to code and files over time, 
allowing developers to revert to previous versions, collaborate simultaneously, 
and prevent conflicting edits.

While each company and team will have different systems
and practices, having a solid understanding of version control is
important for success throughout your internship.

We present Git as it is one of the easiest systems to become familiar 
with and is one of the most prevalent across enterprise codebases.

### Basic Commands
 - ``git commit``: Records a snapshot of your staged changes.
 When commiting, you should write a descriptive message
 detailing the changes made from the last commit
 - ``git add LIST_OF_FILES``: Makes your working changes in the files listed 
 ready to commit
 - ``git push``: Uploads your local repository content to
 the other repository so others can view your changes
 - ``git pull``: Brings changes that were made from the remote
 repository into the local repository.

A typical workflow should typically contain the following steps:

 1. Pull changes with ``git pull``
 2. Make local changes, committing periodically using `git add` and
 then ``git commit``
 3. When satisfied, making them visible using ``git push``

### Branching
One of the core features of Git is that you can create separate independent
paths to work on changes that are independent of one another. When working
with a large codebase such as during an internship, it is recommended to create a
separate branch for each independent feature that you are working on.

To create a new branch, use the following command: ``git checkout -b NAME_OF_BRANCH``.
This spawns a new branch from the commit point that you are already at, and then you 
can independently add new commits onto this branch without affecting the pre-exisiting
branches.

### Rebasing
As you work on several different branches, your coworkers will likely have also made
changes to the codebase that you will need to design your code around. To avoid having
problems where the status of your code differs significantly from the existing master branch, 
you should periodically refresh your branch with the latest changes from the master branch, which we 
call rebasing. 

To rebase the master code onto your branch, use the following steps:

1. ``git checkout -b NAME_OF_BRANCH_YOU_WANT_TO_REBASE_ON``
2. ``git pull master``: This brings in any changes that were made by others
onto your master branch
3. ``git rebase master``: This will update the status of your branch such that your
changes will sit on top of the existing repository.

### Pull Requests and Code Reviews
Once you are satisfied with the changes that you've made, you are ready to merge them
into the main repository. However, in a corporate setting, you should **NEVER** attempt
to push directly into ``master``, as your changes need to be reviewed by someone on your
team. Instead, you would create a pull request, signifying that your changes are ready for
review to be merged into the master branch.

Depending on the scope of your changes, your reviewer may either approve the changes or leave
comments and request a revision. It's completely normal for your changes to be rejected at
the first pass, so don't obsess over writing completely perfect code. Often times, there may
be an edge case that you hadn't considered or a different approach that might work better. Instead,
you should focus on making sure that you understand the changes requested and make a note of them
so that you don't repeat the mistakes in the future.

<span style="background-color: yellow;">
**Pro Tip:**
</span>
Keep a separate document to write down every major comment that you received in a 
code review and reference it periodically to ensure that you are following your team's best practices
and avoid making the same mistakes repeatedly.

## AI Usage
In the age of AI, many companies are increasingly encouraging
developers to use AI for increasing productivity. While AI tools
can be useful, one of the primary goals of an internship is to learn
how to navigate a large codebase and tackle complex design challenges,
so over-relying on AI will circumvent the learning process.

**IMPORTANT:** Most open-source models, such as ChatGPT, Claude, and
Google Gemini, **should not** be used 
for company work due to privacy regulations. Instead, you should use
internal models within your company that are approved by Corporate
Security