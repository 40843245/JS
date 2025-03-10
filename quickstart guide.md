# quickstart guide
## install Node.JS
You can install Node.JS from [homepage of Node.JS official website](https://nodejs.org/zh-tw)

> [!WARNING]
> After installing, please restart your computer to make the change effect.

## verify Node.JS s fully installed
You can verify it in `node` command in terminal.

```
node -v
```

This command will output version of Node.JS to console.

## install npm command-line tool
npm command-line tool is fully installed by default when installing Node.JS from [homepage of Node.JS official website](https://nodejs.org/zh-tw)

> [!WARNING]
> If you want to use `npm` command in terminal other than `DOS command-line prompt`.
>
> Please add the location of `npm.cmd` to environment system variable - `PATH`.
 
## verify npm command-line tool s fully installed
You can verify it in `npm` command in terminal.

```
npm -v
```

> [!NOTE]
> You may encounter this issue
>
> ```
> npm : C:\Program Files\nodejs\npm.ps1 檔案無法載入。檔案 C:\Program Files\nodejs\npm.ps1 未經數位簽署
> ```
>
> When executing `npm -v` command in VSC terminal.
>
> It indicates that file `C:\Program Files\nodejs\npm.ps1` is not certificated by VSC.
>
> For more explanation of Google Gemini's answer, see [npm.ps1 is not certificated](https://github.com/40843245/npm/blob/main/Q&A/npm.ps1%20is%20not%20certificated.md)
## install other module
You can install other module with `npm` command in terminal.

```
npm install <ModuleName>
```

where

`<ModuleName>` is the module name you want to install.

## reference
+ [Downloading and installing Node.js and npm (npm docs)](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
+ [Download Node.js® (Node.JS docs)](https://nodejs.org/zh-tw/download)
