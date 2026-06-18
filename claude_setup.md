# NF AI Workshop Tutorial
brought to you by the [2026 NF AI Workshop](https://nf-ai-workshop.github.io/nf_conference2026/)

> reach out to [Gloria Wang](https://gxywang.github.io) with any feedback on this tutorial


### Table of Contents
1. [Setting Up Claude Code in VS Code](#1-setting-up-claude-code-in-vs-code)
2. [Starting a Project with Claude Code](#2-starting-a-project-with-claude-code)
   - 2.1  [Setting up a new project](#21-setting-up-a-new-project)
   - 2.2  [An introduction to VS Code](#22-an-introduction-to-vs-code)
   - 2.3  [Claude settings](#23-claude-settings)
   - 2.4  [Tips on using Claude in VS Code](#24-tips-on-using-claude-in-vs-code)

</br>

# 1. Setting Up Claude Code in VS Code
- Go to [VS Code](https://code.visualstudio.com/) and select the `Download` button in the middle of the screen

![vs code screenshot](media/vscode.png)

- Once the file has finished downloading, open your `Downloads` folder and double-click on the file `VSCode-darwin-arm64.dmg`. A pop-up window should appear like the one below (for Mac):

![vs code download](media/vscode_install.png)

- Follow the instructions in the pop-up window. On Mac, drag the `Visual Studio Code` icon into the `Applications` folder.

- Bringup the app by searching for `Visual Studio Code` in Spotlight Search (on Mac) or Windows Search (on Windows).

![vs code](media/vscode_welcome.png)

- Select the `Extensions` button on the left sidebar where the mouse cursor is on the image above. This will pull up a side window where you can search for `claude` and install the extension called `Claude Code for VS Code` as seen in the image below.

![vs code extensions](media/vscode_extensions.png)

- Then click the `Claude Code` button in the top right corner to bring up the extension.

![vs code claude extension](media/vscode_claude_ext.png)

- Now you should see something similar to the image below with `Claude Code` on the right window.

![vs code claude code](media/vscode_claude_code.png)

- You can clean up the screen by clicking the `Extension` button on the left sidebar again to minimize the window.

![vs code minimize extension](media/vscode_ext_minimize.png)

- And close the `Extension: Claude Code for VS Code` window by clicking the `X` button on the top menu.

![vs code exit extension](media/vscode_exit_ext.png)

- Your screen should look similar to below.

![vs code clean](media/vscode_clean.png)

- In `Claude Code`, click login with `Anthropic Console` and allow the pop-up window to open.

![claude login](media/claude_login.png)

- This will pull up a login page on your browser like the one below. Login with the email you used to register for the workshop, and follow the login instructions on the screen.

![claude console login](media/claude_console_login.png)

- If you are asked which organization to connect, pick `NF AI Workshop`

![claude console organization selection](media/claude_console_org_selection.png)

- Authorize access, then close the window when prompted and go back to `VS Code`.

![claude console authorize](media/claude_console_authorize.png)

- You're `Claude Code` window should now look like this.

![claude code](media/claude_code.png)

# 2. Starting a Project with Claude Code

## 2.1 Setting up a new project

- Now let's start a project. Click the `Open...` button on the `Welcome` page.

![vscode open folder](media/vscode_open_folder.png)

- Make a new folder and name it something related to your project.

![new folder](media/new_folder.png)

- And open the folder.

![open folder](media/open_folder.png)

- Your VS Code should now look like this:

![new proj](media/new_proj.png)

- In the top-right corner, click the `...` menu next to `CHAT` and select `Claude Code` to pull up Claude in the window.

![claude code chat](media/claude_code_chat.png)

- Now you are good to go! In the section below, we will introduce some basic commands when using VS Code and Claude.

## 2.2 An introduction to VS Code

> VS Code is a popular software development environment.

- On the left-hand menu, click the `file +` icon to create a new file. You can also drag-and-drop existing files to add them to your project.

![vs code new file](media/vscode_new_file.png)

- The `folder +` icon to the right creates a new folder. Use this to organize your project.

![vs code new folder](media/vscode_new_folder.png)

- At the top menu bar, select `Terminal` -> `New Terminal` (or use the shortcut `Ctrl+Shift+tilde`) to bring up a new terminal.

![vs code new terminal](media/vscode_new_terminal.png)

- The new terminal will appear at the bottom of your screen. You can use it to run scripts. If you're not sure how, feel free to ask Claude which commands to run or let Claude run it for you.

![vs code terminal](media/vscode_terminal.png)

## 2.3 Claude settings

- Type `/` in the bottom text bar like so, and it will bring up some common settings.

  ![claude options](media/claude_options.png)

  - `Switch model...` lets us choose which model to use. The table below gives a short description of the latest models. We recommend Opus 4.8 for coding tasks.

  - > Anthropic's newest model, Fable 5.0, is unavailable due to [government restrictions](https://www.anthropic.com/news/fable-mythos-access).

  ![claude model comparison](media/claude_model_comparison.png)

  - `Effort` determines how many tokens Claude is willing to use when responding to requests. You can read more about it [here](https://platform.claude.com/docs/en/build-with-claude/effort#effort-levels).

  - `Thinking` will enhance reasoning capabilities and increase the amount of time Claude takes to produce an answer.

- Select the `</>` button at the bottom of the prompt box to change permission settings. For larger projects, we recommend to use `Plan mode` first, and then `edit automatically` once you think the plan looks good.

![claude permissions](media/claude_permission.png)

- Click the `+` button in the top-right corner to start a new chat.

![claude new chat](media/claude_new_chat.png)

- The clock icon in the top-right corner lets you go through previous conversations.

![claude prev convo](media/claude_prev_convo.png)

- To learn more about using Claude in VS Code, take a look at the [documentation](https://code.claude.com/docs/en/vs-code#get-started).


## 2.4 Tips on using Claude in VS Code

### General tips

- `CLAUDE.md` is a file that gives Claude a set of rules to follow throughout the whole project. It automatically loads into every session, so you don't need to re-explain general guidelines. Create a `CLAUDE.md` at the root of your project and copy-paste this into your file: [Kaparthy skills for Claude](https://github.com/multica-ai/andrej-karpathy-skills/blob/main/CLAUDE.md).

- In the prompt box, you can `@-file` (e.g. `@project_docs.md`) to reference a file in your project directly, so Claude doesn't have to go look for it.

- Manage context-- how much information Claude sees at a time-- by running `/clear` or `/compact <instructions>` (e.g. `/compact Focus on changes`) fairly often to help Claude focus and reduce token usage. Another trick is to let Claude summarize its progress in a `PROGRESS.md` file as it works so you can use `/clear` often without loosing information about what Claude is doing.

- Use `/btw` for quick questions that don't need to be recorded in conversation history.

> Visit [Claude Best Practices](https://code.claude.com/docs/en/best-practices) for more tips and tricks on using Claude.



### Smaller projects

For smaller projects like personal websites or data filtering scripts, you can use the prompt box to directly tell Claude what to do.

![claude prompt](media/claude_prompt.png)
- use the `+` button on the bottom left to add relevant files for Claude to reference

You can follow up with any feedback or additional requests by using the prompt box in the same chat.

### Larger projects
For larger projects, I recommend writing a project plan document with the task, requirements, relevant resources and references-- similar to a research proposal. You can also directly give Claude the research proposal and let it start working from there.

- Here is an example project plan:

![claude project plan](media/claude_plan.png)

- View the full document [here](media/example_plan.md).

These plans are often written in Markdown, which is used to easily format text. Just create a file with the ending `.md` and start writing. 

- [This](https://www.markdownguide.org/cheat-sheet/) is a formatting cheat sheet. 

- You can view formatted text in VS Code by clicking the `magnifying glass book` icon on the top-right corner of the middle window, near the Claude icon. This will pull up a preview on the right tab, while you write in the left tab.

![markdown preview](media/markdown_preview.png)
