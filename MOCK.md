# Mock developement setup

If you want to edit the launcher without having to use the Bridge Launcher app to preview, you can use the Bridge mock api.

Setup instructions:
1. Download index.js from [here](https://unpkg.com/@bridgelauncher/api-mock@latest/dist/index.js)
2. Place it in the project root and rename it to mock.js
3. (On android) Go to the Bridge Launcher app settings and under "Export installed apps" press Export
4. (On android) Make a new folder called mock and export to there
5. Transfer the mock folder to your project root ( `adb pull /storage/emulated/0/mock .` )

Your project root should look like this:
```
<project root>
    |---mock.js
    |---mock/
    |     |---apps.json
    |     |---icons/
    |           |...
    |---index.html
    |...
```
You don't need to edit `index.html` as it handles automatically creating the mock setup when its required.

Pro tip: 
```
python -m http.server 8080
```
will give you a link to preview the launcher, visit `localhost:8080` to see it (make sure you followed the mock instructions first)
(replace `python` with `py` if it doesnt work on windows)
