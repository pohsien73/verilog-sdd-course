# Publishing Guide

## Recommended public location
- GitHub username: `pohsien73`
- Repository: `verilog-sdd-course`
- Site URL: `https://pohsien73.github.io/verilog-sdd-course/`

## What is already prepared
- MkDocs site structure
- Material theme config
- GitHub Pages workflow
- course homepage, syllabus, lessons, homework, quizzes

## What you still need
1. Create GitHub account `pohsien73` if available
2. Create repository `verilog-sdd-course`
3. Push this folder to the repo
4. In GitHub repo settings, enable Pages with GitHub Actions

## Minimal commands after GitHub account exists
```bash
cd verilog-sdd-course
git init
git add .
git commit -m "Initial course site"
git branch -M main
git remote add origin git@github.com:pohsien73/verilog-sdd-course.git
git push -u origin main
```

## Important note
I can prepare everything, but I cannot directly register a GitHub account on your behalf from here.
