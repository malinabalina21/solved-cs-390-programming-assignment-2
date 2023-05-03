Download Link: https://assignmentchef.com/product/solved-cs-390-programming-assignment-2
<br>
<h1>Introduction</h1>

The shell is the primary means for user interaction with a unix system. The shell is a program like any other program and has the capabilities built into the logic to implement the functionality users require.




<h1>AssignmentDescription</h1>

This assignment is to update the shell program assigned in Program 1. The additional capabilities are 1) implement command execution, and 2) implement a additional program called myls.c which will read a directory and display the contents.




<h1>ProgramRequirements</h1>

<ol>

 <li>The student shall create an application which will implement a command loop and accept the commands defined by the following requirements.</li>

 <li>The student shall implement the command execution routine to execute an external command submitted to the shell program.</li>

 <li>The command execution routine shall recognize a simple program name or an absolute path.</li>

 <li>The exec( ) command shall be “ int execv(const char *path, char *const argv[]);”</li>

 <li>When a simple program name is used the program shall use getenv( “PATH”) to find the program location.</li>

 <li>The student shall implement a separate program call myls.c which will display the contents of a directory.</li>

 <li>c shall accept no argument or the “-a” arg as in the “ls” command and behave accordingly.</li>

 <li>The name of the program shall be “mysh2”, an abbreviation of “my shell”. The program must be written in “C” and named “mysh2.c.</li>

 <li>The name of the directory list program shall be “myls”. This program must be written in “C” and named “myls.c”.</li>

 <li>The student will “tar” the program. The tar command for the “C” program is :</li>

 <li><strong>$ tar czf studentlastname_mysh2.tgz c myls.c</strong></li>

</ol>




<h1>SubmissionGuidelines</h1>

<ol>

 <li>The assignment shall be uploaded to the instructor using the <strong>CANVAS</strong></li>

 <li>The tar file shall use the following naming convention:</li>

</ol>

<strong>studentlastname_mysh2.tgz</strong>. For example, if your last name is “smith” the filename would be <strong>smith_mysh2.tgz</strong>. The <strong>myls.c</strong> file shall be in the tar file.

<ol start="3">

 <li>The assignment will be due Tuesday, March 26, 2019.</li>

 <li>The assignment may be turned in Thursday, March 28, 2019 for a mandatory loss of one letter grade. The assignment will not be accepted after this date.</li>

</ol>

AN EXAMPLE OF ARGV USAGE:




#define TRUE  1

#define FALSE 0




int main(int argc,const char* argv[])

{     int status = 0;     int arg1,flagError;




flagError = FALSE;




if (argc == 1)

{

arg1 = FALSE;

}

else if (argc == 2)

{

if (strcmp(argv[1],”-a”) == 0)

{

arg1 = TRUE;

}         else         {

printf(“ERROR: invalid argument
”);             flagError = TRUE;

}

}     else     {

printf(“Usage: $ ls [-a]
”);

}




if (flagError == FALSE)

{

/* DO CODE */

}     else     {

status = 1;

}     return status; }


