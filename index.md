<div style="background-color:#FFEBCD">
  
<h3 style="font:Arial Black;"> Lab Report 1 </h3>
<p style="font:Tahoma;"> October 3, 2023</p>

<h4 style="font:Tahoma;"> Terminal Commands </h4>
<p style="font:Tahoma;"> For week 1's lab, we learned how to use Edstem, a workspace, which has a terminal that we can use to run commands. Three of these such commands are <i>cd</i>, <i>ls</i>, and <i>cat</i>.</p>

<ul style="font:Tahoma;">
  <li><b>cd</b></li>
  
  <table>
  <tr>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.35.35 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.37.49 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.40.01 PM.png"></div></td>
  </tr>
  <tr>
    <td> <div style="length: 620 px">This is an example of using the command cd with no arguments. The working directory was /home. Since there was no argument, cd did nothing, as the command is supposed to change the directory to whatever the argument is. The lack of output is intentional.</div></td>
    <td> <div style="length: 620 px">This is an example of using the command cd on a path to a directory as an argument. In this example, cd changed the working directory from /home to /home/lecture1. The lack of output is intentional, and there is no error, as the directory sucessfully changed. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command cd on a path to a file as an argument. However, since cd needs a directory as an argument (to change the directory into whatever was entered), the command produced an error; both inputs in the example above are files, not directories. </div></td>
  </tr>
</table>
  
  <li><b>ls</b></li>

<table>
  <tr>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.40.40 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.41.11 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.41.38 PM.png"></div></td>
  </tr>
  <tr>
    <td> <div style="length: 620 px">This is an example of using the command ls with no arguments. The command outputs all the files and directories (essentially the contents) within the current directory, which is /home/lecture1. Because there are no arguments, the command outputs the contents of the current directory, by default. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command ls on a path to a directory as an argument. The current directory is /home/lecture1, but since we input /home/lecture1/messages as the input, the command instead prints the directory contents of the input. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command ls on a path to a file as an argument. The current directory is /home/lecture1; normally, the command would print its contents, by default. However, since we used a file as the input, the command only prints out the file itself (as it's the only content within it). </div></td>
  </tr>
</table>

  <li><b>cat</b></li>

<table>
  <tr>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.43.06 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.43.42 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.44.24 PM.png"></div></td>
  </tr>
  <tr>
    <td> <div style="length: 620 px">This is an example of using the command cat with no arguments. The current directory is simply /home. The command produced an error, and in this specific terminal, it stopped accepting further command inputs. This is an error, as cat requires file arguments to output something.</div></td>
    <td> <div style="length: 620 px">This is an example of using the command cat on a path to a directory as an argument. The current directory is /home. In the command, we used the directory /lecture1 as an argument. This produced an error, as cat requires files to print out an output.</div></td>
    <td> <div style="length: 620 px">This is an example of using the command cat on a path to a file as an argument. The current directory is /home, and we are using /lecture1/Hello.java as a file input. This successfully produces an output, which is the contents of the Hello.java file.</div></td>
  </tr>
</table>
  
</ul>

</div>
