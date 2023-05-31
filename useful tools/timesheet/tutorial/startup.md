# timesheet
## Objective
This article talks about startup of the useful tool timesheet in JS.
## Prepare
To startup, either do the following way, then import it in the .html file.
### bower
install the git with bower with following command.
    
    bower install https://github.com/sbstjn/timesheet.js.git
### Grunt commands
Use grunt to build all JavaScript and StyleSheet files located inside dist/.

## Import 
You have to import one js file and one css file.

To import a js file, the tag you should use in .html file. Such as 

    <script src="timesheet.min.js"></script>
 
To import a css file, the tag you should use in .html file. Such as 

    <link href="timesheet.min.css" rel="stylesheet">
    
instead of

    <script src="timesheet.min.js"></script>

For the reason, see my other articles in GitHub.

https://github.com/40843245/HTML/blob/main/File/File%20import/tutorial.md

## Create a new Timesheet
To create a new timesheet, just instantiate the object -- Timesheet.
Such as the following example.

                new Timesheet('timesheet', 2002, 2013, [
                ['2002', '09/2002', 'A freaking awesome time', 'lorem'],
                ['06/2002', '09/2003', 'Some great memories', 'ipsum'],
                ['2003', 'Had very bad luck'],
                ['10/2003', '2006', 'At least had fun', 'dolor'],
                ['02/2005', '05/2006', 'Enjoyed those times as well', 'ipsum'],
                ['07/2005', '09/2005', 'Bad luck again', 'default'],
                ['10/2005', '2008', 'For a long time nothing happened', 'dolor'],
                ['01/2008', '05/2009', 'LOST Season #4', 'lorem'],
                ['01/2009', '05/2009', 'LOST Season #4', 'lorem'],
                ['02/2010', '05/2010', 'LOST Season #5', 'lorem'],
                ['09/2008', '06/2010', 'FRINGE #1 & #2', 'ipsum']
                ]);
    
## Ref

In GitHub:

https://github.com/sbstjn/timesheet.js
     
    
