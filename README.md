## Microsoft Open Source Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# msftdynamicsgpdocs
Welcome to the repository for documentation and guides for Microsoft Dynamics GP! The content is available as markdown files (.md), where each file represents an article in the help that publishes to [https://docs.microsoft.com/en-us/dynamics-gp/](https://docs.microsoft.com/en-us/dynamics-gp/). This repo also provides a way for you to actively contribute to the Dynamics GP content, and we welcome your contributions.

The *live* branch has been updated for the latest release of Dynamics GP with most recent tax updates.

If you have any questions, please contact the Dynamics SMB User Assistance (UA) team at nav-olh@microsoft.com.

## Getting started

1. Fork this repo

    You cannot work directly in the msftdynamicsgpdocs repo, so the first thing you need to do is create a fork of the repo under your GitHub account. A fork basically is copy of this repo that lets you work freely on the content without affecting the msftdynamicsgpdocs repo. For more information, see [Fork a Repo](https://help.github.com/articles/fork-a-repo/).

2.  Install GitHub Desktop (optional) and clone your forked repo.

    GitHub Desktop makes is easy to work and collaborate with repos locally from your own desktop. For more information, see [GitHub Desktop](https://desktop.github.com/).   

2. Get hold of your favorite MarkDown editor, and start making changes.

    The help content is stored in the dynamics-gp folder of the repo. Articles use a syntax for formatting text called GitHub Flavored Markdown. To learn more about working with markdown, see [Getting started with writing and formatting on GitHub](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/).

3. Optionally, build the HTML files for your website.


## Building HTML files from the MarkDown files
One way you can build the HTML files is by using DocFX, which is an open source tool for converting markdown files. This section provides some guidance on how you can use DocFX to publish HTML files.

1.  Install DocFX on your computer.

    For more information, see [DocFx](https://dotnet.github.io/docfx/).

2.  Specify the output folder in which to store the generated HTML files.

    By default the files will be saved in the folder *c:/output*. The output folder is set in the docfx.json file. If you want to change this folder, do the following:

    a. In the folder [clone path\msftdynamicsgpdocs\dynamics-gp\, open the docfx.json file in your editor.  
    b.  Set the *"dest:"* parameter to your output folder, and save the changes.  

3.  Go to your desktop and open a command prompt.

3.  Go to the docfx installation folder.

4.  Run the following command:
    ```
    docfx "[clone path]\msftdynamicsgpdocs\dynamics-gp\docfx.json"'
    ```

The files are generated as .html files and stored in the specified output.

## Contributing to Dynamics GP content
A benefit of GitHub is the ability for you to contribute to the core content that the Microsoft team provides in the msftdynamicsgpdocs repo. For example, you might have a new article that you think would be beneficial or you might have a correction to an existing article. If you would like to contribute to the msftdynamicsgpdocs repo, you create what is called a *pull request* from your repo to the msftdynamicsgpdocs repo. The Dynamics SMB UA team will then review the request and include the changes as appropriate.

For example, to create a pull request to the msftdynamicsgpdocs repo by using GitHub Desktop, do the following:

1.  Commit the changes to your repo that you want to include in the pull request.
2.  Choose **Sync** to push the changes up to your repo on GitHub.
3.  When the sync is completed, choose **Pull Request**, and then choose send **Pull Request**.

## Contributor guide

Get tips, tools, and guidance in the [Microsoft Docs Contributor Guide](https://docs.microsoft.com/en-us/contribute/).
