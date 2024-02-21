# Saving Skeema Projects to Disk as a Backup HTML file

SOOOO, I have solved how to backup your Skeema Project files from the Skeema server to a locally-available HTML file.

The main issue was that when you saved them as any of the three types commonly available, NONE of the saved files, HTML or MHT, showed any content.

This is because the file is not set to be renderable easily, or by the Skeema folks, so you have to put a base reference line in there yourself.

## Steps to Do (Endure):
1. First navigate to the project's page in Skeema in your browser. We'll use my <a href="https://web.skeema.com/p/bAxcuK8tnH5Yvz8qeTyD">**Liascript and Such**</a> Skeema Project shared page as an example throughout.
2. Hit the **Share** icon on the top right of the Project page.
3. Slide the slider over to show blue on the **Get viewer link** section.
4. Click the **Open in new tab** icon to the right of the URL dialog, which is a small square with an arrow pointing to the top right of the square.
5. This will open the Shared Skeema page in a new tab in your browser.
6. Use the **FILE -> SAVE** function in your browser to save the file locally, using the **__Webpage, Complete__** format.  NOTE:  This will NOT work otherwise.
7. Edit the HTML file you saved to disk, (say with Atom or VS Code) and at the top of the file you'll find a line that is similar to the below:
    ```
    <!-- saved from url=(0045)https://web.skeema.com/p/bAxcuK8tnH5Yvz8qeTyD -->
    ```
8.  While in that file, add a line to the **_TOP_** of the file that replaces my `SKEEMSHAREURLHERE` with the proper URL from the line above.
    ```
    <base href="SKEEMASHAREURLHERE">
    ```
9.  This will give you a file with the top two lines that look like this:
    ```
    <base href="https://web.skeema.com/p/bAxcuK8tnH5Yvz8qeTyD">
    <!-- saved from url=(0045)https://web.skeema.com/p/bAxcuK8tnH5Yvz8qeTyD -->
    ```
10.  Save this file, it's now able to show the URL's from the Skeema page you saved.
11.  Just load it in the browser by double-clicking on it or use the **FILE -> OPEN** menu option.

**Note:**  yes, there are things that could work better, all the circles and fancy icons aren't working, but you can now save your project pages locally and not LOSE everything if Skeema goes away.

Enjoy!
