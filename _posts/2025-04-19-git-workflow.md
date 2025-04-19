---
layout: post
title:"Getting to grips with git"
date: 2025-04-19
---

I found getting my head around git a bit tricky, so for my own benefit I've written up a workflow that avoids getting things mixed up.

### What *Is* Git, Anyway?

Before jumping into commands, let’s take a moment to understand what Git actually **is** — and **why** it matters.

#### Git is a version control system.

That means it **keeps track of changes** you make to files over time — kind of like a save system in a video game.

Every time you make edits and save them using Git, you're creating a **checkpoint** (called a **commit**) that you can go back to later. This is especially useful when:

- You want to undo a mistake  
- You need to see what changed between two versions  
- You’re working on a big project and want to stay organized  
- You're collaborating with others and need to keep everyone's work in sync

Think of Git like this:

- Your **project folder** is a digital notebook.  
- Git is the **invisible pen** keeping a detailed history of every change.  
- Each **commit** is like a new page with notes on what changed and why.  
- GitHub is where you **upload your notebook** so others (or future-you) can read it, use it, or help edit it.

#### Local vs. Remote

- **Local**: The version of your project on your own computer.  
- **Remote**: The version stored on GitHub (or another Git host).

Git helps you move changes back and forth between those two places — safely and in order.

### A Github workflow

When working on a project, the basic cycle is  
    pull → edit → add → commit → push

#### Pull (Get the latest changes)
To make sure that changes that have been made on the remote server are reflected in the local copy, run'git pull origin main'
#### Edit (Make changes locally)
Fix typos, write new posts, all that sort of thing. Git notices which files are changed.
#### Add
This is the phase that made me scratch my head the hardest. After editing, files must be 'staged'or marked as ready to be included. This is done with the "add" command.
'git add .'
marks all changed files as staged
#### Commit (save a snapshot of changes)
'git commit -m "a message about the changes made"'
This tells git what has changed and why
#### Push (upload the changes to GitHub)
'git push origin main'
makes the changes live online, and (for example) makes new blogposts appear

### Recap

'git pull origin main   # Always start by syncing with GitHub
# edit files
git add .              # Stage all changes
git commit -m "Describe your changes"
git push origin main   # Send to GitHub'

I read somewhere, but didn't understand at the time, that git is "like saving your work, only smarter, safer, and with time travel." 

I'm still not certain I understand, and I know there is an awful lot to learn. But I feel like I might be getting there. 
