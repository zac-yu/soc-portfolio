# GitHub Upload Guide

## Option A — GitHub website (easiest)

1. Sign in to GitHub and select **New repository**.
2. Repository name: `soc-analyst-home-lab`.
3. Description: `End-to-end SOC home lab covering Active Directory, Intune, Splunk, Sysmon, Suricata IDS, detection engineering and incident response.`
4. Choose **Public** so recruiters can view it.
5. Do not initialize it with a README because this project already contains one.
6. Create the repository.
7. On the empty repository page, select **uploading an existing file**.
8. Drag the contents of the `soc-analyst-home-lab` folder into the upload area.
9. Commit message: `Initial SOC home lab portfolio documentation`.
10. Select **Commit changes**.

For a whole folder structure, GitHub Desktop or Git command line is usually more reliable than browser upload.

## Option B — GitHub Desktop (recommended for beginners)

1. Install and sign in to GitHub Desktop.
2. Select **File → Add local repository**.
3. If prompted that the folder is not a repository, choose **create a repository**.
4. Set the local path to the extracted `soc-analyst-home-lab` folder.
5. Confirm the repository name and create it.
6. Review every file in the Changes view.
7. Summary: `Initial SOC home lab portfolio documentation`.
8. Select **Commit to main**.
9. Select **Publish repository**.
10. Clear **Keep this code private** and publish.

## Option C — Git command line

Run these commands from inside the project folder. Replace `YOUR-USERNAME` with the GitHub username and use the exact URL GitHub provides.

```bash
git init
git branch -M main
git add .
git status
git diff --staged
git commit -m "Initial SOC home lab portfolio documentation"
git remote add origin https://github.com/YOUR-USERNAME/soc-analyst-home-lab.git
git push -u origin main
```

If Git requests your identity:

```bash
git config --global user.name "Zac Yu"
git config --global user.email "YOUR-GITHUB-EMAIL"
```

GitHub no longer accepts a normal account password for Git operations over HTTPS. Sign in through GitHub Desktop, Git Credential Manager, SSH, or a personal access token.

## Add screenshots later

1. Crop and sanitize each screenshot.
2. Give it a descriptive name, for example `suricata-fast-log-alert.png`.
3. Place it under the relevant screenshots folder.
4. Add it to a Markdown file:

```markdown
![Suricata custom ICMP alert](../screenshots/suricata/suricata-fast-log-alert.png)
```

5. Commit and push:

```bash
git add .
git status
git commit -m "Add Suricata detection evidence"
git push
```

## Recommended repository settings

- Add topics: `cybersecurity`, `soc`, `splunk`, `suricata`, `sysmon`, `active-directory`, `intune`, `incident-response`.
- Pin the repository on your GitHub profile.
- Put the repository link on your resume and LinkedIn Featured section.
- Update `PROJECT_STATUS.md` after each lab session.
- Prefer small, evidence-based commits instead of uploading everything under one vague message.

