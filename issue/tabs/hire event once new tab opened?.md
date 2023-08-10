# How to hire event once new tab opened in JS?
## NO way
There are no way to achievethis in JS since JS does NOT operate between tabs as security issue.
## Way to achieve similar tasks
window.open opens a pop up. You can then access that popup from within your script. Note however that behaviour of how pop-ups are shown vary from browser to browser. Some open it in a new tab, some in a new window, ... Note however that to be able to access the popup, it has to be same domain, protocol, port, ...

## NOTICE
Notice that
The approach, however, doesn't work if the user manually opens a new window/tab to your site because you don't have a reference to it.

## Reference
![image](https://github.com/40843245/JS/assets/75050655/488da683-004d-4bc9-bbbd-70b8e1ad11c4)

https://stackoverflow.com/questions/24698101/open-new-tab-then-listen-for-an-event-being-fired
